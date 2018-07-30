# webpack-2

项目克隆：git clone git@github.com:luojiao123/webpack-2.git

安装依赖：npm install

运行：webpack-dev-server






webpack的深度配置

在服务器上使用：

生产环境              webpack -pw

开发环境              webpack-dev-server


安装  环境-全局安装

npm i webpack-dev-server -g   // 安装过就无需再次安装


开发环境运行

使用时直接在命令中输入  webpack-dev-server即可

如果想要更改访问的端口号则输入： webpack-dev-server  --port  2999


访问：localhost:2999


优点：修改内容保存后可直接在浏览器看到效果，不需要多次运行


端口号也可在webpack.config.js中直接修改配置：

devServer:{

    port:1289,   // 端口配置

    open:true,   // 运行就直接在浏览器打开，默认false

    inline:true,   // 自动刷新，默认true

    contentBase:'./app', // 指定服务器目录

}


指定服务器目录示例：

在根目录（webpack.config.js所在目录）新建一个app文件夹

将index.js和index.html放入app文件夹

然后在webpack.config.js文件配置 contentBase:'./app'

entry入口文件修改成 entry:'./app/index.js'

运行webpack：webpack-dev-server，打开浏览器查看也能正常显示



