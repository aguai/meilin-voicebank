## 更新紀錄
   * 01/15/2013更新，上傳20140115版。

## 目標
  * 本計畫是作能唱華語（台灣風格）與日語的虛擬歌手，徵音梅林。
  * Purpose of the project is to make a virtual singer "Linne" which can sing Mardarin(Taiwanese accent) and Japanese.

## 檔案說明
  * tar.gz請用  " tar xvf 檔名 " 解開（其他平台請使用可以用的解壓縮軟體來解）
  * voicebank裡面的聲波檔都是無損壓縮的flac，在解開的目錄下，複製貼上執行下面這一行，就可以還原成原來的wav檔

```sh
for i in *.flac ; do flac -d $i ; done;rm *.flac
```

## voicebank
  * 標題為Voicebank的壓縮檔裡面裝的是16bit 44100hz單音的聲波取樣，這是給EFB-GW引擎來使用的。
  * Voicebank is filled with  16 bit 44100hz mono wave sample files. Used by EFB-GW.

## voicebank-src
  * 標題為Voicebank的壓縮檔裡面裝的是當初在專業錄音工作室錄的原始檔，檔案格式是24bit 48000hz的單聲道聲波取樣。
  * Voicebank-src is the original source recorded in professional studio. Sample files are 24bit 48000hz mono wave sample fles.

## csv
 * 所有錄音的列表。**output.csv**是```華語```的，**output_japanese.csv**是```日語```的，others是其他項目或者將來增補的。檔案內的項目格式是：
 * 該語文方便人看的音標（注音或者假名）,IPA標示,檔名
 * 第一項是為了方便一般人閱讀，其中由於音標有時並不能真實記載實際的語音的變體，例如「**ㄇㄛ**」這個單獨音，「**麼**」跟「**魔**」注音一模一樣，但是實際發音不同，記載上，我們會加上大寫英文的後綴來編碼表示，標示為A的，會選擇日常生活最常用的那一個。
 * IPA標示則是程式運算的邏輯
 * 檔名是為了跨系統平台，各種編碼系統可以正確顯示而設定，所以編成ASCII，編輯的邏輯使用語言標音的羅馬拼音。
 * 華語首字使用小寫，日語使用首字使用大寫
