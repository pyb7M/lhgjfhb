# VLESS Heroku

## ����

������ Heroku �ϲ��� vless+websocket+tls��ÿ�β����Զ�ѡ�����µ� alpine linux �� xray core��  
vless ��� vmess ���ܸ������㣬ռ����Դ���٣����и����ȶ���

## ����

�����Ա�����ռ���ڴ���Դ�ϵͣ������ȶ���

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://dashboard.heroku.com/new?template=https%3A%2F%2Fgithub.com%2Fpyb7M%2Flhgjfhb)

## ע��

### ·��

`WebSocket` ·��(�����ļ��е� `path` )Ϊ `/app` ��

### �˿�

`�˿�` Ϊ `443` ��

### alterId

`alterId` Ϊ `0` ��

### UUID

`UUID` Ĭ��Ϊ `3a53a3e5-da83-48d2-aee9-d88a498eb3dd` ���������á�

## ������ת

����ʹ��cloudflare��workers��`��ת����`������Ϊ��  

addEventListener(  
&emsp;&emsp;"fetch",event => {  
&emsp;&emsp;&emsp;&emsp;let url=new URL(event.request.url);  
&emsp;&emsp;&emsp;&emsp;url.hostname="xx.herokuapp.com";//���heroku����    
&emsp;&emsp;&emsp;&emsp;let request=new Request(url,event.request);  
&emsp;&emsp;&emsp;&emsp;event. respondWith(  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;fetch(request)  
&emsp;&emsp;&emsp;&emsp;)  
&emsp;&emsp;}  
)  
