Laravel Sanctum 为 SPA (单页面应用程序)、移动应用程序和简单的、基于令牌的 API 提供轻量级身份验证系统。Sanctum 允许应用程序的每个用户为他们的帐户生成多个 API 令牌。这些令牌可能被授予指定允许令牌执行哪些操作的能力 / 范围。

简单理解，某系统包含商品管理模块goods和文章管理模块post，同时呢系统中的admin用户，可以管理这些模块，
现在有新用户a需要访问并操作商品api，我们可以使用Laravel Sanctum把商品相关API包裹起来，为admin生成一个token，ability定义为`goods/*`。
然后把token给用户a就可以了，用户a请求商品api时，到header里带上`Authorization: Bearer <生成的token>`就可以了

### 课程来源
https://www.youtube.com/watch?v=MT-GJQIY3EU&ab_channel=TraversyMedia

### Postman API导入
lara-sanctum-api.postman_collection.json

注意使用的是数据库是`database/database.sqlite`，直接用navicat打开即可测试
