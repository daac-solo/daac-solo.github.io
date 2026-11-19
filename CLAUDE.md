# daac-solo.github.io

个人网站。内容不是在这里写的——`data/` 下的文件由 Signal Flow 的
`push-website.ts` 从 Obsidian vault 同步过来。**不要手改 `data/` 里的任何
文件**，下一次同步会覆盖掉。

## 配色：南山 / 夜山

`brand/tokens.css` 是这个站的配色，它**不是在这里维护的**——它由
`push-website.ts` 从 `signal-flow/brand/tokens.css` 推过来，是我所有产品
共用的同一份。在这个仓库里改它没有意义，下次同步会盖掉。

页面只用 `var(--…)`，不要写死颜色：

```
南山(浅)  --bg #f9f9f8  --paper #fdfdfc  --fg #1d3e56  --muted #63635e
          --accent #00749e  --alarm #c0481f
夜山(深)  --bg #111113  --paper #b9b6af  --fg #eeeeec  --muted #b0b4ba
          --accent #75c7f0  --alarm #ff9478
圆角 11px   缓动 cubic-bezier(.2,0,0,1)   字号只有 11 / 13 / 17
```

规则，违反了算 bug：

1. 只用 tokens 里的值。不在里面的颜色就是不存在。
2. 一页三种字号，数出来的。
3. 不用「·」做分隔符。
4. 界面上不写解释性的句子。
5. **对比度是量出来的，不是看出来的。** 两套主题都要量。
6. 0.5px 发丝线（2dppx 下）。

`--paper` 是纸的颜色，不是背景的颜色。深色下它是浅的（`#b9b6af`，暗房间里
的一张真纸）。从 `--bg` 推它，纸质元素会变成黑的。

## 这个站现在的样子

深色、胶片颗粒、自定义光标、Lora 衬线。**质感保留**——颗粒和光标是材质不是
颜色。要换的只是色值：原来那套自己的暖金（`#c4a882`）换成夜山的 `--accent`，
并且补上南山的浅色主题。

完整的来由在 signal-flow 的 `brand/BRAND.md`。
