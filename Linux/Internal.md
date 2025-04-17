![image](https://github.com/user-attachments/assets/7b266bcb-574c-44cf-b79a-156ead305056)
![image](https://github.com/user-attachments/assets/105078f9-9709-4f54-bd69-706646f4f2e7)
![image](https://github.com/user-attachments/assets/8b1e49b9-f1df-46e2-87ca-5af58ea77cde)
![image](https://github.com/user-attachments/assets/7a4b060e-b327-49af-842b-9c09265d9ac7)
![image](https://github.com/user-attachments/assets/fa3a900f-b644-4b37-ac32-b108d40755f7)
![image](https://github.com/user-attachments/assets/0365731c-cfcb-4503-af37-e8ca44624ed5)
![image](https://github.com/user-attachments/assets/4db58e87-8e42-43d0-a2f8-109964fcf333)
![image](https://github.com/user-attachments/assets/063230cf-757a-40dc-8f1d-6660b4af094c)
![image](https://github.com/user-attachments/assets/4dd587e0-31cf-4a77-a0ab-4f24c8226512)

Above, enumerate against /wordpress/. Below, enumerate against /blog/, get user admin.

![image](https://github.com/user-attachments/assets/627fd3cd-099c-4231-87d1-8c102f62011f)
![image](https://github.com/user-attachments/assets/abf82a4f-8de1-4766-9ef4-c1ca331d8337)
![image](https://github.com/user-attachments/assets/bcbdbc8c-7485-4784-b317-1428d90538e3)
![image](https://github.com/user-attachments/assets/335819c0-9cca-4376-8cc7-e3f1de5fbd1e)
![image](https://github.com/user-attachments/assets/f63cb7da-30bd-4a3d-8304-5e0cbacaa203)
![image](https://github.com/user-attachments/assets/debb016b-0a9b-4443-afbb-72a9462db6d9)
![image](https://github.com/user-attachments/assets/b099310f-a574-42dc-abe0-118105748a5c)

Visit /blog/, click on "Log in" --> redirect to internal.thm/blog/wp-login.php

![image](https://github.com/user-attachments/assets/f21fe702-bc4a-4da6-9463-0382a2076df2)
![image](https://github.com/user-attachments/assets/660392bd-fad3-49df-a348-901c21c4d968)
![image](https://github.com/user-attachments/assets/bdf24487-db1f-4473-a6fd-a999a1a61ee4)
![image](https://github.com/user-attachments/assets/71eb0b8f-a9ac-4a4c-ae1d-2bbae715f6e8)
![image](https://github.com/user-attachments/assets/75ea3c6c-ba3b-4638-8bee-3c87d39df67c)
![image](https://github.com/user-attachments/assets/cd2f747b-051e-4adc-bfce-934028f9be45)


Brute force password against user admin. Login, get reverse shell.

![image](https://github.com/user-attachments/assets/f30cf008-a5dc-4d0d-8059-a824950eeb2f)
![image](https://github.com/user-attachments/assets/ca823bed-1014-4717-afb5-b9b1e775c66b)
![image](https://github.com/user-attachments/assets/bb3bd9a8-ef7c-40f7-96d3-0c539ece0eab)
![image](https://github.com/user-attachments/assets/417d02ae-8464-4e38-9435-6223ca0ae465)
![image](https://github.com/user-attachments/assets/20cd0ab1-2baf-44e7-a2b1-f7817bdc0a0e)
![image](https://github.com/user-attachments/assets/8b7b910e-0c26-4985-a497-d3cf1d5b727b)
![image](https://github.com/user-attachments/assets/9018c9c2-92f1-4459-8bc6-01a9b61a71cd)
![image](https://github.com/user-attachments/assets/8a81d886-35e3-400f-a88a-efd5c7c54203)
![image](https://github.com/user-attachments/assets/50c2dd77-7692-4c17-a27f-61e50f559122)
![image](https://github.com/user-attachments/assets/2d514fe5-f4eb-4f10-b886-a756f10218a7)
![image](https://github.com/user-attachments/assets/24558e2f-dfb0-40f2-870b-ee992d1fb879)


Linpeas not find much useful info. Back to / and look around. Find credential.

![image](https://github.com/user-attachments/assets/3f1f30dc-8506-4c54-8dfd-fd721d583aff)
![image](https://github.com/user-attachments/assets/a42ab000-e796-4a1c-a02f-57f7b7abab9e)

Aubreanna in adm group, read /var/log, no password.

![image](https://github.com/user-attachments/assets/58945426-e8ad-4d83-9622-49f486b735ac)

Check home directory jenkins.txt again. SSH local port forwarding.

![image](https://github.com/user-attachments/assets/1a53ddb8-0078-44ef-9da4-5935835082a4)
![image](https://github.com/user-attachments/assets/4fde5818-6a85-4e5c-a284-b08616000f72)
![image](https://github.com/user-attachments/assets/d8a75d36-a913-4f5d-8c8f-fdb049fd4df8)
![image](https://github.com/user-attachments/assets/b0aaa340-b56b-44eb-9447-8020f71d560e)
![image](https://github.com/user-attachments/assets/6471752b-1616-4f96-84f1-e78c534ded9f)

Take a break. Restart machine. Newly assigned IP.

SSH local port forward to 8000. User admin. ZAP to brute force passwd --> rockyou.txt

Get Jenkins login passwd. 

![image](https://github.com/user-attachments/assets/cdd24acd-8735-4568-a54a-2b0bfba8a5b0)
![image](https://github.com/user-attachments/assets/d65f53d0-d12e-4e1c-9a44-a339fed234df)

Jenkins -> Manage Jenkins -> Script Console -> Groovy code -> Run -> Get reverse shell

![image](https://github.com/user-attachments/assets/d0102154-5e31-4980-858b-9472d5077727)
![image](https://github.com/user-attachments/assets/bb8c7498-e48c-4d4e-9e28-8fedeb9bf6c4)
![image](https://github.com/user-attachments/assets/2a6778da-653f-4e33-8ca2-c891014a2fda)
![image](https://github.com/user-attachments/assets/310d23c5-d44e-4047-b3e6-31a9258e7b9f)
![image](https://github.com/user-attachments/assets/9f80dd3f-f5fe-4318-97bf-728efd6321b0)




