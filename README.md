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

4.Nesne Yönelimli Programlama (OOP)

5. Veri Yapıları ve Algoritmalar




