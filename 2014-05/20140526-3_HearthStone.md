# 緣起

不少網站提供玩家查詢[爐石戰記]卡牌的相關資訊，不過，由於官方沒提供，因此每家都自建「卡牌資料庫」。雖然可以查到卡牌資料，但我覺得還不夠好。如果能有一個開放原始碼的「爐石戰記卡牌資料庫」，該有多好！

開放的「爐石戰記卡牌資料庫」，再加上統一的「卡牌編碼」，可以做什麼呢？

> The Only Limitation Is Your Imagination.

本文討論以下項目：

- 爐石戰記卡牌編碼法（HearthStone Card Index (HSCI)）
- HSCI in JSON
- 潛在應用
  - Replay
  - P2C (Person to Computer)


# 爐石戰記卡牌編碼

目前想到的編碼方式有兩種：

- 五碼，由左至右：
  - 前二碼（12\*\*\*）表示**職業（Class）**。**0** 表示中立（All），**01** 表示德魯伊（Druid），以此類推（全職業列表後述）。
  - 第三碼（\*\*3\*\*）表示稀有度（Rarity），**0** 表示基本牌（Basic），**1** 表示普通（Common），以此類推（全稀有度後述），例：
  - 第三至五碼（\*\*\*45）表示卡牌編號。     
- 三碼，號碼由 0 - 999，照順序排，不加任何輔助資訊。

## 五碼編法

爐石戰記目前版本（1.0.0.5314）共有九種職業，為因應未來需求，故以兩位數表示職業。全職業表列如下：

<table>
  <tr>
    <td>ID</td>
    <td>Class</td>
    <td>藝名</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Druid</td>
    <td>德魯伊</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Hunter</td>
    <td>獵人</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Mage</td>
    <td>法師</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Paladin</td>
    <td>聖騎士</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Priest</td>
    <td>牧師</td>
  </tr>
  <tr>
    <td>6</td>
    <td>Rogue</td>
    <td>盜賊</td>
  </tr>
  <tr>
    <td>7</td>
    <td>Shaman</td>
    <td>薩滿 </td>
  </tr>
  <tr>
    <td>8</td>
    <td>Warlock</td>
    <td>術士</td>
  </tr>
  <tr>
    <td>9</td>
    <td>Warrior</td>
    <td>戰士</td>
  </tr>
</table>

卡牌稀有度目前分為五種：

<table>
  <tr>
     <td>ID</td>
     <td>Rarity</td>
     <td>中文</td>
  </tr>
  <tr>
     <td>1</td>
     <td>Basic</td>
     <td>基本</td>
  </tr>
  <tr>
     <td>2</td>
     <td>Common</td>
     <td>普通</td>
  </tr>
  <tr>
     <td>3</td>
     <td>Rare</td>
     <td>精良</td>
  </tr>
  <tr>
     <td>4</td>
     <td>Epic</td>
     <td>史詩</td>
  </tr>
  <tr>
     <td>5</td>
     <td>Legendary</td>
     <td>傳說</td>
  </tr>
</table>

### 爐石戰記卡牌編碼（HSCI）－五碼範例

- #00208：中立（All）的精良（Rare）卡，編號**08**。
- #01308：德魯伊（Druid）專屬的史詩（Epic）卡，編號**08**。

# HSCI in JSON（hsci.json）

用一個 JSON 檔把所有的卡牌通通包含在裡面，這麼做使用卡牌資料容易維護、修改，而且轉換至其他格式也不困難。

JSON 格式彈性大，因此，決定使用 [JSON Schema] 定義 hsci.json 的語法。透過統一的規範，減少未來片牌編碼的歧異。

---Planning---

> 我有三張手牌，牌堆的十張牌裡，有四張法術牌（2費*2, 3費*1, 5費*1）、三張手下（損人、補血、嘲諷）、一張炸雞勇者、一張嘲諷、

不少人抱怨官方不提供卡牌


- HearthStone Web Service
  - hsci.bz (HearthStone Card Index.Blizzard)
  - Card API
- 算牌
- AI
- Replay
- How to capture/describe **moves** made by player?



[爐石戰記]:http://bit.ly/1juKf00
[爐石戰記透視鏡]:http://bit.ly/1juKdVH
[JSON Schema]:http://json-schema.org/
