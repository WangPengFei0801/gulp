# gulp
主要记录了一些关于gulp的一些事情
第一点：gulp的相关概念
  专业的术语将gulp称为前端自动化工具
  那么？什么是前端自动化工具？？
  通俗的来说比如我们去加工一瓶矿泉水 肯定的包含什么贴标签啊，盖瓶盖这些操作· 那么如果将这些东西全部交给机器自动化完成那是不是很提高我们的
  工作效率，同样的来说·在前端开发领域 我们的代码压缩等操作也是必不可少的操作 ，这时候我们就将其交给前端自动化工具来完成 。
  其中有很多的前端自动化工具 ：gulp（流体化）（在一个工作间 不断的js来和去）
                            grunt（频繁的操作IO流）（比如一段js-进去---出来 进去出来这样的操作很不好）
                            webpeak等
                            注释：全局安装相当于你安装了一个大型软件（eg.ps） 是我们软件运行的环境
                                  然后是在项目本身中安装一个插件 是用来被项目调用
                            
  Gulp：
     第一步：安装：详情请见我的qq记事本实现第一个默认程序：
     第二部：实现插件的安装以及使用：
             gulp常用插件 npm install --save-dev gulp-stylus（插件名称）

. 编译stylus (gulp-stylus)
. 压缩css (gulp-minify-css)
. 压缩js (gulp-uglify)
. 压缩图片 (gulp-imagemin)
. js检查 (gulp-jshint)
. 文件合并 (gulp-concat)
. 自动刷新 (gulp-livereload) 需要安装谷歌插件LiveReload(2.0.9)
. 文件清理 (gulp-clean)
. 变动监听 (gulp-cache) 只有文件变化了才再次触发任务
. 变动通知 (gulp-notify)
. 文件重命名 (gulp-rename)；
然后在文档中引用先关的插件：var stylus = require('gulp-stylus');
然后实现相关任务：eg：
gulp.task('one', function () {
  return gulp.src('./css/one.styl')
    .pipe(stylus())
    .pipe(gulp.dest('./css/build'));
});
其中one代表的是任务文件名称
. gulp.task() 用来定义任务
. gulp.src() 需要处理的源文件路径
. gulp.dest() 处理后的发布路径
. gulp.watch() 用来监视文件的变化，当文件发生变化后，我们可以利用它来执行相应的任务，例如文件压缩等。

     
