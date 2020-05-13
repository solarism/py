Python教學
================

*   [環境安裝](#install)
    *   [簡易安裝](#easy)
    *   [一般安裝](#normal)
    *   [開發平台安裝](#IDE)
    *   [其他編輯器](#NB)
*   [套件管理工具](#Package)
    *   [The Python Package Installer](#PIP)
    *   [使用方式](#install)
*   [虛擬環境](#Virtualenv)

 
*   [感謝](#acknowledgement)


* * *

<h2 id="install">環境安裝</h2>

<h3 id="easy">簡易安裝</h3>

* 安裝Anaconda https://www.anaconda.com/distribution/ 

    Windows預設安裝路徑在：

      C:\Users\[user]\anacondaX\

    Mac預設安裝路徑在：

<h3 id="normal">一般安裝</h3>

* 下載Python直譯器 https://www.python.org/downloads/ 

    Windows預設安裝路徑在：
  
      C:\Users\[user]\AppData\Local\Programs\Python\PythonX.Y\
   
    Mac預設安裝路徑在：

<h3 id="IDE">開發平台安裝</h3>

* PyCharm https://www.jetbrains.com/pycharm/
* Visual Studio Code (VSCode) https://code.visualstudio.com/ 
* Spyder <font color="steelblue">Anaconda安裝好就有</font>

<h3 id="NB">其他編輯器</h3>

* Jupter Notebook <font color="steelblue">Anaconda安裝好就有</font>
* Google Colaboratory https://colab.research.google.com/ 

<h2 id="Package">套件管理工具</h2>

<h3 id="PIP">The Python Package Installer：pip</h3>

Python安裝完成後，Python 2在2.7.9含以上或Python 3在3.4含以上，預設已經安裝了pip

Windows預設pip路徑在：

    Anaconda安裝
    C:\Users\[user]\anaconda[版本]\Scripts

    一般安裝
    C:\Users\[user]\AppData\Local\Programs\Python\PythonX.Y\Scripts

Mac預設pip路徑在：

<h3 id="install">套件安裝方式</h3>

    $ pip install 套件名稱

Windows預設套件安裝在：

    Anaconda安裝
    C:\Users\[user]\anaconda[版本]\pkgs

    一般安裝
    C:\Users\[user]\AppData\Local\Programs\Python\PythonX.Y\Lib\site-packages

Mac預設套件安裝在：

列出所有已經安裝的套件
    
    pip list 

套件相關資訊與安裝路徑
    
    pip show 套件名稱

<h2 id="Virtualenv">虛擬環境</h2>






---
包括 [Setext] [1]、[atx] [2]、[Textile] [3]、[reStructuredText] [4]、[Grutatext] [5] 和 [EtText] [6]，然而最大靈感來源其實是純文字的電子郵件格式。

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/



是的，這確實需要花比較多功夫來插入 `<br />` ，但是「每個換行都轉換為 `<br />`」的方法在 Markdown 中並不適合， Markdown 中 email 式的 [區塊引言][bq] 和多段落的 [清單][l] 在使用換行來排版的時候，不但更好用，還更好閱讀。

  [bq]: #blockquote
  [l]:  #list

<h3 id="header">標題</h3>

Markdown 支援兩種標題的語法，[Setext] [1] 和 [atx] [2] 形式。



<h2 id="acknowledgement">感謝</h2>

感謝 [leafy7382][] 協助翻譯，[hlb][]、[Randylien][] 幫忙潤稿，[ethantw][] 的[漢字標準格式・CSS Reset][]， [WM][] 回報文字錯誤。

[leafy7382]:https://twitter.com/#!/leafy7382
[hlb]:http://iamhlb.com/
[Randylien]:http://twitter.com/randylien
[ethantw]:https://twitter.com/#!/ethantw
[漢字標準格式・CSS Reset]:http://ethantw.net/projects/han/
[WM]:http://kidwm.net/
