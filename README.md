### ����
- �ô洢�����`Wopi Host`��ʾ�����ٷ��ṩ��ʾ����Ŀ`SampleWopiHandler`��
- ֧��`DOCX`�༭���Լ�`PPTX`��`XLSX`
- ֧��Эͬ������Word��Excel�� PowerPoint��

### ע��
- ����������Ҫע����룬(δʵ��)
- ����`Wopi Host`��Ҫ **����Ա** 
- `Wopi Host`����������`Office Online 2016`��������Ҳ����������`Web`������

### ����
#### [2019-04-17]
- MVC�汾���ɲ���linux������������ Jexus��
- ���һ�� �ӿ� �ĵ�

#### [2019-04-04]
- ����Office Online Server�������һЩ���⣨ʵ��ͼƬ�ϴ����鿴��wordЭͬ��PPT���ã�

#### [2019-04-01]
-  ���¹ٷ��ṩ��ʾ���汾�� **IIS����** ����`SampleWopiHandler` �� **�Ƽ�ʹ��** 
- `WopiHost` ��Ŀ��ʼ��������������ʱ����ּ�����״̬������ԭ��֪
- ʵ�⣬�ٷ��ṩ��ʾ���汾  **��Ӧ�ٶȿ�**�� **�ȶ�** 
- <https://github.com/Microsoft/Office-Online-Test-Tools-and-Documentation>

----------

> ��װ�̳̣�https://docs.microsoft.com/zh-cn/officeonlineserver/deploy-office-online-server

> ��װ�����У���֤ **Windows Update** �������

> ͨ��Զ�̷��ʷ�������װʱ������ͨ����Դ������̵ķ�ʽֱ�����У�������ͨ�������̷��ķ�ʽ���У���`\\192.168.1.188\G$`

> Server2012 R2 ���ϣ�������Server2016Ϊ��

> ����`PowerShell`�������Ƿ�������Ĭ��Administrator�˺�Ϊ **����Ա** 

### ��һ������ɫ�ͷ���

Windows Server 2012 R2:
```
Add-WindowsFeature Web-Server,Web-Mgmt-Tools,Web-Mgmt-Console,Web-WebServer,Web-Common-Http,Web-Default-Doc,Web-Static-Content,Web-Performance,Web-Stat-Compression,Web-Dyn-Compression,Web-Security,Web-Filtering,Web-Windows-Auth,Web-App-Dev,Web-Net-Ext45,Web-Asp-Net45,Web-ISAPI-Ext,Web-ISAPI-Filter,Web-Includes,InkandHandwritingServices,NET-Framework-Features,NET-Framework-Core,NET-HTTP-Activation,NET-Non-HTTP-Activ,NET-WCF-HTTP-Activation45,Windows-Identity-Foundation,Server-Media-Foundation
```
Windows Server 2016��
```
Add-WindowsFeature Web-Server,Web-Mgmt-Tools,Web-Mgmt-Console,Web-WebServer,Web-Common-Http,Web-Default-Doc,Web-Static-Content,Web-Performance,Web-Stat-Compression,Web-Dyn-Compression,Web-Security,Web-Filtering,Web-Windows-Auth,Web-App-Dev,Web-Net-Ext45,Web-Asp-Net45,Web-ISAPI-Ext,Web-ISAPI-Filter,Web-Includes,NET-Framework-Features,NET-Framework-45-Features,NET-Framework-Core,NET-Framework-45-Core,NET-HTTP-Activation,NET-Non-HTTP-Activ,NET-WCF-HTTP-Activation45,Windows-Identity-Foundation,Server-Media-Foundation
```
### �ڶ�������������

 **.NET Framework 4.5.2** 

https://go.microsoft.com/fwlink/p/?LinkId=510096

 **Visual C++ Redistributable Packages for Visual Studio 2013** 

https://www.microsoft.com/download/details.aspx?id=40784

 **Visual C++ Redistributable for Visual Studio 2015** 

https://go.microsoft.com/fwlink/p/?LinkId=620071

 **Microsoft.IdentityModel.Extention.dll** 

https://go.microsoft.com/fwlink/p/?LinkId=620072

### ��������������
##### ��˵����
https://www.cnblogs.com/wanggege/p/4605678.html

��ӽ�ɫ�͹��ܣ�ѡ�� **Active Directory �����** ��װ���ȴ���ɣ���Ҫ�رգ�
��� **���˷���������Ϊ�������** ��ѡ�� **�������** ���������������  **`oos.com`**  ���Լ���㶨�壬�������룬��װ���Զ�����

### ���Ĳ�����װOffice Online Server
û�а������ڣ�MSDN�Ҹ����� ����
```
ed2k://|file|cn_office_online_server_last_updated_march_2017_x64_dvd_10245068.iso|730759168|DA70F58CB8FFAF37C02302F2501CE635|/
```

##### Office Online Serverע�����
https://docs.microsoft.com/zh-cn/officeonlineserver/plan-office-online-server

- ��Ҫ��װSQL Server�ȷ���������
- ��Ҫ�ڶ˿� 80��443 �� 809 �ϰ�װ���� Web ������ (IIS) ��ɫ���κη�����ɫ
- ��Ҫ��װ�κΰ汾�� Office
- ��Ҫ����������ϰ�װ Office Online Server
- �����֮��һ̨�ɾ��ķ�����

### ���岽����װ���԰�
http://go.microsoft.com/fwlink/p/?LinkId=798136

### ��������ټ���
<https://download.microsoft.com/download/6/B/D/6BD1D664-1212-4AB2-9BE8-447731F2CA0E/wacserver2016-kb4011025-fullfile-x64-glb.exe>

### ������������OfficeWebApps ģ��
```
Import-Module -Name OfficeWebApps
```

### ���߲�������Office Online Server��
```
New-OfficeWebAppsFarm -InternalURL "http://oos.com" -AllowHttp -EditingEnabled
```

### �ڰ˲�����֤Office Online Server��
http://oos.com/hosting/discovery	��ķ�ʽ���ʣ���Ҫ���ʵĿͻ��˼�����

http://localhost/hosting/discovery	���ط���

http://192.168.1.78/hosting/discovery	IP����	���������ܷ��ʣ�ȥ��IIS���Ѿ��Զ������վ��

### �ھŲ�������Wopi��Ŀ
https://github.com/netnr/WopiHost

https://gitee.com/netnr/WopiHost

�������񣬸���config.json���������

### ��ʮ����ʹ��
```
�༭word
http://192.168.1.78/we/WordEditorFrame.aspx?WOPISrc=http://192.168.1.188:78/wopi/files/word.docx&ui=zh-CN&access_token=123456
�鿴word
http://192.168.1.78/wv/wordviewerframe.aspx?WOPISrc=http://192.168.1.188:78/wopi/files/word.docx&ui=zh-CN&access_token=123456
�鿴excel
http://192.168.1.78/x/_layouts/xlviewerinternal.aspx?WOPISrc=http://192.168.1.188:78/wopi/files/excel.xlsx&ui=zh-CN&access_token=123456
�༭excel
http://192.168.1.78/x/_layouts/xlviewerinternal.aspx?edit=1&WOPISrc=http://192.168.1.188:78/wopi/files/excel.xlsx&ui=zh-CN&access_token=123456
�鿴ppt
http://192.168.1.78/p/PowerPointFrame.aspx?PowerPointView=ReadingView&WOPISrc=http://192.168.1.188:78/wopi/files/ppt.pptx&ui=zh-CN&access_token=123456
�༭ppt
http://192.168.1.78/p/PowerPointFrame.aspx?PowerPointView=EditView&WOPISrc=http://192.168.1.188:78/wopi/files/ppt.pptx&ui=zh-CN&access_token=123456
```
- office�����ַ������IP��Ҳ���Ǵ���Office Online Server��ָ���� **InternalURL**  ��`http://oos.com`
- `192.168.1.78` �� office�����IP��ַ��`192.168.1.188` �� wopi������ñ�֤office�������ܷ���wopi����ĵ�ַ
- token������������Ȩ��֤����Ҫwopi��������ʵ��
- WOPISrc������Ҫ����`UserId`��`UserName`,��ʾ��ǰ���û���Эͬ��������Ҫurl����
    - ʾ����`http://192.168.1.188:78/wopi/files/word.docx?UserId=1&UserName=1`
    - ���룺`http%3A%2F%2F192.168.1.188%3A78%2Fwopi%2Ffiles%2Fword.docx%3FUserId%3D1%26UserName%3D1`

### ����
- `Get-OfficeWebAppsFarm` ���ص�ǰ������������ OfficeWebAppsFarm �������ϸ��Ϣ
- `New-OfficeWebAppsFarm` �ڱ��ؼ�����ϴ����� Office Online Server ��
- `Set-OfficeWebAppsFarm` �������� Office Online Server ��������
- `Remove-OfficeWebAppsMachine` �� Office Online Server ����ɾ�����з�������ɾ��Farm��
- �������<https://docs.microsoft.com/zh-cn/officeonlineserver/windows-powershell-for-office-online-server/windows-powershell-for-office-online-server>

### ��ͼ

Word��ͼ

![word](https://netnr.gitee.io/gs/2018/11/13/593bab5043.png)

Excel��ͼ

![excel](https://netnr.gitee.io/gs/2018/11/13/852ec9c947.png)