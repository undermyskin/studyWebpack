npm init————创建新的package.json;

npm install webpack --save-dev————安装webpack并写入package.json

npm install css-loader style-loader --save-dev -g————安装可引入css文件的模块

webpack SOME.js SOME.bundle.js————打包js文件

require('./xxx.js')————CommonJS的方式引用js文件

require('style-loader!css-loader!./style.css')————webpack也可引用css文件，但必须用两个loader：style-loader负责让css在页面中显示出样式，css-loader负责引入css文件
或者：
require('./style.css')————用命令行来进行模块的绑定：webpack hello4js hello4.bundle.js --module-bind "css=style-loader!css-loader"
(注意是双引号""，而不是单引号，并且与js引用模块相比，只需要一个叹号!)

webpack hello4.js hello4.bundle.js --module-bind "css=style-loader!css-loader" --watch————
watch参数：当文件自动改变时，自动重新打包，避免了手动重复输入
progess参数：可以看打包过程
display-modules：显示所有的模块
display-reasons：显示打包模块的原因