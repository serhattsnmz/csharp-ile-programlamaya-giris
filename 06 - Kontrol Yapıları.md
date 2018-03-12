## KONTROL YAPILARI

### 01 – If - Else If - Else Yapısı
### 02 – Switch Case Yapısı
- Case yapısı içinde goto ile başka bir case içine yönlendirme

```cs
int not = int.Parse(Console.ReadLine());
switch (not)
{
    case 0: Console.WriteLine("Kaldınız"); break;
    case 1: goto case 0;
    case 2: goto case 0;
    case 3: Console.WriteLine("Geçtiniz"); break;
    case 4: goto case 3;
    case 5: goto case 3;
    default: break;
}
```