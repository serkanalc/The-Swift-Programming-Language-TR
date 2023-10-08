# Temeller
### <ins>*Yaygın veri türleriyle çalışın ve temel syntax yazın.*</ins>



Swift, iOS, macOS, watchOS ve tvOS uygulama geliştirmek için bir programlama dilidir. C veya Objective-C'de geliştirme deneyiminiz varsa, Swift'in birçok bölümü size tanıdık gelecektir.

Swift, tüm temel C ve Objective-C tiplerinin kendi versiyonlarını sağlar; bunlar arasında tamsayılar için Int, kayan nokta değerleri için Double ve Float, Boolean değerleri için Bool ve metinsel veri için String bulunmaktadır. Swift, [Koleksiyon Türleri](https://github.com/serkanalc/The-Swift-Programming-Language-TR/blob/main/DOC%2007%20%7C%20Koleksiyon%20T%C3%BCrleri.md) bölümünde açıklandığı gibi, Array, Set ve Dictionary olmak üzere üç ana koleksiyon tipinin güçlü versiyonlarını da sağlar.

C gibi Swift, değerleri saklamak ve bir tanımlayıcı adıyla referans almak için değişkenleri kullanır. Swift, değerlerinin değiştirilemediği değişkenlerin de geniş bir kullanımını yapar. Bunlara sabitler denir ve C'deki sabitlerden çok daha güçlüdürler. Değişmemesi gereken değerlerle çalışırken kodu daha güvenli ve amacı daha açık hale getirmek için Swift boyunca sabitler kullanılır.

Tanıdık tiplere ek olarak, Swift, Objective-C'de bulunmayan ileri tipleri, örneğin demetleri (tuples) tanıtır. Demetler, değer gruplamalarını oluşturmanıza ve aktarmanıza olanak tanır. Bir işlevden tek bir bileşik değer olarak birden çok değeri döndürmek için bir demet kullanabilirsiniz.

Swift ayrıca, bir değerin olmamasını ele alan opsiyonel tipleri de tanıtır. Opsiyoneller “bir değer var ve bu x'e eşit” veya “hiçbir değer yok” şeklinde ifade edilir.

Swift, tür güvenliği olan bir dildir, bu da dilin kodunuzun hangi değer türleriyle çalışabileceği konusunda size net olmanıza yardımcı olduğu anlamına gelir. Kodunuzun bir bölümü String gerektiriyorsa, tür güvenliği ona yanlışlıkla bir Int geçirmenizi engeller. Aynı şekilde, tür güvenliği bir kod parçasına yanlışlıkla opsiyonel olmayan bir String yerine opsiyonel bir String geçirmenizi engeller. Tür güvenliği, hataları geliştirme sürecinde olabildiğince erken yakalamanıza ve düzeltmenize yardımcı olur.

### Sabitler ve Değişkenler Sayfa Bağlantısı
Sabitler ve değişkenler, bir ismi (örneğin maximumNumberOfLoginAttempts veya welcomeMessage) belirli bir tipin değeriyle (örneğin 10 numarası veya "Merhaba" stringi) ilişkilendirir. Bir sabitin değeri belirlendikten sonra değiştirilemezken, bir değişkenin değeri gelecekte farklı bir değere ayarlanabilir.

### Sabitlerin ve Değişkenlerin Bildirimi Sayfa Bağlantısı
Sabitler ve değişkenler kullanılmadan önce bildirilmelidir. Sabitleri let anahtar kelimesiyle ve değişkenleri var anahtar kelimesiyle bildirirsiniz. İşte sabitlerin ve değişkenlerin bir kullanıcının kaç kez giriş yapmayı denediğini izlemek için nasıl kullanılabileceğine dair bir örnek:

```swift
let maximumNumberOfLoginAttempts = 10
var currentLoginAttempt = 0
```
Bu kod şu şekilde okunabilir:

“*maximumNumberOfLoginAttempts* adında yeni bir sabit tanımla ve ona 10 değerini ver. Ardından, *currentLoginAttempt* adında yeni bir değişken tanımla ve ona başlangıç değeri olarak 0 ver.”

Bu örnekte, izin verilen maksimum giriş denemesi sayısı değişmeyen bir maksimum değer olarak sabit olarak tanımlanmıştır. Şu anki giriş denemesi sayacı, her başarısız giriş denemesinden sonra artırılması gereken bir değer olduğu için değişken olarak tanımlanmıştır.

Tek bir satırda virgülle ayrılarak birden fazla sabit veya birden fazla değişken tanımlayabilirsiniz:

```swift
var x = 0.0, y = 0.0, z = 0.0
```
> **_NOT:_**
> Kodunuzdaki depolanan bir değer değişmeyecekse, her zaman onu let anahtar kelimesiyle bir sabit olarak tanımlayın. Değiştirilebilir olması gereken değerleri depolamak için yalnızca değişkenleri kullanın.

### Tür Açıklamaları Sayfa Bağlantısı

Bir sabit veya değişken tanımladığınızda, sabitin veya değişkenin hangi türde değerleri saklayabileceği konusunda açık olmak için bir tür açıklaması sağlayabilirsiniz. Bir tür açıklaması yazmak için sabit veya değişken adından sonra iki nokta üst üste koyun, ardından bir boşluk bırakın ve kullanılacak türün adını yazın.

Bu örnek, *welcomeMessage* adlı bir değişken için bir tür açıklaması sağlar ve bu değişkenin String değerlerini saklayabileceğini belirtir:

```swift
var welcomeMessage: String
```

Yukarıdaki tanımlamadaki iki nokta üst üste "... türünde ..." anlamına gelir, bu nedenle yukarıdaki kod şu şekilde okunabilir:

“String türünde welcomeMessage adında bir değişken tanımla.”

“String türünde” ifadesi “herhangi bir String değerini saklayabilir” anlamına gelir. Bunun “saklanabilecek şeyin türü” (veya “saklanabilecek şeyin çeşidi”) anlamına geldiğini düşünün.

Şimdi welcomeMessage değişkeni herhangi bir string değerine hata olmadan ayarlanabilir:

```swift
welcomeMessage = "Hello"
```
Tek bir satırda, virgülle ayrılmış, final değişken adından sonra tek bir tür açıklamasıyla aynı türde birden çok ilişkili değişken tanımlayabilirsiniz:

```swift
var red, green, blue: Double
```

> **_NOT:_**
> Pratikte tür açıklamaları yazmanız gerektiği nadirdir. Bir sabit veya değişken için tanımlandığı noktada bir başlangıç değeri sağlarsanız, Swift bu sabit veya değişken için kullanılacak türü neredeyse her zaman çıkarabilir, Tür Güvenliği ve Tür Çıkarımı bölümünde açıklandığı gibi. Yukarıdaki HoşgeldinizMesajı örneğinde başlangıç değeri sağlanmamıştır ve bu nedenle HoşgeldinizMesajı değişkeninin türü, bir başlangıç değerinden çıkarılmak yerine bir tür açıklamasıyla belirtilmiştir.



  
