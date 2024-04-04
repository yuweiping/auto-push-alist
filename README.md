# auto-push-oss

方便将编译出来的文件上传到alist中

## Inputs

|参数|描述|
|----|----|
|`username`|alist的用户名|
|`password`|alist的密码|
|`upUrl`|alist地址|
|`saveDir`|alist保存的路径|
|`upDir`|本地要上传的目录|
|`upFile`|本地要上传的文件|

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