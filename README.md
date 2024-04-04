# auto-push-oss

方便将编译出来的文件上传到alist中

## Inputs

|参数|描述|必填|
|----|----|----|
|`username`|alist的用户名|是|
|`password`|alist的密码|是|
|`upUrl`|alist地址|是|
|`saveDir`|alist保存的路径|是|
|`upDir`|本地要上传的目录|否|
|`upFile`|本地要上传的文件|否|
|`asTask`|是否添加为任务，默认为否,除了true其余值均为否|否|

## Example usage

上传文件夹
```yaml
uses: yuweiping/auto-push-alist@master
with:
  username: ${{secrets.alistName}}
  password: ${{secrets.alistPasswd}}
  upUrl: http://v5.123456.xyz
  saveDir: /public/baiduyun/
  upDir: ./apks
  asTask: ture
```

上传文件
```yaml
uses: yuweiping/auto-push-alist@master
with:
  username: ${{secrets.alistName}}
  password: ${{secrets.alistPasswd}}
  upUrl: http://v5.123456.xyz
  saveDir: /public/baiduyun/
  upFile: apks
```