只要輸入年月日，就可以轉換成`年柱`,`月柱`,`日柱`,`時柱`,`農曆月`,`農曆日`,`節氣`,`星期`的資訊  
# 命理基本的查詢
![npm](https://img.shields.io/npm/v/@tony801015/chinese-lunar)
![npm](https://img.shields.io/npm/dm/@tony801015/chinese-lunar)

近期會頻繁的更新，但整體的架構未來會劃分為三個 `BasicLunar`、`AdvancedLunar`、 `ApplicationLunar` 可以依照你的需求去使用唷。

使用範例如下:
```
npm i @tony801015/chinese-lunar -S
```

```js
const { BasicLunar, AdvancedLunar, ApplicationLunar } = require('@tony801015/chinese-lunar');

const Lunar = new BasicLunar('2021', '02', '13');

// BasicLunar
console.log(Lunar.year, Lunar.month, Lunar.day); // 2020 03 05
console.log(`${Lunar.chineseYear}/${Lunar.chineseMonth}/${Lunar.chineseDay}`); // 庚子/己卯/丁未
console.log(`${Lunar.lunarMonth}/${Lunar.lunarDay}`); // 二月/十二
console.log(`${Lunar.solarTerms}`); // 驚蟄
console.log(`${Lunar.week}`); // 4
console.log(`${Lunar.chineseTime}`); // 庚子,辛丑,壬寅,癸卯,甲辰,乙巳,丙午,丁未,戊申,己酉,庚戌,辛亥

// AdvancedLunar 時間的十神, 登貴
console.log(`${Lunar.chineseTimeTenGod}`); // ㄗ,印,比,劫,食,傷,才,財,殺,官,ㄗ,印
console.log(`${Lunar.dengGui}`); // 申午

// ApplicationLunar
```

設定檔 `config.js` 裡面有一些整理過的資訊，希望可以幫助到大家對於命理上的研究。歡迎大家找我討論～

注意:目前計算的時間以1956年開始至2050年，1956以前的都無法計算。

未來會再增加 ~~時柱~~,`生肖`,`星座`等等作轉換
