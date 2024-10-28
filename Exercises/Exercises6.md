### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

## film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.

``` sql
SELECT rating, COUNT(*)
FROM film
GROUP BY rating

```

## film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
``` sql
SELECT replacement_cost, COUNT(*) AS film_sayisi
FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY film_sayisi DESC;

```

## customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir? 
``` sql
SELECT store_id, COUNT(*) AS musteri_sayisi
FROM customer
GROUP BY store_id;
```

##  city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.

``` sql
SELECT country_id, COUNT(*) AS sehir_sayisi
FROM city
GROUP BY country_id
ORDER BY sehir_sayisi DESC
LIMIT 1

```

