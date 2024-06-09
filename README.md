

## Pages 部署方法
### 1. 部署 Cloudflare Pages：
   - 在 Github 上先 Fork 本项目，并点上 Star !!!
   - 在 Cloudflare Pages 控制台中选择 `连接到 Git`后，选中 `CF-Workers-SUB`项目后点击 `开始设置`。

### 2. 给 Pages绑定 自定义域：
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `fuck.cloudns.biz`，则添加自定义域填入 `sub.fuck.cloudns.biz`即可；
   - 按照 Cloudflare 的要求将返回你的域名DNS服务商，添加 该自定义域 `sub`的 CNAME记录 `CF-Workers-SUB.pages.dev` 后，点击 `激活域`即可。

### 3. 修改 快速订阅入口 ：

  例如您的pages项目域名为：`sub.fuck.cloudns.biz`；
   - 添加 `TOKEN` 变量，快速订阅访问入口，默认值为: `auto` ，获取订阅器默认节点订阅地址即 `/auto` ，例如 `https://sub.fuck.cloudns.biz/auto`

### 4. 添加你的节.点和订.阅链接：
   - 添加 `LINK` 变量，参数添加你的自建链接和订.阅链接，确保每行一个链接，例如：
   ```
   aaaa
   ```




## 变量说明
| 变量名 | 示例 | 备注 | 
|--------|---------|-----|
| LINK | vless://b7a39... vmess://ew0K... https://sub...  | 可同时放入多个节 点链接与多个订 阅链接, 链接之间用换行做间隔 | 
| TOKEN | auto | 快速订 阅内置节.点的订阅路径地址 /auto | 
| TGTOKEN | 6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXXXXqWXgBA | 发送T.G通知的机器人token | 
| TGID | 6946912345 | 接收t.g通知的账户数字ID | 
| SUBAPI | apiurl.v1.mk | clash、singbox等 订阅转换后端 | 
| SUBCONFIG | [https://raw.github.../ACL4SSR_Online_MultiCountry.ini](https://raw.githubusercontent.com/cmliu/ACL4SSR/main/Clash/config/ACL4SSR_Online_MultiCountry.ini) | clas h、singb ox等 订.阅转换配置文件 | 


