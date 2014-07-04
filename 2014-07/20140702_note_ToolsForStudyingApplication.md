# [免費好物] Process Explorer

軟體工程師除了「開發」軟體，也「使用」軟體。許多工程師藉由「研究」軟體來增加功力，增廣見聞——如果你沒這習慣，為了自己的職涯發展，最好現在開始養成。

我是軟體工程師，我用軟體解決問題。有時候遇到好用的軟體，我會很好奇的想了解它們是怎麼做出來的：使用了哪些技術？背後的理念為何？

本文介紹 [Process Explorer]，由神人 [Mark Russinovich] 所開發。被微軟招募後，馬克的公司（Sysinternals）及其作品皆納入微軟TechNet 旗下，供大眾免費享用。Process Explorer 的功能多不勝數，接下來介紹幾個我常用的功能：

## Process 子母關係

有些程式表面看起來只有單一執行檔，運行時卻會「生」出其他 process（行程）。透過 Process Explorer，我可以觀察 Processes 之間的子母關係，進而推敲出其運作原理。

底下是 Google Chrome 運行時的狀態，外掛裝越多，Process生越多：

![Google Chrome in Process Explorer](https://dl.dropboxusercontent.com/u/367600/blog_assets/20140704_ProcessExplorerChromeProcesses.png)

## Process 相依的模組

單一程式要能夠運行，需配合許多其它模組。透過 Process Explorer 的 **View Handle**/**View DLLs** 的功能，可以找出該 Process 相依於哪些模組。

我經常使用此功能來找出軟體用到了哪些第三方函式庫。下圖為 MarkdownPad 的模組相依圖，我是這樣發現 [Awesomium]，並把它排入之後研究的目標。

**View DLLs** 還可以用來觀察某模組的載入與釋出，這個功能對於開發軟體很有幫助。舉例來說，當你的程式用到 LoadLibrary / FreeLibrary 來動態載入與釋出某個 DLL，則 Process Explorer 能夠即時顯其載入與釋出的相關資訊。

![Process Explorer View DLLs](https://dl.dropboxusercontent.com/u/367600/blog_assets/20140704_ProcessExplorerDllDep.png)

## Process 即時資訊

Process Explorer 可即時顯示 Process 的相關資訊，豐富的程度令人佩服。這個功能最適合「近距離、貼身」觀察某程式的運作狀態。下圖顯示 MarkdownPad 的執行緒狀態：

![MarkdownPad Threads](https://dl.dropboxusercontent.com/u/367600/blog_assets/20140704_ProcessExplorerProperties.png) 

## 結論

Process Explorer 是我天天都會用到的工具，通常都是開機後就執行起來，用以掌握電腦的即時狀態。作者神人馬克曾說這個工具是用來取代 Windows 內建的 Task Manager。這個目的可說百分之百達成！

[Spy++]:http://msdn.microsoft.com/zh-tw/library/vstudio/dd460760.aspx
[Process Explorer]:http://technet.microsoft.com/en-us/sysinternals/bb896653
[Mark Russinovich]:http://en.wikipedia.org/wiki/Mark_Russinovich
[Awesomium]:http://www.awesomium.com/