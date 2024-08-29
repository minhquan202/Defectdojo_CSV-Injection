**Description:**


CSV Injection on the lis api:
- `/engagement/{id}/edit` -> param: name
- `/product/{id}/new_engagement` -> param: name
- `/product/{id}/ad_hoc_finding` -> param: name
- `/finding/{id}/edit` -> param: title
- `/finding/{id}/edit` -> param: component_name 
- `/product/type/add` -> param: name
- `/product/type/{id}/edit` -> param: name

  
of Defectdojo version 2.37.3 ([https://github.com/DefectDojo/django-DefectDojo](https://github.com/DefectDojo/django-DefectDojo)) allow remote attackers to insert malicious code. When user execute export product with type csv. When executed open file immediately malicious code is executed.

**Proof of Concept:**
1. Add or edit the above API list with malicious script tags at Param malicious.
2. Export type csv corresponding to the api
3. Open the csv file that was just downloaded. The malicious code is immediately executed.




![image](https://github.com/user-attachments/assets/ecd30011-443d-416f-8b6c-ace9574eb449)
![image](https://github.com/user-attachments/assets/de133008-3be5-4c9b-a6e9-a5de03813c2d)
![image](https://github.com/user-attachments/assets/6a152028-160c-41a5-be88-71c1b993506f)
![image](https://github.com/user-attachments/assets/fd9581b2-2f63-4a33-a408-3a4f4b7ffd94)



**Impact:**


Execution of Malicious Code
