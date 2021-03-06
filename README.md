# WatcherVim

## 快捷键
### 多文件
#### 1·vim未启动时
  vim file1 file2 ... filen
#### 2·vim已经启动
  :e file        再打开一个文件   
  Ctrl + 6       切换文件   
  :bn            下一个文件   
  :bp            上一个文件   
  :ls            列出打开的文件，带编号   
  :b1~n          切换至第n个文件

### 多窗口
  Ctrl + ww      切换到下一个窗格

### 复制多行
在命令模式下，将光标移动到将要复制的首行处，按“nyy”复制n行；其中n为1、2、3......

### 粘贴
在命令模式下，将光标移动到将要粘贴的行处，按“p”进行粘贴

### 删除一行
在命令模式下，将光标移动到将要删除的行处，但“dd”进行删除

## Ctags on OSX
**Snow Leo ships with ctags not suitable for Ruby development. I.e. if you try to generate tags recursively, it will error out:**   

`$ ctags -R`   
ctags: illegal option -- R   
usage: ctags [-BFadtuwvx] [-f tagsfile] file ...

`$ which ctags`   
/usr/bin/ctags

**homebrew to the rescue:**

`$ brew install ctags`   
==> Downloading http://downloads.sourceforge.net/ctags/ctags-5.8.tar.gz   
######################################################################## 100.0%   
==> ./configure --prefix=/usr/local/Cellar/ctags/5.8 --enable-macro-patterns--mandir=/usr/local/Cellar/ctags/5.8/share/man --with-readlib   
==> make install   
/usr/local/Cellar/ctags/5.8: 6 files, 392K, built in 12 seconds

**Now we need to alias ctags to use new version:**

``$ alias ctags="`brew --prefix`/bin/ctags"``   

**And now back to coding:**

`$ ctags -R`   
ctags: Warning: ignoring null tag in public/audio/audio-player.js   

**Dont forget to save ctags alias, ie like this:**

`$ alias ctags >> ~/.zshrc`   

**And yes, homebrew rocks!**

## Tips
  Mac os中，Ctrl = shift + control
