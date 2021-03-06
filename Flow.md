# 控制流程 #
一個 Python 程式碼的執行流程是由上而下，一行接著一行執行，本章節將介紹如何在 Python 程式中，利用\_條件判斷式\_及\_迴圈\_來改變程式碼的執行流程。


# 條件判斷 #

## if 關鍵字 ##

若想要根據一些條件判斷改變程式碼執行的流程，可以運用 `if` 關鍵字，以下列程式碼為例：
```
x = input('Please enter a integer: ')
if x > 0:
    print 'You have entered a positive integer.'
```
程式執行後，會等待操作者輸入一個整數，若是這個整數數值大於 **0** ，程式才會印出 `You have entered a positive integer.` 的文字。

這裡我們使用了 `if` 這個關鍵字，在 `if` 之後緊接著就是條件的判斷式（`x > 0`），每一個條件判斷式會以 `True` 或 `False` 作為判斷的結果，而只有當結果為 `True` 時，才會執行內部區塊（block）的程式碼。內部區塊是以條件判斷式後的 `:` 開始，同一層縮排的程式碼才視為是同一個區塊。

> | 一般程式語言都是以 `{` 及 `}` 標記程式碼區塊，Python 則是使用程式碼的縮排來表示。雖然縮排可以使用空白字元或是 tab 鍵，不過為了一致性及不同編輯器間的閱讀性，建議使用 **4個空白字元** 作為縮排的標準 |
|:-----------------------------------------------------------------------------------------------------------------|

試試看下列程式碼，若 `x` 及 `y` 放入不同的數值，程式碼會輸出什麼：
```
x = 5
y = 15
if x > 0:
    if y < 20:
        print 'x > 0 and y < 20'
```

## if-else 子句 ##

當程式碼需要條件判斷時，也許不只要處理條件成立（結果為 `True`）時的狀況，如果有這樣的需要，可以在使用 `if` 語法時，搭配 `else` 關鍵字：
```
x = input('Please input an integer: ')
if x > 10:
    print 'x is greater than 10'
else:
    print 'x is not greater than 10'
```
此時，當 `x > 10` 的結果為 `False` 時，程式則會印出 `x is not greater than 10` 的文字。

而當判斷的條件不只一個的時候，可以再加上 `elif` 來使用：
```
x = input('Please input an integer: ')
if x > 0:
    print 'Positive'
elif x == 0:
    print 'Zero'
else:
    print 'Negative'
```