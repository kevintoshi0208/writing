#[框架簡介]Symfony

## 什麼是Symfony?
對於有使用Laravel開發過的工程師來說，想必對Symfony這個名詞應該不陌生，在安裝和開發的過程中，都會看到這個名詞。
那麼什麼是Symfony呢?
看看官網的定義:

> Symfony is a set of PHP Components, a Web Application framework, a Philosophy, and a Community-all working together in harmony.
> Symfony 是 一套php的組件，一個框架，一個哲學，一個社群- 這些元素一起和諧的運作

簡單來說，Symfony是一套可重用獨立的PHP組件
除了可用這些套件來解決web開發問題以外
也可以選擇Symfony Framework 一套全栈式的php框架 來開發
或甚至用Symfony來建立一套屬於自己的框架

## Symfony 背景

Symfony背後是一間法國公司：SensioLabs。它創建於12年前，是個web專案開發商，擁有各領域的代表客戶。
受到了Spring Framework的啟發， 為了加速Web應用程序的創建和維護，和取代重複的編碼任務，以及能為企業提供健壯的應用程序，SensioLabs公司開啟了Symfony的專案，並以MIT License開源發布。
為了滿足SensioLabs自身需求，Symfony框架至今仍是其團隊用於開發客戶系統的日常工具。自推出以来，Symfony周圍也出現了一個完整的生態系統與共同使用和維運的社群。

## Symfony 特性

### 高擴展 高覆用

Symfony從最小的brick到完整的kernel，每樣東西都是以plugin方式來呈現。
每個組件意在為框架增加功能性，每個組件也可以覆用在其他項目中，被整個社群所共享。
Symfony其低耦合，高內聚的特性，包括console，http-foundation，security，finder，每一項組件都可以被獨立的安裝與運用。
核心為了每一個Component設計了Interface，使其可以隨時被修改，而不需要重新的配置部署。

### 高靈活

> Everything for change。
> 皆應萬變

Symfony是為了因應改變而生，甚至包括框架核心本身都開放改變與替換，其組件皆互相獨立，使用不同的介面相互溝通。
除此之外不同需求也可以選擇不同的開發方案。
你可以使用完整的Framework套件，也可以根據你的需求去選擇你要特定的組件，甚至你可以只應用某一小塊的部分在你現有的專案中。

### 長久與穩定的支援

Symfony是由SensioLabs所支援的專案，每一個穩定版本都有長達三年的維護，針對安全性問題更幾乎永久保固。

### Symfony 技術與模式

#### Annotation

Symfony的各項設定可以使用annotation,yml,xml,php等方式。
不過由Spring Framework啟發，Symfony最推薦的模式仍是annotaion。
Annotation有助於開發上的方便以及更易於維護。
將Config和Code結合 提供了易開發 易維護的特性。
(能把Config寫在Code裡面 ， 好用!)
Doctrine(ORM) - Repository Pattern And Unit Of Work
Doctrine 支援了近乎所有RMDBS類型的資料庫(Mysql,MSSQL,Oracle,MariaDB,PostgreSQL,SAP Sybase,SQLite)
不同於其他框架的MVC，在早期便採用了Repository Pattern,Unit Of Work等模式，以應付大型的專案。
相較於傳統的MVC中的Model容易擁腫
有遠見的使用了Repository Pattern
這種模式將Model分開為 Entity,Repository,UnitOfWork
降低資料實體 和 查詢 和 資料異動的耦合度 以因應需求的替換
其EntityManger物件 也大量的簡化流程 與 增強ORM的功能

#### Dependency Injection(Service Container)

Symfony預設使用了IoC的概念，將所有組件 包在Container中，以依賴注入的方式降低各組件的耦合度，在架構面達成易於替換的效果。

#### Event Dispatcher

做為一個優秀的框架，中介層是不可少的，Symfony使用了Event Listener的概念，能在每一個動作節點都加入不同的event，不管你要在Request,Response,Controller,Validate 等之類的動作前後都可以加入不同的event 執行。

#### Form Component

Symfony提供了Form Component來處理大部分的Request
除了基本Csrf防護之外
只要事先建立好物件就能自動配合twig的生成html
request發出後能validate所有欄位
還能能將欄位的mapping到entity
甚至能自動mapping操作複雜的OneToMany,ManyToMany等關聯
大大減少了工程師平常處理複雜關聯的難度

#### PHPUnit Bridge

為單元測試和整合測試而生的Component

#### Debug Component

強大的Debug Profile，提個各種資訊，以進行各個模組的偵錯。

#### 其他基本模組

近乎支援 所有近代Framework 該支援的項目
使用了Symfony的項目
著名的Joomla,Drupal,Laravel,Behat
多多少少都使用Symfony Support的組件

### 學習資源與文件

#### SymfonyCast
前端(js,es6,webpack,react),
後端(symfony,api,testing,oath2,jwt)
devOp(ansible) 應有盡有

#### Symfony Document

### 結論

Symfony Framework或許因其稍微複雜的架構和理念，增加了上手難度，而在普及度上不如Laravel。
但我認為在上手後的開發速度,可維護性,開源貢獻上 Symfony還是比較優。
若你也正為了用php組織大型應用的架構和維護面煩惱，不妨考慮試試Symfony吧。