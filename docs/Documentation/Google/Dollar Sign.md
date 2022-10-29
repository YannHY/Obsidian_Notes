---
tags: [Documentation, Google, Sheets]
author: [Arch]
date: 13-06-2022
---

When used in formulas, dollar symbols indicate to Google Sheets that the next number or letter to the right of it should remain static. Even when copy pasted, any value without the symbol will increment, and those with it will not. As an example, the formula `=$A1*B$1` copy pasted to cell `D2` will not increment `A` in `A1`, or `1` in `B1`. The resulting formula would be `=$A2*C$1`. As long as there is a `$` before it, that number or letter will not change when pasted into another cell. All other values will increment in the series.

[Link](https://www.techjunkie.com/google-sheets-dollar-sign-meaning/)