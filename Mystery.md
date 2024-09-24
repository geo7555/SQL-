SELECT *
  FROM crime_scene_report where type='murder' and city='SQL City' and date=20180115

SELECT *
  FROM person where address_street_name='Northwestern Dr' or'Franklin Ave'

SELECT *
  FROM person where address_street_name='Northwestern Dr'ORDER BY address_number DESC limit 1

SELECT *
  FROM person where name like '%Annabel%' and address_street_name='Franklin Ave'

SELECT *
  FROM interview where person_id=14887

SELECT *
FROM interview where person_id=16371

SELECT *
FROM get_fit_now_member
where person_id=16371

SELECT *
FROM get_fit_now_check_in
where check_in_date=20180109 and membership_id like&#39 '%48Z%'

SELECT *
FROM get_fit_now_member
WHERE id = &#39;48Z7A&#39; OR id = '48Z55';

SELECT *
FROM drivers_license
where plate_number like '%H42W%'

SELECT *
FROM person
where license_id=423327 or license_id=664760

SELECT *
FROM person
WHERE (license_id=423327 OR license_id=664760) AND (id=67318 OR
id=28819);
