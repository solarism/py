> [name=Weichen]
**Python開發環境**
###### tags: `Python`

[TOC]

* * *

# 環境安裝

在Mac電腦上，若你的系統版本為OS X 10.8-10.15，是內建了Python的。所以不需要另外安裝就可以使用Python，但版本為Python 2.7。有使用過python開發的人都會有以下的困擾，[如下圖]所示：

![](https://i.imgur.com/1vr5xos.png)

[如下圖]: https://xkcd.com/1987/


## 簡易安裝

* 安裝Anaconda：https://www.anaconda.com/distribution/ 

    Windows預設安裝路徑在：

      C:\Users\[user]\anacondaX\

    Mac預設安裝路徑在：
    
      ~/opt/anacondaX/      

### 一般安裝

* 下載Python直譯器：https://www.python.org/downloads/ 

    Windows預設安裝路徑在：
  
      C:\Users\[user]\AppData\Local\Programs\Python\PythonX.Y\
    
    Mac預設安裝路徑在：
    
      自己安裝的python
      /usr/local/bin/
      
      Mac OS內建的python 2.7
      /usr/bin/python2.7
      
* Homebrew安裝Python(限Mac，如Windows可能需另外安裝Cygwin或WSL等linux模擬環境)
    * 安裝Python

          $ brew install python3   
    
    * 如何使用Homebrew
            
            * 安裝Homebrew
              $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"          
            * 搜尋套件
              $ brew search 套件名稱
            * 安裝套件
              $ brew install 套件名稱    
            * 更新所有已安裝的套件
              $ brew upgrade 
            * 移除套件
              $ brew uninstall 套件名稱    
            * 查詢目前已安裝的套件
              $ brew list

* 檢查安裝是否成功

    終端機模式下輸入以下指令，將進入Python交互模式(Interactive Mode)
           
      $ python
 
       Python 3.8.3 (tags/v3.8.3:6f8c832, May 13 2020, 22:37:02) [MSC v.1924 64 bit (AMD64)] on win32
       Type "help", "copyright", "credits" or "license" for more information.
       >>>

    終端機模式下輸入以下指令，將會出現目前python版本

      $ python --version
      Python 3.8.3
      
      或
      
      $ python -V
      Python 3.8.3
    
    查看系統路徑設定
     
      交互模式下
      >>> import sys
      >>> sys.path

      或終端機模式   
      $ python -m site
      
    Windows注意
    
    輸入`python --version`沒反應或輸入`python`開啟Microsoft Store詢問是否透過此安裝python，注意千萬不要再安裝另一個版本python，請至`設定->應用程式->應用程式執行別名`，將python相關的部分關閉

    ![](https://i.imgur.com/toRxZ8o.jpg =300x300)


### 開發平台安裝

* PyCharm：https://www.jetbrains.com/pycharm/
* Visual Studio Code (VSCode)：https://code.visualstudio.com/
    * 並安裝Python延伸模組(Python extension for VSCode) 
* Spyder：<font color="steelblue">Anaconda安裝好就有</font>

### 其他編輯器

* Jupter Notebook：<font color="steelblue">Anaconda安裝好就有</font>
* Google Colaboratory：https://colab.research.google.com/ 

## python使用

     檢查版本
     $ python -V 
     
     執行套件
     $ python -m 套件名稱
     
     查詢使用方式
     $ python -h
     
     直譯.py程式
     $ python 程式名稱.py

## 套件管理工具

### The Python Package Installer：pip

Python安裝完成後，預設已經安裝了pip套件

Windows預設pip路徑在：

    Anaconda安裝
    C:\Users\[user]\anaconda[版本]\Scripts\

    一般安裝
    C:\Users\[user]\AppData\Local\Programs\Python\PythonX.Y\Scripts\

Mac預設pip路徑在：

    Anaconda安裝
    ~/opt/anacondaX/bin/
  
    自己安裝的python
    /usr/local/bin/
      
    Mac OS內建的python 2.7
    /usr/bin/

### 套件安裝方式

一般安裝
    
    $ pip install 套件名稱
    或
    $ python -m pip install 套件名稱

使用 requirements.txt 安裝

    $ pip install -r requirements.txt
      
    requirements.txt 內容應為
    numpy==1.18.2
    pandas==1.0.3
    :
    
    將現有已安裝的套件匯出到 requirements.txt
    $ pip freeze > requirements.txt
    
Windows預設套件安裝在：

    Anaconda安裝
    C:\Users\[user]\anaconda[版本]\Lib\site-packagess\

    一般安裝
    C:\Users\[user]\AppData\Local\Programs\Python\PythonX.Y\Lib\site-packages\

Mac預設套件安裝在：

    Anaconda安裝
    ~/opt/anacondaX/lib/pythonX.Y/site-packages/
  
    自己安裝的python
    /usr/local/lib/pythonX.Y/site-packages/
      
    Mac OS內建的python 2.7
    /usr/lib/

pip常用指令

    套件安裝
    $ pip install 套件名稱
    
    pip更新
    $ pip install --upgrade pip
    
    指定安裝套件版本
    $ pip install -v 套件名稱==版本
    (範例 pip install requests==2.6.0)
    (範例 pip install -v flask==1.0)
    
    更新套件版本
    $ pip install -U 套件名稱
    
    列出所有已經安裝的套件
    $ pip freeze
    或
    $ pip list 

    套件相關資訊與安裝路徑
    $ pip show 套件名稱
    
    移除套件    
    $ pip uninstall 套件名稱
    
## 虛擬環境

當

* 不同專案，要安裝不同套件時
* 不同專案，要安裝相同套件不同版本時

例如應用程式 A 需要一個特定的模組的 1.0 版，但另外一個應用程式 B 需要 2.0 版，這時候就可以用虛擬環境來管理


### step 1：安裝virtualenv套件

    $ pip install virtualenv

### step 2：建立虛擬環境 

建立工作個資料夾(方便管理，非必要)，並且在此資料夾下輸入並執行下列其中一指令

    $ virtualenv 虛擬環境名稱
    或
    $ python -m virtualenv 虛擬環境名稱
    或
    $ python -m venv 虛擬環境名稱

### step 3：進出虛擬環境

Windows環境進入資料夾`\虛擬環境名稱\Scripts\`，Mac環境進入資料夾`/虛擬環境名稱/bin/`，輸入以下指令

    進入虛擬環境
    $ activate

    離開虛擬環境
    $ deactivate

[官方參考資料](https://docs.python.org/zh-tw/3/index.html)

