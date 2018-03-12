## OBJECT ORIENTED PROGRAMMING

### 01 – Class Nedir? 
- Class yapısı, birden çok veriyi paketleyen bir paketleyici olarak düşünülebilir.
- Class yapısı içinde o class’a ait özellikleri alan alanlar açılır.
    - Örn : canlılar > hayvanlar > kedigiller > van kedisi 
- Class yapıları soyut yapılardır. Nesne türetilip somut hale getirilebilir. 
    - Somut hale getirilme, new ile yapılır.
    - New kullanılmadan class tanımlanırsa, sadece referans almış olur, nesne oluşmaz.
- İçerisinde değişkenler ve metotlar barındırabilir.
- Class’ları ana kısımda ve ayrı bir dosya olarak tanımlama
- Class yapıları, proje içinde direk kullanılabileceği gibi, dll dosyası haline getirilip ( class library ) başka projelere dışarıdan da dahil edilebilir.

### 02 – Erişim Belirleyiciler
- Private
- Public

### 03 – Field Kavramı

### 04 – Property ve Auto-Implemented Property
- Get ve Set için ayrı ayrı metotlar tanımlama
- Bu metoları kısa olarak property olarak yazma
- Auto Property kullanarak ayrı ayrı field ve ilgili property tanımından kurtulma
- Auto Property Initializers
    - Property tanımlarken varsıyılan değer ataması yapılabilir.
    - C# 6 + 
- Read Only Auto Property
    - Set metodunun yazılmadığı property
    - Bu property üzerine atama yapılamaz. Initializer ile veya constractor ile atama yapılabiilr.

### 05 – This Anahtar Sözcüğü
- İçinde bulunduğu class’ı belirtir.
- Kullanılması zorunlu değildir. Fakat okunabilirlik açısından ve class içindeki elemanlara otomatik erişim için yararlıdır.

### 06 - Constructors ( Yapıcı Metodlar )
- C# içinde, new ile bir nesne türettiğimiz zaman, nesne, constructor metot ile kurulur. Bu metodun tanımlanmadığı durumlarda, C#, default cont metot kullanarak tüm değişkenlere default değerleri kendi atar ve nesneyi bu şekilde oluşturur.  
Kendimiz cont metot tanımlarsak, nesne oluşturulurken bu metot baz alınır ve default ayarlamalar bu metot üzerinden yapılır.
- Dönüş tipi almazlar. Erişim tipi her zaman public olmak zorundadır.
- Parametre alabilirler ve overload edilebilirler.
- Metot isimleri, sınıf isimleriyle aynı olmak zorundadır.
- Ctor + tab + tab -> Kısa yolu
- Constructors ile field’lara default değer atama
- Nesne ürettikten sonra bu verileri ezme
- Constructors ile nesne oluştururken zorunlu olarak alan girilmesini sağlama
- Birden fazla, overloading constructor method oluşturma

### 07 – Destructors ( Yıkıcı Metotlar )
- C# içinde bizim tanımladığımız sınıflar yada framework ile birlikte gelen yerleşik sınıfları hafızaya çıkarıp birer nesne oluşturduğumuz vakit hafızadan  silimeden hemen önce çalışan metotlardır.
- Destructor metotlar çağırılamazlar.
- Overload edilemezler. Bir tane bulunur.
- Erişim belirleyicileri yoktur.
- Kalıtımları yoktur, miras alınamazlar.

### 08 – Static Üyeler
- Soyut class’lar içinde somut veriler ve fonksiyonlar tutmaya yarar.
- Statik üyeler, nesne oluşturulmadan direk kullanılır. Nesne oluşturulduğu zaman kullanılamaz.
- Nesneler oluşturulduğu zaman, dinamik yapıda olduğundan dolayı garbage collector tarafından işleri bittiğinde silinir. Static üyeler ise program bitene kadar ram üzerinde saklanır ve silinmez.
- Static olarak tanımlanmış metolar içinde sadece statik değişkenler ve metotlar kullanılabilir.