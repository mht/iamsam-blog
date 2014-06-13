[筆記] Vesper Sync Design 教我的事

這篇〈[How to Make a Vesper: Sync]〉由 [Vesper] 的另一位成員所撰寫，主要提供開發 Vesper Sync 功能背後的諸多考量。有幾項我覺得不錯，值得學起來：

### Do not use 'no-reply' for e-mail confirmation

標準的「新增帳號」流程，其中一步通常會寄送一張「確認函（Confirmation E-mail）」至指定的電子信箱，使用者點選隨信的超連結即完成確認。

[Vesper] 也採用同樣流程，但與其他服務不同之處在於：該郵件上的「寄件人住址」非 no-reply，而是 Vesper 的支援電郵。

如此一來，使用者不但確認自己帳戶，同時也得知該產品的支援信箱，若遇上問題，直接回覆該郵件即可與開發商聯絡。

[Dave Wiskus]:https://twitter.com/dwiskus
[Vesper]:http://vesperapp.co/
[How to Make a Vesper: Sync]:http://bit.ly/1wZdNHr