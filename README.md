Java Nedir?

1995 yılında Sun Microsystems tarafından geliştirilmiş olup şuanda Oracle'ın sahip olduğu programlama dilidir.
Nesne yönelimli , platformdan bağımsız programlama dilidir.(JVM)(Bir kez yaz her yerde çalıştır.)
Java; web siteleri , mobil uygulamalar , oyun geliştirme , gömülü sistemler , masaüstü uygulamalarında yaılım geliştirmek için kullanılır.

Java Nasıl Çalışır? Java kaynak kodu bytecode'na derleyerek çalışır. Daha sonra bytecode  JVM sanal makine ile makine koduna derlenebilir. Java'nın bytecode
JVM'e sahip herhangi bir cihazda çalışabilir. Her işletim sistemi kendi (JVM) java sanal makinesine sahip olduğunda java'yı bilgisayarların analayabileceği koda
dönüştüren ana platformdan bağımsız bir ortam olmasını sağlar.

JVM (Java Virtual Machine): Java programlarını çalıştıran ortamdır. Yazılmış olan kodu önce bytecode'a dönüştürür ve JVM bytecode'u çalıştırır. Bu sayede
platform bağımsızlığını sağlar.
-----
JRE (Java Runtime Environment): JVM ve kütüphanelerden oluşur, Java uygulamalarını çalıştırmak için gerekli olan tüm  araçları içerir. Java programlarının 
işletim sistemi arasında iletişim kuran temel teknolijidir.
Java API (Java’nın kütüphaneleri ve sınıfları) bulundurur.
-----
JDK (Java Development Kit): Java uygulamaları geliştirmek için kullanılan araç setidir. JRE'yi içermektedir ve bunun üzerine java kodu yazmayı, 
derlemeyi ve hata ayıklamayı sağlayan araçları ekler.
Derlenen java kodunu bytecode'a (javac tarafından oluşturulan .class dosyalarına dönüştürür.)


Özellik			JVM				JRE					JDK
Amacı		Java bytecode’u çalıştırır.	Java uygulamalarını çalıştırır. 	Java uygulamalarını geliştirir.
Kapsamı		Yalnızca çalıştırma ortamı.	   JVM + Kütüphaneler.	                 JRE + Derleyici ve araçlar.
Kim Kullanır?	      Kullanıcılar		       Kullanıcılar			      Geliştiriciler

Geliştirici -> Kod bloğu -> JDK derleyici -> ByteCode -> Kullanıcı -> Çalıştırma Komutu > JRE -> JVM ByteCode'u çalıştırır.
Java kodu yazmak geliştirmek için Ide gerekli değildir.

JDK yükle -> Metin Editörü(SublimeText , Notepad) -> Örnek HellWorld yaz. -> Dosya uzantısını .java olarak kaydet. > Komut İstemi CMD 
>Bulunduğu dizin yazılır -> javac dosyaadı.java ile dosyayı derle. > Sonucunda dosyaadı.class adında bytecode dosyası oluşmakta 
> Başarılı ise java dosyaadı olarak çalıştır. Doğru ise println("HelloWorld!"); karşınıza gelicek.

IDE: İntegrated development environment => Tümleşik Entegre geliştirme ortamı -> Programlama sürecleri için kullanılan yazılım uygulamasıdır.
Özellikleri : Söz dizimlerini vurgulama: Programlama veya parantes gibi yazım kuralı olan hataları renklendirerek gösterip kolaylık sağlar. Sınıf , döngü , fonksiyon
tanımla yapılmalarını kolaylaştırır.


1-Temel Programlama Kavramları
   a.Değişkenler(Variables)
 Değişlenler veriyi saklamak için kullanılan isimlendirilmiş bellek alanlarıdır.
 Bir değişken bellirli bir veri tipine sahip olabilir ve bu deperi değiştirebiliriz.
 Değişkenler programda bir isimle tanımlanır. Bir değikeni tanımlarken önce veri tipi belirtiriz , sonra değişkenin ismini ve değerini atarız.

   b.Veri Tipleri(Data Types)
Veri tipleri değişkenlerde saklanan veri türünü belirtir.
	İnteger -> int > Tam sayılar için kullanılır.
	Float   -> float > Ondalıklı veya kesirli sayılar için kullanılır. (Virgül)
	String  -> Metinsel ifadeler için kullanılır. "a" , 'a' şeklinde kullanabiliriz.
	Boolean -> Mantıksal değerler için kullanılır.
	List 	-> Birden fazla veriyi bir arada tutmak için kullanılır farklı veri tiplerinde olabilir. ["bmw" , "audi" , "mercesedes"] [1,2,3]

/*	
	int:Tam sayılar için kullanılır.(32 bitlik bellek alanı kapsar. 4 byte)
	byte:Küçük tam sayıları saklamak için kullanılır. (2byte, -128 ile 127 arası)	
	short:int'en daha küçük aralıklı sayılar için kullanılır. (2byte, -32,768 ile 32,767 arasındaki sayılar.)	
	long:Büyük sayıları saklamak için kullanılır.(8byte, -9,223,372,036,854,775,808 -- 9,223,372,036,854,775,807 )
	float:Ondalıklı sayılarla işlem yaparken kullanılır. float değeri belirtmek için sonuna f eklenir. (4 byte örnek 3.14 7 basamağa kadar.)
	double:Çift hasasiyetli ondalıklı sayılar. (8byte , 3.14123456789015 15basamağa kadar.)

	char:Tek bir karakteri tutar. (2byte 16bit)
	boolean:Mantıksal değerleri temsil eder. İki değeri olabilir.  true veya false.


/* 

Veri Tipi	Boyut (bit)	Değer Aralığı	Örnek
byte	8	-128 ile 127	byte b = 100;
short	16	-32,768 ile 32,767	short s = 32000;
int	32	-2,147,483,648 ile 2,147,483,647	int i = 100000;
long	64	-9,223,372,036,854,775,808 ile 9,223,372,036,854,775,807	long l = 10000000000L;
float	32	±3.40282347 × 10^38 (7 basamağa kadar hassasiyet)	float f = 3.14f;
double	64	±1.79769313486231570 × 10^308 (15 basamağa kadar hassasiyet)	double d = 3.14159265359;
char	16	0 ile 65,535 arasındaki Unicode karakterleri	char c = 'A';
boolean	1	true veya false	boolean isActive = true;

*/


*/
   c.Operatörler
 .Aritmetik Operatörler
+ Toplama , - Çıkarma , * Çarpma , / Bölme , % Bölümünden kalan

 .Karşılaştırma (İlişkisel Operatörler)
İki değeri karşılaştırır ve bir boolean sonucu döndürür.
== Eşittir , != Eşit değil , > Büyüktür , < Küçüktür , >= Büyük veya eşittir , <= Küçük veya eşittir.

 .Mantıksal Operatörler
Boolean değerlerle işlem yapar.
&& Ve , || Veya , ! Değil

 .Atama Operatörleri
Değişkenleri değişkenlere atmak için kullanılır.
= Basit Atama , += Aartı Atama , -= Eksi Atama , *= Çarpma Atama , /= Bölme Atama , %= Kalanından atama

 .Artırma ve Azaltma Operatörleri
++ Artırma , -- Azaltma

  ç.Koşullar
Programın akışını belirlemek için kullanılır. Belirli bir durumun doğru olup olmadığını kontrol eder ve durumlara göre farklı kod bloklarını çalıştırır.
 
 İf koşulu = Örnek RESİM
	if(koşul)
	 {
	   Koşul sağlanıyor ise if bloğu içerisindeki kod çalışacaktır.
	 }
 if-else -> koşul sağlanmadığı durumlarda else bloğu çalışır.
         if(koşul)
	  {
	  }
	else
	   {
	     Koşul sağlanmadığı durumlarda else bloğu çalışır.
	   }
if-else-else if -> ilk koşul sağlanmaz ise diğer koşullar sırasıyla kontrol edilir.

  Switch Koşulu
Farklı olasılıklara göre farklı kod bloklarını çalıştırmak için kullanılır.
  switch(değişken){
	case value1:
	 break;
	case value2:
	 break:
	default:Değerler ile eşleşmez ise  kod bloğu çalışacaktır.


   d.Döngüler
Bir işlemi birden fazla tekrar etmek için kullanılır. Belirli bir koşul sağlandığı sürece çalışmaya devam edip işlem bitene kadar çalışır.

 	For Döngüsü: Başlangıç , koşul , artış veya azalış ifadeleri belirtilerek belirli bir sayıda tekrar yapmak için kullanılır.
		for(başlangıç; koşul; artış/azalış;)
			{
				Her defasında çalıştırılacak (yazdırılacak) olan kod bloğu.
			}

Başlangıç: Değişkenin ilk değerini belirler.
Koşul: Her adımda kontrol edilir , koşul sağlandıı sürece döngü devam eder.
Artış/ Azalış :  Koşul sağlandığı sürece artırma/azaltma işlemi gerçekleşir.

	While Döngüsü
Koşul doğru ollduğu sürece çalışır , döngü başlamadan koşul kontrol edilir.
	while(koşul)
	{
	 System.out.println(); koşul doğru ise çalışır.
	 a++;
        }

	Do- While Döngüsü
İlk önce kod bloğu çalıştırır sonra koşulu kontrol eder. En az bir kere döngü çalışır , koşul döngü sonunda kontrol edilir.

	do{  System.out.println();
	}
	while(koşul);

	int a=2;
	do{
	  System.out.println(a);
	  a++;
	}
	while(a<=10);

Döngüde break ve Continue Kullanımı
 break; Döngüyü hemen sonlandırır.
 continue: Döngünün o anki tekrarlama işlemini sonlandırı bir sonrakine geçer.

    for(int a=1; a<=5; a++)					
	{
	  if(a == 4 ){
	break; // 4 olduğunda döngü sonlanır.	
	}
	System.out.println(a);
	}

     for(int a=1; a<=5; a++)					
	{
	  if(a == 4 ){
	continue; // 4 olduğunda atlayıp döngüye devam eder.	
	}
       System.out.println(a);
	}

Fonksiyonlar
3.Fonksiyonlar (Metodlar)

Fonksiyon Nedir:

Belirli bir görevi yerine getirmek için tanımlanmış ifade bloklarıdır.


Neden Kullanırız?
Programın anlaşılabilirliğini , hata takibini ve program içerisinde kod takibini kolaylaştırmak için programın fonksiyonlara(metotlara) ayrılması(küçük programcıklar
haline getirilmesi) işimizi kolaylaştırır.

***Genel
Bir defa oluşturulur birden fazla kez çağrılabilir.
Genellikle çağıran programdan aldıkları girdileri verileri işleyerek sonuçları yine çağıran programa geri göndeririz.
Metot girdilerine parametre veya argüman adı verilir.
Bir metot geriye (çağrıldığı yere) bir değer dönmüyorsa "void" tipindedir.***
Geriye değer döndürecek metotlarda ise "return" ifadesi kullanırız.
..Metot veri tipi ile return veri tipi kesinlikle aynı olmalıdır.//Tür uyumsuzluğu şeklinde uyarı dönmektedir. 


Kod içerisinde tekrar tekrar kullandığımız kod parçaçıklarını fonskiyon olarak tanımlarız bu şekilde tekrar eden kod yazmak durumunda kalmayız.

Günlük yaşamımızdan örnek verecek olursak : Çamaşır Makinesi kullanım amacı.

Bir fonksiyon bir ve birden fazla parametre alabilir  ama sadece bir tip "int,string,double..." dönebilir.

Rekursif Fonsksiyonlar?

4.Data Structures
Veri Yapıları (Data Structures)
Verileri düzenlemek , saklamak sonrasında üzerinden işlem yapmak için kullanılırız.
Veri yapılarını doğru bir şekilde kullanarak  işlemleri daha hızlı ve az bellek  kullanarak gerçekleştirebiliriz.

//Array (Dizi)//

Sabit Boyutlu bir veri yapısıdır. Veriler sırayla saklanır.
int[] sayi = {1,2,3};

//ArrayList (Dinamik Dizi)//
ArrayList, Java'da dinamik bir dizi gibi çalışan bir veri yapısıdır. Eleman sayısına göre boyutu otomatik olarak ayarlanır.
Veri ekleme, çıkarma ve güncelleme işlemlerini kolaylaştırır.
Elemanlar eklenme sırasına göre saklanır ve erişilir.
Elemanlara dizilerde olduğu gibi indeks numarasıyla erişilir. İlk eleman 0. indeksdedir.
Sadece String, Integer gibi nesne tiplerini saklar. Temel veri tipleri (örneğin, int, double) autoboxing ile nesneye çevrilir.
java.util paketinde yer alır ve List arayüzünü uygular.
Verilerin dinamik yapıda saklanması gerektiğinde kullanırız.

Tanımlama Örneği:
ArrayList<Tip> isim = new ArrayList<>();
add(eleman) → Listeye eleman ekler.				names.add("Tuana");
add(index, eleman) → Belirtilen indekse eleman ekler.		names.add(1);    	
remove(index) → Belirtilen indeksteki elemanı çıkarır.       	names.remove(1);   
remove(eleman) → Belirtilen değeri taşıyan elemanı çıkarır.     names.remove("Tuana");
get(index) → Belirtilen indeksteki elemanı döner.   		String names= names(0);
contains(eleman) → Elemanın listede olup olmadığını kontrol eder. 
if (isimler.contains("Ayşe")) {
    System.out.println("Ayşe listede!");
}       
indexOf(eleman) → Elemanın indeksini döner, yoksa -1 döner.

	Metot				Açıklama
add(E eleman)			ArrayList'e eleman ekler.
add(int index, E eleman)	Belirtilen indekse eleman ekler.
remove(int index)		Belirtilen indeksteki elemanı siler.
get(int index)			Belirtilen indeksteki elemanı döner.
set(int index, E eleman)	Belirtilen indeksteki elemanı değiştirir.
size()				ArrayList'in boyutunu döner.
isEmpty()			ArrayList boşsa true, aksi halde false döner.
contains(Object o)		Belirtilen elemanın listede olup olmadığını kontrol eder.
clear()				Tüm elemanları siler.
indexOf(Object o)		Belirtilen elemanın ilk indeksini döner.

/*Örnek

ArrayList <String> names =  new ArrayList<>(); //Arraylist Tanımlamam
names.add("Ozan"); 
names.add("Tuana"); //Eleman Ekleme
names.add("Kaan");

names.remove(1); //1.indekse göre eleman çıkarma. //Tuana çıkarılır. 
names.remove("Tuana"); //Değere göre eleman çıkarma.
names.clear();//Dizine ait tüm elemanları  kaldırıp , boş bir listeye döndürür.


System.out.println(names);//Arraylist'i yazdırma
*/

//LinkedList (Bağlı Liste)//
Veri elemanları, bellekte ardışık şekilde değil, birbirine bağlı düğümler (nodes) olarak saklanır. Her düğüm;
Bir veri (data) içerir. Bir sonraki düğüme (veya önceki düğüme, çift yönlü bağlı listelerde) bağlantı içerir.
Liste başına, sonuna veya ortasına hızlıca eleman eklenebilir veya çıkarılabilir.
Dizi Tabanlı Değildir: Veriler bellekte ardışık olarak değil, düğümler üzerinden saklanır.
Çift Yönlü Bağlantı: Java'da LinkedList, çift yönlü bağlı liste (doubly linked list) olarak uygulanır. Her düğüm hem önceki hem de sonraki düğümü işaret eder.
List ve Deque Arayüzlerini Uygular: Bu sayede hem liste hem de kuyruk (queue) gibi kullanılabilir.

LinkedList kullanımı için java.util.LinkedList sınıfını import etmeniz gerekir.

Tanımlama Örneği:

 LinkedList<String> meyveler = new LinkedList<>();
	
Örnek.1.1
   LinkedList<String> hayvanlar = new LinkedList<>();

        // Listeye eleman ekleme
        hayvanlar.add("Kedi"); // Sona ekler
        hayvanlar.addFirst("Köpek"); // Başa ekler
        hayvanlar.addLast("Tavşan"); // Sona ekler
        hayvanlar.add(1, "Aslan"); // 1. indekse ekler

        System.out.println("Hayvanlar: " + hayvanlar);

  Metot			    Açıklama
add(E e)		Sona eleman ekler.
addFirst(E e)		Başa eleman ekler.
addLast(E e)		Sona eleman ekler.
remove()		İlk elemanı çıkarır.
remove(int index)	Belirtilen indeksteki elemanı çıkarır.
removeFirst()		İlk elemanı çıkarır.
removeLast()		Son elemanı çıkarır.
get(int index)		Belirtilen indeksteki elemanı döner.
getFirst()		İlk elemanı döner.
getLast()		Son elemanı döner.
size()			Listedeki eleman sayısını döner.
clear()			Tüm elemanları siler.
contains(Object o)	Elemanın listede olup olmadığını kontrol eder.
indexOf(Object o)	Elemanın ilk indeksini döner.

Sık sık ekleme ve çıkarma işlemleri yapmamız gerekiyorsa.
Veri boyutunun başlangıçta bilinmediği durumlarda.
Liste ortasında veri ekleme/çıkarma gerektiğinde (LinkedList bu işlemlerde daha verimlidir).

//Stack (Yığın)//
Stack (Yığın), bir veri yapısıdır ve veriler son giren ilk çıkar (LIFO - Last In, First Out) mantığıyla çalışır.
Yani, yığına eklenen en son eleman, ilk çıkarılır. Bu yapı, bir dizi görev veya işlemi geriye doğru çözmek gerektiğinde kullanışlıdır. 
Örneğin:
Fonksiyon çağrıları,
Geri alma işlemleri (örneğin, tarayıcıdaki geri tuşu),
Parantez dengeleme veya ifadelerin değerlendirilmesi.

Temel İşlemleri
Push: Yığına bir eleman ekler.
Pop: Yığının en üstündeki elemanı çıkarır ve döner.
Peek: Yığının en üstündeki elemanı döner, ancak çıkarmaz.
isEmpty: Yığının boş olup olmadığını kontrol eder.


 Metot			 Açıklama
push(E eleman)		Yığına eleman ekler.
pop()			Yığının en üstündeki elemanı çıkarır ve döner.
peek()			Yığının en üstündeki elemanı döner ancak çıkarmaz.
isEmpty()		Yığının boş olup olmadığını kontrol eder.
search(Object o)	Belirtilen elemanın yığındaki pozisyonunu döner. Bulunamazsa -1.
size()			Yığındaki eleman sayısını döner.


//Queue (Kuyruk)//
Queue (Kuyruk), bir veri yapısıdır ve ilk giren ilk çıkar (FIFO - First In, First Out) prensibiyle çalışır. 
Yani, kuyruğa ilk eklenen eleman, ilk çıkarılır. Günlük hayatta sıraya girme gibi durumlar bu prensibe uygundur.

 Temel Özellikleri
FIFO Mantığı: İlk eklenen eleman ilk çıkar.
Dinamik Veri Yapısı: Boyutu dinamik olarak artar veya azalır.
Kuyruk Operasyonları:
Enqueue (offer): Kuyruğun sonuna eleman ekler.
Dequeue (poll): Kuyruğun başındaki elemanı çıkarır ve döner.
Peek: Kuyruğun başındaki elemanı döner ancak çıkarmaz.


 Metot				Açıklama
add(E e)	Kuyruğun sonuna eleman ekler. Eğer kuyruk doluysa, bir hata fırlatır.
offer(E e)	Kuyruğun sonuna eleman ekler. Kuyruk doluysa false döner.
poll()		Kuyruğun başındaki elemanı çıkarır ve döner. Kuyruk boşsa null döner.
remove()	Kuyruğun başındaki elemanı çıkarır. Kuyruk boşsa hata fırlatır.
peek()		Kuyruğun başındaki elemanı döner ama çıkarmaz. Kuyruk boşsa null.
element()	Kuyruğun başındaki elemanı döner ama çıkarmaz. Kuyruk boşsa hata fırlatır.
isEmpty()	Kuyruğun boş olup olmadığını kontrol eder.
size()		Kuyruktaki eleman sayısını döner.

Genişlik Öncelikli Arama (BFS): Graf veya ağaç yapılarında arama yapmak için.
İş Kuyruğu: İşlemleri sırayla gerçekleştirmek için.
Veri İletişimi: Mesajlaşma sistemlerinde (örneğin, mesaj kuyruğu).

//HashMap (Anahtar-Değer Çifti)//
HashMap, Java'da anahtar-değer çiftleri ile çalışan bir veri yapısıdır. Veri saklamak ve erişmek için anahtarları kullanır. Bu yapı, verilerin hızlı bir şekilde depolanması ve alınması gereken durumlarda kullanışlıdır.

HashMap'in Temel Özellikleri:

Anahtarlar Benzersizdir: Aynı anahtar tekrar eklenemez.
Değerler Tekrar Edebilir: Aynı değer birden fazla anahtarla eşleştirilebilir.
Hızlı Erişim: Anahtarlar, bir hashing algoritması ile hızlıca eşleştirilir.
Sıralama Yoktur: HashMap, ekleme sırasını garanti etmez.
null Anahtar ve Değer: Bir null anahtar ve birden fazla null değer saklanabilir.

Kullanım Senaryoları
Kullanıcı bilgilerini ID ile eşleştirmek,
Çeşitli sayımlar (örneğin, kelime sayımı),
Sözlük uygulamaları (kelime-çeviri eşleştirmesi).

   HashMap<Integer, String> ogrenciler = new HashMap<>();

        // Öğrenci bilgilerini ekleme
        ogrenciler.put(101, "Ahmet");
        ogrenciler.put(102, "Mehmet");
        ogrenciler.put(103, "Ayşe");

        // Belirli bir öğrencinin adını bulma
        System.out.println("102 numaralı öğrenci: " + ogrenciler.get(102));

        // Tüm öğrencileri yazdırma
        System.out.println("Öğrenciler: " + ogrenciler);


Sıralama Yok: HashMap sıralı bir yapı değildir. Elemanlar ekleme sırasına göre saklanmaz.
Eğer sıralama gerekliyse LinkedHashMap veya TreeMap kullanılabilir.
Veritabanı uygulamalarında veri eşleştirme,
Anahtar-değer tabanlı önbellekleme,
Sözlük uygulamaları (kelime-çeviri eşleştirmesi).


5.Nesne Yönelimli Programlama (OOP)

6. Algoritmalar 
Konular ile ilgili yapılan örneklerimi atacağım link  belirtilecek.
Tüm öğrendiklerimi gösterebileceğim küçük bir proje?





