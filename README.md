# fscan_poc

由于fscan的端口扫描以及漏洞扫描集成比较方便，因此也会常常被用于安全检查中，这里从其他项目中改写了一些poc，如果某个poc存在bug请及时联系作者解决。如果您有希望加入的poc，也可以联系作者进行添加。

如果有需求，联系作者获取。

感谢以下师傅对问题的提交:
s1g0day、cross

更新
```
本次更新首次使用了<response.body != "">的语法，但是没有验证表达式是否有效，如果无法使用，感谢及时反馈。

更新了2024HW期间海康威视、亿赛通、用友的部分POC
hikvision-iSecure-Cente-clusters-fileupload
hikvision-iSecure-Cente-detection-Rce
hikvision-iSecure-Cente-licenseExpire-Rce
hikvision-iSecure-Cente-uploadAllPackage-fileupload
yisaitong-CDG-DecryptionApp-deserialization-rce
yisaitong-CDG-docRenewApp-deserialization-rce
yisaitong-CDG-druid-submitLogin-defaultpasswd
yisaitong-CDG-getAllUsers-info-leak
yisaitong-CDG-SecureUsbConnection-deserialization-rce
yonyou-crm-help-fileread
yonyou-crm-reservationcomplete-rce
yonyou-NC-cloud-queryPsnInfo-sqli
yonyou-NC-cloud-queryStaffByName-sqli
yonyou-UFIDA-NC-fileupload-rce
yonyou-UFIDA-NC-querygoodsgridbycode-sqli
```



```
增加
poc-finger-geoserver
poc-geoserver-cve-2024-36401-rce
这里在测试时发现由于延迟问题导致未发现漏洞问题，但是没有确定是否为特例，需要在测试时关注
```


```
1.修改了一部分报错的poc，由于在代码中加入了反引号导致的poc报错
2.修改了一些引号滥用问题
wanhu-OA-ezOffice-RhinoScriptEngineService-rce
yongyou-ksoa-sKeyvalue-sqli

3.删除了一部分时间注入的POC，这里由于fscan无法测试时间注入，因此在寻找到更好的方法后重新引入
yonyou-UFIDA-NC-pagesServlet-sqli
hongjing-hcm-pos_dept_post-sql-injection
yonyou-grp-u8-bx_dj_check-sql-injection
yonyou-grp-u8-u8qx-sql-injection
weaver-ecology-filedownloadforoutdoc-sqli
yongyou-grp-u8-bx_historyDataChecks-sqli
poc-yaml-FZMediaEditor-binary-SQL-injection
poc-yaml-yisaitong-secretkeyservice-sql-injection
poc-yaml-yisaitong-JLockSeniorDao-findByLockName-dwr-sql-injection
poc-yisaitong-update-sqli

4.关于误报poc建议师傅们自己选择是否保留
alibaba-nacos-config-download
alibaba-nacos-sync-unauth
DH-DSS-user_edit_action-Information-disclosure

```


```
poc-yaml-SpringBlade-tenant-list-sqli
hongjing-hcm-pos_dept_post-sql-injection
poc-yaml-FZMediaEditor-assess-syn-Information-disclosure
Hikvision-iSecure-Cente-download-readfile
poc-yaml-yisaitong-JLockSeniorDao-findByLockName-dwr-sql-injection
wanhu-ezEIP-success-deserialization
yonyou-grp-u8-bx_dj_check-sql-injection
yonyou-grp-u8-u8qx-sql-injection
Hikvision-iSecure-Cente-AutoLoginTicket-Rce
poc-yaml-h3c-nms-arbitrary-file-read
weaver-oa-e-cology-resourceservlet-file-read
poc-yaml-FZMediaEditor-binary-SQL-injection
yonyou-UFIDA-NC-pagesServlet-sqli
weaver-oa-ecology-filedownload-file-read
DH-DSS-user_edit_action-Information-disclosure
yonyou-u8-crm-file-upload
poc-yaml-PHP-CGI-Windows-RCE-CVE-2024-4577
yonyou-nc-downCourseWare-fileread
poc-yaml-dx-gateway-config-manage-fileupload
poc-yaml-ruijie-selfservice-login_judge-fileread
poc-yaml-nexus-repo-path-traversal
poc-yaml-REALOR-agentboard-xgi-sql-injection
poc-yaml-yisaitong-secretkeyservice-sql-injection
poc-yaml-cmecloud-console-readfile
hongjing-hcm-OutputCode-file-read
poc-yaml-kingdee-cloud-user-deserialization-vuln
hongjing-hcm-openFile-file-read
```


```
poc-yaml-sslvpn-path-rce
dahua-dss-file-read
dahua-icc-readpic-fileread
dahua-smart-downloadbyurlatt-fileread
dahua-zhyq-getfacecapture-sqli
dahua-zhyq-password-disclosure
dahua-zhyq-pio-fileupload
dahua-zhyq-video-fileupload
alibaba-nacos-actuator-leak
alibaba-nacos-config-server-sql-inject
alibaba-nacos-authentication-bypass
alibaba-nacos-default-password
alibaba-nacos-jraftserver-deserialization-rce
alibaba-nacos-secret-default-key-unauth
alibaba-nacos-severidentity-bypass
alibaba-nacos-core-auth-enabled-bypass
alibaba-nacos-sync-unauth
grafana-file-read
hikvision-files-upload
hikvision-ivms-8700-upload-action-upload
hikvision-af-env-info-disclosure
hikvision-anfang-files-fileupload
hikvision-anfang-report-fileupload-2
hikvision-anfang-report-fileupload
hikvision-downdb-file-read
hikvision-userxml-info-disclosure
nsfocus-sas-getfile-readfile
nsfocus-sas-localuser-login-anyuser
yonyou-chanjet-tplus-password-reset
yonyou-chanjet-gnremote-sql-inject
yonyou-chanjet-tplus-file-upload
yonyou-chanjet-tplus-rce
yonyou-chanjet-tplus-read-file
yonyou-cloud-jsinvoke-uploadfile
yonyou-fe-templateoftaohong-manager-path-traversal
yonyou-grp-u8-app-proxy-uploadfile
yonyou-grp-u8-bx_historyDataChecks-sqli
yonyou-grp-u8-logs-disclosure
yonyou-grp-u8-uploadfiledata
yonyou-grp-u8-upload-file-data
yonyou-mobile-uploadapk-fileupload
yonyou-nc-accept-upload
yonyou-nccloud-ncchr-fileupload
yonyou-nccloud-uapjs-upload-rce
yonyou-nc-download-fileread
yonyou-nc-monitorservlet-rce
yonyou-nc-ncmessageservlet-rce
yonyou-nc-uploadservlet-rce
yonyou-nc-word-docx-fileread
yonyou-u8-cloud-fileupload
yonyou-u8-crm-getemaildata-fileread
yonyou-u8-crm-getemaildata-uploadfile
yonyou-ufida-ksoa-image-upload-file
yonyou-ufida-oa-uapws-xxe
poc-wangshen-SecGate3600-loginpass
seeyon-resetpassword-anyuser
seeyon-a6-config-disclosure
seeyon-a6-createmysql-disclosure
seeyon-fanruan-report-server-directory-travesal
seeyon-m1-usertokenservice-rce
seeyon-oa-ajax-anyfile-upload
seeyon-wpsassistservlet-fileread
seeyon-wps-assist-servlet-upload
tongda-contact-list-disclosure
tongda-down-php-unauthorized-access
tongda-oa-2017-auth-bypass
tongda-oa-logincode-any-user-login
tongda-path-traversal
tongda-report-bi-func-sql-inject
tongda-swfupload-new-sql-inject
tongda-v11-getdata-rce
tongda-v11-session-disclosure-login-bypass
tongda-v2017-video-file-file-read
tongda-oa-header-inc-login
weaver-ecology-oa-plugin-checkserver-setting-sqli
weaver-oa-workrelate-file-upload
e-bridge-saveyzjfile-file-read
ecology-changeuserinfo-info-leak
ecology-e-office-getselectlist-crm-sqli
e-cology-e-office-officeserver-file-read
ecology-filedownloadforoutdoc-sqli
e-cology-getsqldata-sql-inject
ecology-ifnewscheckoutbycurrentuser-dwr-sqli
e-cology-jqueryfiletree-ile-inclusion
ecology-ktreeuploadaction-upload
ecology-oa-database-info-leak
ecology-oa-deleteuserrequestinfobyxml-xxe
e-cology-oa-e-weaver-signature-download
ecology-ofslogin-aul
e-cology-v8-sqli
e-cology-verify-quick-login-user-login
ecology-gete9developallnamevalue2-fileread
weaver-ecology-XmlRpcServlet-FileRead
poc-qmxc-4A-info-leak
poc-yaml-webui-fileread
poc-yaml-sslvpn-suffix-rce
spon-broadcastsystem-rce
poc-aiohttp-path-travesal
nsfocus-sas-localuser-login-anyuser
nsfocus-sas-getfile-readfile
poc-yisaitong-rce
poc-yisaitong-S2-fileupload
poc-yisaitong-SC-fileupload
poc-yisaitong-update-sqli
poc-yml-magic-api-unauth
```


## 仅供技术研究使用，请勿用于非法用途，否则后果作者概不负责

## This is for technical research only, please do not use it for illegal purposes, otherwise the author will not be responsible for the consequences.

## 如果存在误报可以添加作者进行排查解决，感谢您的支持

![image](https://github.com/fliggyaa/fscanpoc/assets/82925172/fa29250c-6591-423d-acb4-6c74aa5157ce)

