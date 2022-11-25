forked from [yangyinchun/yapi-plugin-ms-oauth](https://github.com/yangyinchun/yapi-plugin-ms-oauth)

Yapi第三方插件，Microsoft Azure Active Directory 基于oauth2协议登录，安装并且在配置文件中添加如下配置：

```yaml
"plugins": [{
    "name": "aadsso",
    "options": {
      "type": "oauth2",
      "hostscheme": "https",
      "hostname": "login.partner.microsoftonline.cn",
      "authPath": "/8209af61-7dcc-42b8-8cdf-xxxxxxxxxxxx/oauth2/v2.0/authorize",
      "tokenPath": "/8209af61-7dcc-42b8-8cdf-xxxxxxxxxxxx/oauth2/v2.0/token",
      "redirectUri": "https://yapi.example.com/api/plugin/oauth2/callback",
      "appId": "d4b1f920-ecf9-4386-adbc-xxxxxxxxxxxx",
      "appSecret": "ffl3k8E~.s7VsXgXT-l3I5Xt_xxxxxxxxx"
    }
  }
]
```

### 需要修改的配置项
名称 | 含义 | 示例
---------|-------------|----
hostname | 终结点域名 | Azure AD: login.microsoftonline.com
 　 | 　 | Azure AD China: login.partner.microsoftonline.cn
authPath | OAuth 2.0 授权终结点(v2) | /[Tenant ID]/oauth2/v2.0/authorize
tokenPath | OAuth 2.0 令牌终结点(v2) | /[Tenant ID]/oauth2/v2.0/token
redirectUri | 重定向 URI | https://yapi.example.com/api/plugin/oauth2/callback
appId | 应用程序(客户端) ID | d4b1f920-ecf9-4386-adbc-xxxxxxxxxxxx
appSecret | 客户端密码 | ffl3k8E~.s7VsXgXT-l3I5Xt_xxxxxxxxx