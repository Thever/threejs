# 打开预览Three.js案例(跨域问题)

不需要加载外部贴图和模型文件的three.js案例，可以直接使用浏览器打开.html案例文件，通常一个threejs项目案例往往都会加载一些外部模型，因此打开threejs案例要搭建一个本地的静态服务器，否则的话，threejs案例无法正常打开，浏览器控制台会提示[跨域问题](http://www.yanhuangxueyuan.com/three.js_course/longword/crossdomain.html)。

如果你知道怎么搭建本地静态服务器，自己用任何方式搭建都可以。如果不了解的话，建议使用nodejs去快速搭建一个本地静态服务器，对于一个WebGL工程师或前端工程师来说，肯定是要学习Nodejs的。

### Nodejs本地静态服务器

使用Nodejs搭建本地静态服务器很简单，首先是你要先百度Nodejs安装的相关文章，先在你的电脑上安装配置好Nodejs，熟悉下NPM的使用，然后使用npm执行`npm install -g live-server`安装`live-server`模块，如果你想通过安装好的`live-server`模块开启一个静态服务器，打开命令行，进入threejs案例所在的文件目录，然后执行`live-server`命令就可以。

通过浏览器访问`http://localhost:8080`或`http://127.0.0.1:8080`地址，找到threejs案例的.html文件直接打开就可以看到三维场景渲染效果。

### 开发调试-热更新

在学习threejs的过程中，往往需要频繁的代码测试，查看threejs代码的渲染效果。这时候你肯定希望代码修改之后，threejs渲染效果立即热更新。

如果通过`live-server`模块搭建的本地静态服务器，你可以实现代码的热加载。也就是说你修改一段代码，然后保存.html代码文件，.html对应的threejs案例就会重新渲染。
