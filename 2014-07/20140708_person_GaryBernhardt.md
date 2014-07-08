# Gary Bernhardt, Talks and TDD War

<a href="https://www.flickr.com/photos/kennethreitz/8031978409" title="Gary Bernhardt by Kenneth Reitz, on Flickr"><img src="https://farm9.staticflickr.com/8178/8031978409_82998db0fd_o.jpg" alt="Gary Bernhardt"></a>   <sup>Photo taken by [Kenneth Reitz](https://www.flickr.com/photos/kennethreitz/) on Flickr</sup>

## 錄影、演講

最先注意到這位仁兄，是看到他的 [Destroy All Software] 系列錄影（原先是收月費，現在則將所有影片分季賣，一季美金 $40 元，共五季）。有幾則錄影讓我印象深刻：

- [Statistics Over Git Repositories]
- [Processes and Jobs]
- [File Navigation in Vim]
- [Composing a Unix Command Line]

[Gary Bernhardt] 在 [Destroy All Software] 錄影教學裡使用的程式語言以 Python, Ruby 為主，搭配行雲流水的 Vim 操作技，口、腦、手同步的展示技巧（他的錄影都是 Live Recording，幾無後製），讓我極為佩服。訂閱了幾個月的 [Destroy All Software]，後因主題多以 Ruby/Rails 為主，離我興趣甚遠，便不再續訂。

[Gary Bernhardt] 的演講風格與 [Scott Hanselman] 有些相似：他們的場子總是歡樂無窮，笑聲不斷，而且幾無冷場。拿這場 Lightning Talk〈[Wat](https://www.destroyallsoftware.com/talks/wat)〉為例，內容與 Ruby, JavaScript 有關。短短五分鐘，笑聲不斷。

另外這場〈[The Birth & Death of JavaScript]〉，主題是 JavaScript, [asm.js]，談的是電腦科學領域的一個概念：

> All problems in computer science can be solved by another level of indirection.

幾乎所有電腦軟體皆由（或可由） C 語言寫就，有了可以把 C 語言編譯成 asm.js 的工具，理論上，所有電腦軟體皆可執行於瀏覽器內，包含 C 語言編譯器，甚至作業系統。這樣的概念可以一直延伸，這也是電腦科學迷人之處：無限可能。

## 文章

除了演講，[Gary Bernhardt] 也寫文章。產量不多，最近期的是針對 [DHH 挑起的 TDD 之爭](Slow database test fallacy)，提出自己的見解－〈[TDD, Straw Men, and Rhetoric]〉。結論是認為 DHH 據以批評 TDD 的理由，根本引用失據，而且不符事實。他認為從 DHH 的文章可以看出：

> David's tests run in a few minutes, and he's fine with that....   I'm not fine with that. A lot of other people are not fine with that.

[Destroy All Software] 的錄影有很多 TDD 有關的主題（RSpec, Isolated Test）。[Gary Bernhardt] 尤其重視測試運行的時間，他認為測試完成的時間應該小於 300ms（毫秒）。文章裡有句話這麼說：

> I aim for test feedback in 300 ms, from the time I press enter to the time I have a result. That's not an abstract desire; I frequently achieve it.

看過他的錄影就知道他所言不假。

## 結論

有個人風格的技術表演者。

[Gary Bernhardt]:https://twitter.com/garybernhardt
[Talks]:https://www.destroyallsoftware.com/talks
[Destroy All Software]:https://www.destroyallsoftware.com/screencasts
[Statistics Over Git Repositories]:https://www.destroyallsoftware.com/screencasts/catalog/statistics-over-git-repositories
[Processes and Jobs]:https://www.destroyallsoftware.com/screencasts/catalog/processes-and-jobs
[File Navigation in Vim]:https://www.destroyallsoftware.com/screencasts/catalog/file-navigation-in-vim
[Composing a Unix Command Line]:https://www.destroyallsoftware.com/screencasts/catalog/composing-a-unix-command-line
[Scott Hanselman]:http://www.hanselman.com/speaking/
[The Birth & Death of JavaScript]:https://www.destroyallsoftware.com/talks/the-birth-and-death-of-javascript
[asm.js]:http://asmjs.org/
[TDD, Straw Men, and Rhetoric]:https://www.destroyallsoftware.com/blog/2014/tdd-straw-men-and-rhetoric