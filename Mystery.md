SELECT *
  FROM crime_scene_report where type='murder' and city='SQL City' and date=20180115
![image](https://github.com/user-attachments/assets/1fa641a7-61f1-40cb-97ed-1ceba831f7f4)

SELECT *
  FROM person where address_street_name='Northwestern Dr' or'Franklin Ave'
![image](https://github.com/user-attachments/assets/06fc5f6e-b438-402a-91cb-046c38d22f2f)

SELECT *
  FROM person where address_street_name='Northwestern Dr'ORDER BY address_number DESC limit 1
![image](https://github.com/user-attachments/assets/59467432-6f18-4de1-95ac-6c4ee9ffa3e9)

SELECT *
  FROM person where name like '%Annabel%' and address_street_name='Franklin Ave'
![image](https://github.com/user-attachments/assets/26c5645b-af03-4199-8096-7badf8fe0b37)

SELECT *
  FROM interview where person_id=14887
![image](https://github.com/user-attachments/assets/2b910149-3e86-479b-90fb-d8089149bd66)

SELECT *
FROM interview where person_id=16371
![image](https://github.com/user-attachments/assets/a0eadab0-bcd6-4fe9-b13c-bbef19e3786f)

SELECT *
FROM get_fit_now_member
where person_id=16371
![image](https://github.com/user-attachments/assets/6979c65f-f990-45a6-b1cd-d059b826d653)

SELECT *
FROM get_fit_now_check_in
where check_in_date=20180109 and membership_id like&#39 '%48Z%'
![image](https://github.com/user-attachments/assets/3911bd41-20ae-4c1d-9e8d-bb9c9c09e7b0)

SELECT *
FROM get_fit_now_member
WHERE id = '48Z7A' OR id = '48Z55';
![image](https://github.com/user-attachments/assets/f501c588-3b53-470b-9a6f-17f0189f4667)

SELECT *
FROM drivers_license
where plate_number like '%H42W%'
![image](https://github.com/user-attachments/assets/d3f4f43e-5677-40a3-8b1c-4e721bb3c6b7)

SELECT *
FROM person
where license_id=423327 or license_id=664760
![image](https://github.com/user-attachments/assets/29eef62c-92df-4eb9-aaff-47debd8f5c3e)

SELECT *
FROM person
WHERE (license_id=423327 OR license_id=664760) AND (id=67318 OR
id=28819);
![image](https://github.com/user-attachments/assets/377d7f4f-d855-4d1e-bc62-9c04c52a4ae3)

INSERT INTO solution VALUES (1, 'Jeremy Bowers');
SELECT value FROM solution;
![image](https://github.com/user-attachments/assets/14477d63-0d78-40aa-b756-0b77a80ad42f)
