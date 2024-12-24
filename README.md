# Otomasyon Kodu README

Bu Python otomasyon kodu, `pyautogui` kütüphanesini kullanarak bir dizi fare hareketi ve klavye işlemi gerçekleştirir. Kod, ekran boyutlarını alır, fareyi ekranın ortasına taşır, sağa hareket ettirir, tıklama yapar, bir yazı yazar ve son olarak ESC tuşuna basar.

## Gereksinimler

Bu kodu çalıştırabilmek için öncelikle `pyautogui` kütüphanesinin yüklü olması gerekir. `pyautogui` kütüphanesini yüklemek için aşağıdaki komutu terminal veya komut satırında çalıştırabilirsiniz:

```bash
pip install pyautogui
```

## Kodun Açıklaması

1. **Ekran Boyutlarını Almak:**
   ```python
   screen_width, screen_height = pyautogui.size()
   ```
   Bu satır, ekranın genişlik ve yüksekliğini alır.

2. **Fareyi Ekranın Ortasına Taşımak:**
   ```python
   pyautogui.moveTo(screen_width / 2, screen_height / 2, duration=2)
   ```
   Fareyi ekranın ortasına doğru 2 saniyede hareket ettirir.

3. **2 Saniye Bekleme:**
   ```python
   time.sleep(2)
   ```
   Fare hareketinin ardından 2 saniye bekler.

4. **Fareyi Sağa Doğru Hareket Ettirme:**
   ```python
   pyautogui.move(200, 0, duration=1)
   ```
   Fareyi sağa doğru 200 piksel hareket ettirir, bu işlem 1 saniye sürer.

5. **Fare ile Tıklama Yapma:**
   ```python
   pyautogui.click()
   ```
   Farenin mevcut konumunda bir sol tıklama yapar.

6. **Klavyeye Yazı Yazma:**
   ```python
   pyautogui.typewrite('Merhaba, bu bir otomasyon örneğidir!', interval=0.1)
   ```
   Klavye ile 'Merhaba, bu bir otomasyon örneğidir!' yazısını yazar. Her karakter arasında 0.1 saniye gecikme vardır.

7. **2 Saniye Bekleme:**
   ```python
   time.sleep(2)
   ```
   Yazı yazdıktan sonra 2 saniye bekler.

8. **ESC Tuşuna Basma:**
   ```python
   pyautogui.press('esc')
   ```
   ESC tuşuna basar.

## Kullanım

Bu kodu çalıştırmak için Python yüklü bir bilgisayarda `pyautogui` kütüphanesini kurduktan sonra, kodu bir Python dosyasına yazıp çalıştırabilirsiniz. Kodu çalıştırmadan önce, ekranınızda yazı yazabileceğiniz bir metin kutusu veya uygulama açmayı unutmayın.

## Dikkat Edilmesi Gerekenler

- Kod, ekranın ortasına fareyi taşırken, aktif pencerenin bir metin alanı veya klavye ile yazı yazılabilir bir uygulama olması gerekir.
- `pyautogui` kütüphanesi, fare hareketleri ve tıklamalar gibi işlemleri gerçekleştirdiğinden, dikkatli kullanılması gerekir. Yanlış bir uygulamada istenmeyen değişiklikler yapabilir.

Bu otomasyon kodu, temel fare hareketlerini ve klavye yazmalarını otomatikleştirir ve bilgisayar üzerinde basit otomasyon görevleri için kullanılabilir.
