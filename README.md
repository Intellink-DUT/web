# 智连星宇网站编辑基本操作

#### 说明：本网站采用 Github+Hexo插件+Butterfly模板 制作，小编只知道下面的方法不会出错，其他的不懂，欢迎接力更新！

### 预先步骤：

配置本地电脑秘钥 ssh key（不要删除原有的ssh key）

#### 方法：
CSDN有很多教程，这里给出一个[参考教程](https://blog.csdn.net/weixin_42310154/article/details/118340458?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522170846999216800215063690%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=170846999216800215063690&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-118340458-null-null.142^v99^control&utm_term=github%E9%85%8D%E7%BD%AEssh%20key&spm=1018.2226.3001.4187)

#### 验证：
输入代码<code>ssh -T git@github.com</code>

如果返回“Hi Intellink-DUT! You've successfully authenticated, but GitHub does not provide shell access.”说明配置正确。

### 首次配置：

在文件夹中选择一个合适的位置，打开cmd，输入以下代码<code>git clone git@github.com:Intellink-DUT/web.git</code>，cmd进入文件夹，输入<code>cd web</code>，~~手动删除web中的.deploy_git文件夹，~~ 配置完毕。

若本地完成过一次clone操作，后续只需要输入<code>git pull</code>则可以完成本地代码的更新。

### 网站编辑：

建议使用VSCode进行编辑，有关主题和博客页面的编辑可直接阅读[Hexo Butterfly官方教程](https://butterfly.js.org/)。

### 网站更新：

在web文件夹中打开cmd，输入<code>hexo clean && hexo generate && hexo deploy</code>

稍等1~2分钟，网站将更新，其中可以查看网站github的Actions查看加载进度。

### web文件夹更新：

在web中打开cmd，输入如下代码：

<code>git add -A</code>

<code>git commit -m '.'</code>

<code>git push</code>

则将完成对web库的内容更新。
