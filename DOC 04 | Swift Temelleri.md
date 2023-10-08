# Temeller
### <ins>*Yaygın veri türleriyle çalışın ve temel syntax yazın.*</ins>



Swift, iOS, macOS, watchOS ve tvOS uygulama geliştirmek için bir programlama dilidir. C veya Objective-C'de geliştirme deneyiminiz varsa, Swift'in birçok bölümü size tanıdık gelecektir.

Swift, tüm temel C ve Objective-C tiplerinin kendi versiyonlarını sağlar; bunlar arasında tamsayılar için Int, kayan nokta değerleri için Double ve Float, Boolean değerleri için Bool ve metinsel veri için String bulunmaktadır. Swift, [Koleksiyon Türleri](https://github.com/serkanalc/The-Swift-Programming-Language-TR/blob/main/DOC%2007%20%7C%20Koleksiyon%20T%C3%BCrleri.md) bölümünde açıklandığı gibi, Array, Set ve Dictionary olmak üzere üç ana koleksiyon tipinin güçlü versiyonlarını da sağlar.

C gibi Swift, değerleri saklamak ve bir tanımlayıcı adıyla referans almak için değişkenleri kullanır. Swift, değerlerinin değiştirilemediği değişkenlerin de geniş bir kullanımını yapar. Bunlara sabitler denir ve C'deki sabitlerden çok daha güçlüdürler. Değişmemesi gereken değerlerle çalışırken kodu daha güvenli ve amacı daha açık hale getirmek için Swift boyunca sabitler kullanılır.

Tanıdık tiplere ek olarak, Swift, Objective-C'de bulunmayan ileri tipleri, örneğin demetleri (tuples) tanıtır. Demetler, değer gruplamalarını oluşturmanıza ve aktarmanıza olanak tanır. Bir işlevden tek bir bileşik değer olarak birden çok değeri döndürmek için bir demet kullanabilirsiniz.

Swift ayrıca, bir değerin olmamasını ele alan opsiyonel tipleri de tanıtır. Opsiyoneller “bir değer var ve bu x'e eşit” veya “hiçbir değer yok” şeklinde ifade edilir.

Swift, tür güvenliği olan bir dildir, bu da dilin kodunuzun hangi değer türleriyle çalışabileceği konusunda size net olmanıza yardımcı olduğu anlamına gelir. Kodunuzun bir bölümü String gerektiriyorsa, tür güvenliği ona yanlışlıkla bir Int geçirmenizi engeller. Aynı şekilde, tür güvenliği bir kod parçasına yanlışlıkla opsiyonel olmayan bir String yerine opsiyonel bir String geçirmenizi engeller. Tür güvenliği, hataları geliştirme sürecinde olabildiğince erken yakalamanıza ve düzeltmenize yardımcı olur.

Sabitler ve Değişkenler Sayfa Bağlantısı
Sabitler ve değişkenler, bir ismi (örneğin maximumNumberOfLoginAttempts veya welcomeMessage) belirli bir tipin değeriyle (örneğin 10 numarası veya "Merhaba" stringi) ilişkilendirir. Bir sabitin değeri belirlendikten sonra değiştirilemezken, bir değişkenin değeri gelecekte farklı bir değere ayarlanabilir.

Sabitlerin ve Değişkenlerin Bildirimi Sayfa Bağlantısı
Sabitler ve değişkenler kullanılmadan önce bildirilmelidir. Sabitleri let anahtar kelimesiyle ve değişkenleri var anahtar kelimesiyle bildirirsiniz. İşte sabitlerin ve değişkenlerin bir kullanıcının kaç kez giriş yapmayı denediğini izlemek için nasıl kullanılabileceğine dair bir örnek:
