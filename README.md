# OUC-beamer模板

编译后的效果请参考slide.pdf。如有建议或者bug请issue。欢迎使用。

使用编译方式：
``` javascript
"name": "xelatex",
"command": "xelatex",
"args": [
    "-synctex=1",
    "-interaction=nonstopmode",
    "-file-line-error",
    "-shell-escape",
    "%DOCFILE%"
],
```

两次xelatex，且需要-shell-escape参数。或者使用latexmk，也要开启-shell-escape参数。

linux或其他os请注意把
``` tex
% --- Font settings ---
% 设置中文字体
\setCJKmainfont{KaiTi}                          % 正文中文用楷体
\setCJKsansfont{KaiTi}                          % 无衬线字体也用楷体
\setCJKmonofont{SimSun-ExtB}                    % 等宽字体（win）SimSun-ExtB
\setmainfont{Times New Roman}                   % 英文统一用Times New Roman
\setsansfont{Times New Roman}                   % 英文无衬线也用Times New Roman
\setmonofont{Consolas}                          % 英文等宽字体用Consolas
（OUC.sty，line 34-39）中的字体换成你有的。默认为win
```

code类型里面不能有中文。
