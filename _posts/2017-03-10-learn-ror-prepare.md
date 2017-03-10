---
layout     : post
title      : "學習 Ruby on Rails - 環境配置"
subtitle   : "RoR 學習筆記 1"
date       : 2017-03-10 10:30
author     : "Martin Wu"
tags       : Rails RVM
#comments   : true
#signature  : true
---
記錄一下自學 RoR 的過程。

### 前期準備
缺什麼就裝什麼吧，使用 Mac OS 的話，記得先把 xcode 跟 homebrew 裝好，會比較方便。

#### 安裝 RVM
安裝 RVM 來管理 Ruby 版本跟 gem 套件，除了避免安裝一堆有的沒的 gem 弄亂系統，也不用每次都要輸入使用者密碼才能安裝套件。

```bash
$ \curl -sSL https://get.rvm.io | bash -s stable
```

懶得每次手動 `source ~/.profile` 可以加入下面設定到常用的 shell 設定檔 (~/.bashrc or ~/.zshrc)
```
export PATH="$PATH:$HOME/.rvm/bin"
```
嗯...現在好像會很機婆的自動幫你加到 .bashrc 跟 .zshrc，上一步就省了...

#### 使用方法
* 列出目前可以安裝的 Ruby 版本
```bash
$ rvm list known
```

* 安裝特定版本的Ruby
```bash
$ rvm install 2.1.1
```

* 秀出目前已安裝的版本
```bash
$ rvm list
```

* 切換版本
```bash
$ rvm use 2.1.1
```

* 設成預設版本
```bash
$ rvm 2.1.1 --default
```

#### 進階用法
* 建立 gemset 讓各個版本的 Rails，擁有自己的套件庫，例如
```bash
$ rvm gemset create r415
```

* 秀出目前的 gemset
```bash
$ rvm gemset list
```

* 切換 gemset
```bash
$ rvm gemset use r415
```

* 刪除已安裝的 gemset
```bash
$ rvm gemset empty r415
```  

#### 安裝 Rails
```bash
$ gem install rails  --no-rdoc --no-ri
```

也可以指定安裝的版本，例如
```bash
$ gem install rails -v='4.1.5' --no-rdoc --no-ri
```

懶得每次都輸入 `--no-rdoc --no-ri`，可以新增一個 `~/.gemrc` 到使用者目錄，檔案內容如下，預設就不產生文件
```
gem: --no-ri --no-rdoc
```

### 參考
* ihower - [Ruby on Rails 實戰聖經](https://ihower.tw/rails/installation.html)
* 高見龍 - [RVM and Gemsets](http://kaochenlong.com/2011/04/08/rvm-and-gemsets)
* JokerCatz - [RVM安裝與使用教學](http://railsfun.tw/t/rvm/28)
