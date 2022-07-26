# PatikaSQL12
PatikaSQL ÖDEV12

SELECT COUNT(*) FROM film
WHERE length > ALL
(SELECT AVG(length) FROM film)

SELECT COUNT(*) FROM film
WHERE rental_rate = ALL
(SELECT MAX(rental_rate) FROM film

SELECT title FROM film
WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) 
OR replacement_cost = (SELECT MIN(replacement_cost) FROM film)

SELECT first_name, last_name, payment.customer_id, COUNT(*) FROM customer
JOIN payment ON customer.customer_id = payment.customer_id
GROUP BY customer.first_name, customer.last_name, payment.customer_id
ORDER BY COUNT DESC

https://app.patika.dev/furkanhaykirer
