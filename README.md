# PostgreSQL

## SQL (Structured Query Language) Nedir ? 
SQL (Structured Query Language), Türkçe adıyla yapılandırılmış sorgu dili, veritabanlarıyla etkileşim kurmak için kullanılan standart bir programlama dilidir. SQL (Structured Query Language) bir deklaratif programlama dili olarak bilinir. Deklaratif Programlama yaklaşımında  programcı, yapılacak işlemi tanımlar, ancak bu işlemin nasıl gerçekleştirileceğini (adım adım prosedürleri) belirtmez. Sistem, belirlenen amaca ulaşmak için gerekli olan adımları kendi kendine belirler ve uygular. Bu, kodun daha okunabilir ve anlaşılır olmasını sağlar.  SQL, bu yaklaşımla veritabanları üzerinde veri sorgulama, ekleme, güncelleme ve silme işlemlerini gerçekleştirir. 

## Veritabanı (Database) Nedir ?
Verilerin organize bir şekilde depolandığı yerdir. Örneğin, bir müşteri bilgilerini, ürün envanterini veya satış kayıtlarını saklayan dijital bir dosya gibidir.

## Veritabanı Yönetim Sistemi (Database Management System - DBMS)
Veritabanlarını oluşturmak, yönetmek ve veriler üzerinde işlem yapmak için kullanılan yazılımdır. Örneğin, MySQL, PostgreSQL, Oracle Database gibi yazılımlar birer DBMS'dir. Bu sistemler, veritabanı üzerinde veri ekleme, silme, güncelleme ve sorgulama gibi işlemleri yapmamızı sağlar.

## Veritabanı - Veritabanı Yönetim Sistemi Farkı 
- Veritabanı, verilerin kendisidir.
- Veritabanı Yönetim Sistemi, bu verilerle çalışmamızı sağlayan yazılımdır.

![image info](/images/dbs.jpeg)
Yukarıdaki şekilde de gördüğümüz üzere farklı kaynaklardan gelen sorgular DBMS yazılımı sayesinde farklı veritabanlarında kullanılır.


## PostgreSQL Nedir ?
Yukarıda anlattığımız gibi PostgreSql bir veri tabanı yönetim sistemidir. Açık kaynaklı ilişkisel veri tabanı yönetim sistemidir. Kısacası PostgreSql veri tabanı yönetim sistemi içerisinde SQL kullanarak verilerimizi yönetiyoruz, düzenliyoruz, siliyoruz, güncelliyoruz vs...

İlişkisel veri tabanı dedik peki bu tam olarak nedir ?

### İlişkisel Veri Tabanı Nedir ?
İlişkisel veritabanı, verilerin tablolar içerisinde saklandığı veritabanıdır. Tablolar satırlar (rows) ve sütünlardan (columns) oluşur. Tablolar arasında ilişkiler olabilir, bu ilişkilerde ortak sütunlar diğer adıyla anahtar sütunlar ile kurulur. Bu şekilde veriler daha düzenli ve tutarlı şekilde kullanılabilir. 
### Örnek Senaryo 
Bir okulda öğrencilerin aldığı dersler için veritabanı oluşturalım. Bu veritabanında öğrenciler ve dersler hakkında bilgiler tutacağız. Ve bu iki tablo (öğrenciler ve dersler) arasında ilişki kuracağız. Çünkü her öğrenci bir veya daha fazla ders alabilir ve her ders bir veya daha fazla öğrenci içerebilir. 
![image info](/images/table_1.png)
Tablolarımızın bu şekilde oluştuğunu düşünelim. Daha sonra ilişkiyi kuracağımız üçüncü tabloyu oluşturalım. 
![image info](/images/table_2.png)
Öğrenci tablosundaki her bir öğrenci bu oluşturduğumuz 3.tablo ile dersler tablosuna bağlanmış olur. Bu oluşturduğumuz 3.tablo öğrenci id ve kurs id saklar. Öğrenciler ve Kurslar tablosu arasında bir ilişki kurar. Tabi PostgreSql'de tablolu oluştururken bazı anahtar kelimeleri kullanarak bunları yapıyoruz. Resim şeklinde anlatmaya çalışmamın sebebi , ilişkisel veri tabanı mantığını daha iyi anlamak.