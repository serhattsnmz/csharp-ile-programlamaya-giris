## TÜR DÖNÜŞÜMLERİ

### 01 – Tür Dönüşümleri ( Bilinçli – Bilinçsiz ) 
- Sayısal türleri birbirine dönüştürmek için kullanılır.
- Bilinçsiz dönüştürme
    - Direk eşitleyerek elde edilir.
- Bilinçli dönüştürme
    - Eşitlemeden önce, parantez içine dönüştürülecek tip yazılır.

### 02 – Parse ve TryParse ile Dönüşüm
- String ifadeleri sayısal türlere dönüştürmek için kullanılır.
- TryParse() yöntemi ile dönüşümde, dönüşüm sonucunu bool olarak bir değişkene atayıp kontrol gerçekleştirebiliriz. 

```cs
string gelenDeger = Console.ReadLine();

int sayi;
bool sonuc = int.TryParse(gelenDeger, out sayi);

if (sonuc)
    Console.WriteLine("Değer dönüşümü yapıldı.");
else
    Console.WriteLine("Dönüşüm yapılamadı!");
```

### 03 – Tür Dönüşümleri ( Boxing ve Unboxing )
- Verileri object üzerinde kutulama.
- Kutudan çıkarırken bilinçli dönüşüm ile tür dönüşümü yapma

### 04 – Tür Dönüşümleri ( Convert Sınıfı ile Dönüşüm )
