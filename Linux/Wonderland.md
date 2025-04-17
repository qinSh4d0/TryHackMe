![image](https://github.com/user-attachments/assets/5584749e-7b6c-4062-9f2a-34280ce00da9)
![image](https://github.com/user-attachments/assets/55ba8ae7-93fe-4a9f-9f6b-c5be303c9b06)
![image](https://github.com/user-attachments/assets/23b6b098-f563-4be0-8cbe-e753fa027818)
![image](https://github.com/user-attachments/assets/3c56addc-321f-46df-9ced-bf5aa65973b6)
![image](https://github.com/user-attachments/assets/bf7373cc-392d-446d-b5e6-e02154ddc278)
![image](https://github.com/user-attachments/assets/bc4edf20-4ad6-43fe-9de4-c7e4bcd16e0a)
![image](https://github.com/user-attachments/assets/5f729f02-9769-48c4-a68c-a5737a3acdde)
![image](https://github.com/user-attachments/assets/4309cfb7-28a5-47ba-8bef-c373ed109b99)
![image](https://github.com/user-attachments/assets/a8474f0b-2fcd-46a1-9728-00edc3f02853)
![image](https://github.com/user-attachments/assets/a70f3699-e25b-4a20-8111-cbf7c3103a56)
![image](https://github.com/user-attachments/assets/65126d24-3281-4f6b-94b3-7e7c3563bcde)
![image](https://github.com/user-attachments/assets/e0dc65a6-941b-4410-9ea1-43f71ebe6b83)
![image](https://github.com/user-attachments/assets/7828b2cd-a348-478c-9a2e-5f421f76b0e1)
![image](https://github.com/user-attachments/assets/c6d0a66f-ca13-4eb4-be21-5fbf19a3dfb4)
![image](https://github.com/user-attachments/assets/b1e6e2ad-4d36-4002-9eee-9d44055f23d9)
![image](https://github.com/user-attachments/assets/e255cda3-189f-45bf-b49e-6cbb943431a0)
![image](https://github.com/user-attachments/assets/1eda11fe-dd4b-4171-9681-7b3bc30e2781)
![image](https://github.com/user-attachments/assets/d7490710-c380-4745-93a0-5a64692553a5)
![image](https://github.com/user-attachments/assets/11f271bf-c855-4407-a51c-966b4475fbc3)
![image](https://github.com/user-attachments/assets/bca4bb2c-58b9-4eae-9984-2491a50fed97)
![image](https://github.com/user-attachments/assets/27ad1e54-ee36-491f-bc38-8382243ef9bb)
![image](https://github.com/user-attachments/assets/53792659-f048-46fb-9d31-da5bea8a3f83)
![image](https://github.com/user-attachments/assets/5ad874da-f0fd-4aaf-9753-8f436bd9af0f)
![image](https://github.com/user-attachments/assets/30c2c399-2c23-4a47-8db2-084e3f5958d8)
![image](https://github.com/user-attachments/assets/4b22a73a-74d9-45cb-9a56-68f18a852d26)
![image](https://github.com/user-attachments/assets/185197b8-8cf6-4c9b-8787-cf4122d7a2b7)
![image](https://github.com/user-attachments/assets/9d78619d-64f5-421a-8e62-16ec7aafb65a)
![image](https://github.com/user-attachments/assets/81386fe7-d7fe-43b6-80f9-f90d07d4c6b3)

1. teaParty binary has SUID set, in "rabbit" home directory.
   
2. no "rabbit" SSH password, change whole directory to 777 for all users.

3. trasfer teaParty to Kali, strings, binary runs "/bin/echo" and "date" but no absolute path for "date".

4. create "date" bash script that execute /bin/bash, make "date" executable, and export $PATH (export PATH=/home/rabbit:$PATH).

5. run teaParty, escalate to Hatter.

6. Hatter not full environment, no permission to run Capabilities command. With Hatter's passwd, su - Hatter.
