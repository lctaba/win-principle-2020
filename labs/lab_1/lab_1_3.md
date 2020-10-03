# How to package an application


***

�ڽ��и�ʵ��֮ǰ�������ѡ���Ƚ���2����ʵ�飺
1. ѧ��鿴֤�飨�μ� [How to View certificates](../../appendix/MSIX/viewCertificates.md)��
2. ����֤�飨���Ҳ�����������������ҵ���

����������ʵ�������ڶ�Ӧ�ó�����д���Ĺ��̵���⣨��ϸ���̲ο�
[Package a desktop or UWP app in Visual Studio](../../appendix/MSIX/packaging-uwp-apps.md)
����

��ʵ��ľ��岽�����£����������ϸ�ʵ�������ɵ���Ŀ winUITest ��Ϊ����������˵������


1. ���� Active solution configuration Ϊ Release

![set active config](pix/activeConfig.PNG)

2. �һ���Ŀ���Ƶ�� Build ����Ŀ��Ӧ�ó��򣨲����ϸ�ʵ�飩

3. Right-click the project and choose Publish->Create App Packages

![Create App Package...](pix/publish.PNG)

4. Select Sideloading in the first page of the wizard and then click Next

![Select distribution method](pix/distributionMethod.PNG)

5. On the Select signing method page, select whether to skip packaging 
signing or select a certificate for signing. You can create a 
new certificate. For an MSIX package to be installed on an end user's 
machine, it must be signed with a cert that is trusted on the machine.

![Select signing method](pix/signingMethod.PNG)

Here we click "Create..." button to create a test certificate:

![create a test certificate](pix/createTestCert.PNG)

Press the button "OK" will then return to the Select signing method page:

![done creating test certificate](pix/doneSigningMethod.PNG)

6. Complete the Select and configure packages page

![Select and configure packages](pix/sel_n_config_pack.PNG)

7. Input in the UNC path a local folder of your computer to store the package,
and then click the Create button

![input an UNC path](pix/UNC_path.PNG)

here we input "file:///F:/tmp"

8. click "copy and close" to generate the install package

![copy and close](pix/copy_n_close.PNG)

9. �����ڵ�7����������� UNC ·���£�������F:\tmp�������˰�װ��������Ϊ��װ֤��
��δע�������ʹ�á�

![folder of the installation package](pix/folderUNC.PNG)

�������ǽ���5�������Ĳ���֤�����ע�ᣨ���ǰ�ǰ����UNC·����Ϊ��װ��·������
* �򿪰�װ��·�������������һ���ļ��У������� winuiTest_1.0.2.0_Test��
* ���ļ�������һ�� winuiTest_1.0.2.0_x64.msixbundle �ļ����һ����������

![msix attribution](pix/msixAttrib.PNG)

���������ǩ������ǩҳ����ǩ���б��е�ǩ����Ȼ���ٵ����λ���ϸ��Ϣ���鿴֤�顢��װ
֤�飺

![install certificate](pix/installCert.PNG)

��֤�������������ؼ�������󵥻���һ����

![local machine](pix/certImport.PNG)

ѡ������֤�鶼�������д洢���ٵ�������Ȼ��ѡ�������εĸ�֤��䷢���������ȷ����

![save certificate](pix/saveCert.PNG)

ȷ��������һ���Ϳɽ�֤�鰲װ��ϵͳ�С���ҿ��԰�ʵ�鿪ʼǰ����ʵ���еķ����鿴֤��
�Ƿ���ȷ��װ��

10. ���֤�鰲װ��ص���װ��·����������µİ�װ���� winuiTest.appinstaller ��
����˳����ɳ���İ�װ�ˡ���װ��ɺ��ڿ�ʼ�˵���Ϳ��Կ�������װ�ĳ��򣬵�������������У�

![start menu](pix/winStart.PNG)

