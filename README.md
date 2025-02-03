# README

***psterm*** 是一個基於 ***iterm2*** 的終端機主題，用於美化介面、方便使用者更直覺的使用 `Git` (將狀態等直接顯示於終端機畫面)。***psterm*** 以 ***iterm2*** 為基底，輔以個人使用 `Shell language` 的邏輯與習慣，以此發展為 ***psterm***。相關資料與筆記整理在下方，是 ***psterm*** 的標準。

目前有兩個版本: ***psterm*** 與 ***pstermd***。兩者類型(type)都一樣。相關差異表格如下:

- Type
  1. path + Git
  2. (root) + text
- Style
  |版本|***psterm***|***pstermd***|
  |-|-|-|
  |樣式|plain|diamond|
  |圖示|text|semi-triangle|

`Git` 相關概念是採用 *Pro Git 2nd by Scott Chacon and Ben Straub*，而此書我也有整理其重要概念與常用指令的筆記，筆記內容同時 Oh My Posh 渲染 `Git` 的標準

## Oh My Posh

- 中英文對照(僅供參考)
  - Block 區塊
  - Segment 模組
  - type 類型
  - style 樣式
  - symbol 圖示
  - template 模板
- Oh My Posh Structure
  - Block
  - Segment
    - type
    - style
      - symbol
    - template
- Style
  - powerline
    > 標準樣式，具有背景和文字顏色，模組會將上一個的末端圖示作為首端圖示
  - plain
    > 背景透明的純文字樣式，沒有背景色
  - diamond
    > 在模組的左右兩端可自定義不同的圖示
- Git
  |區域|狀態|符號|
  |-|-|-|
  |Working Tree|untracked|`?`|
  ||modified|`~`|
  ||deleted|`-`|
  |Staging Area|new file|`+`|
  ||modified|`~`|
  ||deleted|`-`|
- Nerd Font icons
  -  \ue0b0
  -  \ue0b2

## Git

### 狀態

- Working Tree
  - Unmodified: #00909a
  - Modified: #cd9f00
- Staging Area
  - Staged: #f44d27

### 工作流程

1. Modified 與 Staged 同時存在時，會以 `|` 隔開，且顏色顯示為 #f44d27 (Staged)，另外 ***psterm*** 的圖示以縮寫(M、S)來代表檔案的兩大類狀態(Modified、Staged)的變動，而非 ***iterm2*** 的圖示
2. 模板邏輯為: HEAD + Modified + Staged
   > `master M?1 ~1 -1 | S+1 ~1 -1`

## References

- Oh My Posh
  - [Segments](https://ohmyposh.dev/docs/configuration/segment)
  - [Themes](https://ohmyposh.dev/docs/themes)
  - [Nerd Font icons](https://www.nerdfonts.com/cheat-sheet)
- Git
  - [Git顏色定義](https://git-scm.com/book/zh-tw/v2/%e9%96%8b%e5%a7%8b-Git-%e5%9f%ba%e7%a4%8e%e8%a6%81%e9%bb%9e)
