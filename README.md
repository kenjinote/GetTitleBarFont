# GetTitleBarFont
get title bar font

下記の3行でタイトルバーのフォントは取得できます。

```
LOGFONTW lf = {};
SystemParametersInfoW(SPI_GETICONTITLELOGFONT, sizeof(LOGFONTW), &lf, 0);
SetWindowText(hEdit, lf.lfFaceName);
```

ちなみにWindows 11（日本語環境）のフォントは「Yu Gothic UI」でした。
