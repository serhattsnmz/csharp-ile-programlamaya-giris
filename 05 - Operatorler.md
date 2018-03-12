## OPERATORLER

### 01 – Aritmetik Operatörler
- Toplama ( + )
- Çıkarma ( - )
- Çarpma ( * )
- Bölme ( / )
- Mod ( % )
- Eksiltme ( -- )
- Çoğaltma ( ++ )

## 02 – Aktarma Operatorleri
- Aktarma ( = )
- Topla Aktar ( += )
- Çıkar Aktar ( -= )
- Çarp Aktar ( *= )
- Böl Aktar ( /= )
- Üs Al Aktar ( ^= )
- Mod Al Aktar ( %= )
- Ve Aktar ( &= )
- Veya Aktar ( |= )

### 03 – Mantıksal Operatörler
- Ve ( & ) 
    - Her iki yöne de tek tek bakar. 
- Veya ( | )
    - Her iki yöne de tek tek bakar.
- Ve Değil ( && )
    - İlk değişken true ise and işlemi gerçekleştirir. False ise ikinci değişkene bakmaksızın false döndürür.
- Veya Değiş ( || )
    - İlk değişken false ise or işlemi gerçekleştirir. True ise ikinci değişkene bakmaksızın true döndürür. 
- Özel Veya ( ^ )
    - İki değişkenden biri diğerinden farklı olduğunda true üretir.
        - True ^ False = True
        - True ^ True = False
        - False ^ False = False
        - False ^ True = True
- Değil ( ! )
    - Değişken değerini tersine çevirir.
- Null Coalescing ( ?? )
    - Eğer ilk değişken null ise ikinci değişken hesaplanır. Aksi taktirde hesaba koyulmaz.
- Koşul operatorü ( ?: )

### 04 – Karşılaştırma Operatörleri
- Büyüktür ( > )
- Küçüktür ( < )
- Büyük veya eşittir ( >= )
- Küçük veya eşittir ( <= )
- Eşittir ( == )
- Eşit değildir ( != )
- Uzaklaştırma operatörü ( --> )
- Yakınlaştırma operatörü ( <-- ) 

```cs
int i = 3;
while (i --> 0)
    Console.WriteLine(i);
Console.ReadKey();

// OUTPUT:
// 2
// 1
// 0
```