2020.11.27

迫于赚钱，要做php项目

于是跟着李炎恢老师的教程学习ThinkPHP6.x，边学边做

跟着第一课安装tp6.0的时候就他妈问题一堆

由于前几天想学5.1的时候已经安装了Composer

今天通过composer安装tp6发现安装不了，我以为是composer的问题

于是重新安装composer，万万没想到，这一步耗费了我一大晚上的时间

重新安装composer出现了一个问题，始终解决不了

通过软件包安装始终安装不了

因此最后是通过全局安装才安装上

#### composer全局安装

全局安装是将 Composer 安装到系统环境变量 `PATH` 所包含的路径下面，然后就能够在命令行窗口中直接执行 `composer` 命令了。

##### Mac 或 Linux 系统：

打开命令行窗口并执行如下命令将前面下载的 `composer.phar` 文件移动到 `/usr/local/bin/` 目录下面：

复制

```bash
sudo mv composer.phar /usr/local/bin/composer
```

##### Windows 系统：

1. 找到并进入 PHP 的安装目录（和你在命令行中执行的 `php` 指令应该是同一套 PHP）。
2. 将 `composer.phar` 复制到 PHP 的安装目录下面，也就是和 `php.exe` 在同一级目录。
3. 在 PHP 安装目录下新建一个 `composer.bat` 文件，并将下列代码保存到此文件中。

复制，编辑到composer.bat文件

```bash
@php "%~dp0composer.phar" %*
```

最后重新打开一个命令行窗口试一试执行 `composer --version` 看看是否正确输出版本号。



然而安装好了composer还是不能安装tp6

到系统命令行输入php -v后发现版本是5.6.40

而我wamp选定的php是7.3.21

查百度说是环境变量的问题，于是改了图中的变量

<img src="C:\Users\Sylow\AppData\Roaming\Typora\typora-user-images\image-20201128010706778.png" alt="image-20201128010706778" style="zoom:50%;" />

结果重启php -v还是5.6.40，查了半天还是都说是环境变量的问题

终于我再次尝试设置环境变量，才发现我犯了个愚蠢的错误

<img src="C:\Users\Sylow\AppData\Roaming\Typora\typora-user-images\image-20201128010934863.png" alt="image-20201128010934863" style="zoom:50%;" />

是应该设置系统变量，全局的。我之前是改了当前用户的变量，可把我蠢疯了

最终解决的tp6安装不上的原因是php的系统全局变量没设置到7.3.21的路径

就这个问题， 折腾了我一个晚上，我他妈蠢哭了。。。

