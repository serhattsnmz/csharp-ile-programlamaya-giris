## OOP KAVRAMLAR

### 01 – Encapsulation ( Kapsülleme )
- Bir sınıf içindeki değişkenlere dışarıdan erişimi sağlamak, ancak değişken içeriğinde değişiklik yapılmasını engellemek için kullanılır. Bunun için öncelikle değişkeni private olarak tanımlayıp, daha sonra Read Only property ile değişken üzerinde değişiklik yapılmasını engelleriz. Bu işleme Encapsulation denir.

### 02 – Inheritance ( Miras Alma )
- Bir class’ın başka bir class özellikleri barındırmasına, burdan kalıtım alma denir.
- Sadece bir sınıftan miras alınabilir.
- Miras alan bir sınıfın başka bir sınıfa kalıtım vermesi

### 03 – Overloading ( Aşırı Yükleme )
- Bir fonksiyonun birbirinden farklı parametreler almak koşuluyla, aynı isimle birden çok tanımlanması. 
- Overload ettiğimiz fonksiyonlarda, parametre isimleri önemli değildir. Önemli olan, metotların imzasıdır. ( parametre türleri ).

### 04 – Overriding ( Metotları Ezme )
- Miras alınan sınıfın özellik ve metotları üzerinde değişiklik yaparak tekrardan yazma işlemdir.
- Miras alınan sınıf içindeki özellik veya metot ismi aynen yazılarak, yeni değişiklikler yapılır.
    - Bu yeni sınıftan türeyen nesneler artık bu özellik ve metotları kullanır.
- Bu işlemi yapmak için :
    - Herhangi bir önek eklenmeden direk aynı isimle yeni metot yazılabilir. Fakat uyarı verir. ( Hata değil! )
    - Bunu bilinçli olarak yaptığımızı belirtmek için yeni metodun başına new öneki getirilebilir.
    - Eski metodun başına virtual, yeni metodun başına override ifadesi getirilebilir.
    - Eski metot abstract olarak tanımlanmışsa yeni metot için birşey yapmaya gerek yoktur.

### 05 – Virtual ( Sanal ) Metotlar
- Miras alınan sınıftaki metoların ezilip ( overriding ) tekrar yazılmasıdır.
- Miras alınan sınıftaki metodun “virtual” olarak, yeni yazılan metodun ise “override” olarak belirtilmesi gerekmektedir. 

```cs
class insan
{
    public string Ad { get; set; }
    public string Soyad { get; set; }

    public virtual void Yaz()
    {
        Console.WriteLine(Ad + " " + Soyad);
    }
}

class kisi : insan
{
    public string unvan { get; set; }
    public override void Yaz()
    {
        Console.WriteLine(unvan + " " + Ad + " " + Soyad);
    }
}
```

### 06 – Abstract ( Soyut ) Sınıflar
- New anahtar kelimesiyle yeni bir nesne türetilemeyen sınıflardır.
- Özellikle, sadece başka sınıflara miras vermek amacıyla yazılan sınıflarda kullanılır.
    - Sınıf türetilirken kullanılması gereken metot ve propery’lerin bulunduğu bir sınıftır. 
- Abstact sınıflar içine abstract metotlar yazılabilir ve bunlar ezilerek veya kendi halinde alt sınıflarda kullanılır.
    - Abstract metotlar alt sınıflarda kullanılamaz.
    - Bu nedenle Abstract metotlarda kod yazılmaz. 
    - Abstract metotlar, alt sınıflar için bir metot haritası oluşturur ve alt sınıf oluşturulduğunda, bu metotlar üst sınıftan implament edilerek override edilir.
- Abstract sınıflar içine abstract property’ler de tanımlanabilir. 
    - Bu property’lerin de implament edilerek ezilmesi gereklidir.
    - İmplamentasyon yapılmazsa derleme hatası oluşur.

### 07 – Sealed ( Mühürlü ) Sınıflar
- Abstract sınıfların tam tersi olarak düşünülebilir.
- New ile türetilebiler ama başka bir sınıfa kalıtım veremez.
- Genellikle static metotlardan oluşan class yapıları için kullanılır.

### 08 – Interfaces ( Arayüzler )
- Kodların yazılmadığı, sadece implament edilecek property ve metotları bulunduran class yapısıdır.
- Interface içindeki tüm metotlar
    - Abstract olarak kabul edilir.
    - Public olarak kabul edilir.
    - Türetilen sınıflarda override kullanmaya gerek yoktur.
- Interface isimlendirmesi standart olarak “I” ile başlar.
- Bir class birden fazla interface’den implament edilebilir.
- Interface’lerden nesne üretilemezler.
- Interface’ler içindeki tanımlamalara;
    - Erişim öneki getirilemez. Hepsi default olarak public olur.
    - Static keyword’ü kullanılamaz.
    - Field’lar kullanılamaz. Sadece metot ve property
    - Construction metotlar tanımlanamaz.

### 09 – Polymorphism ( Çok Biçimlilik )
- Virtual olarak belirttiğimiz üst sınıftaki metodun, alt metotlarda ezilmesi olayına polymorphism denir.

### 10 – Partial ( Kısmi ) Sınıflar
- Bir class elemanlarını parça halinde yazma anlamına gelir. 
- Partial olarak tanımlanmış bir class, aynı isimle yine tanımlanarak yeni özellikler eklenmesi sağlanabilir.