/*******************************
  公众号:木木IOS分享
关注了解更多新科技！！！
白描 文字识别 A+
脚本名称:白描 文字识别 A+
使用声明：️此脚本仅供学习与交流，
        请勿转载与贩卖！️️️
群1077223830
*******************************
[rewrite_local]
^http[s]?:\/\/baimiao.uzero.cn\/api\/*.+$ url script-response-body baimiao.js
[mitm] 
hostname = *.baimiao.*
*******************************
Surge

[Script]
^http[s]?:\/\/baimiao.uzero.cn\/api\/*.+$ requires-body=1,max-size=0,script-path=baimiao.js

[MITM]
hostname = *.baimiao.*

*******************************/
var obj = JSON.parse($response.body);
    obj.recognizeTranslateAll= 999;
obj.normalCount= 999;
obj.batchCount= 999;
obj.translateCount= 999;
obj.remainNormal= 999;
obj.remainBatch= 999;
obj.remainTranslate= 999;
    $done({body: JSON.stringify(obj)});
