ファイルに定義した関呼び出し

```
Prelude> :l sec1/fn
[1 of 1] Compiling Main             ( sec1/fn.hs, interpreted ) [flags changed]
Ok, one module loaded.
*Main> doubleme 3
6
*Main> 
```

関数を追加して再読込 + 実行

```
*Main> :r
[1 of 1] Compiling Main             ( sec1/fn.hs, interpreted )
Ok, one module loaded.
*Main> doubleUs 3 4
14
*Main> 
```

if を使った関数

```
*Main> :r
[1 of 1] Compiling Main             ( sec1/fn.hs, interpreted )
Ok, one module loaded.
*Main> doubleSmallNumber 10
20
*Main> doubleSmallNumber 1000
1000
*Main> 
```

カッコと関数名にアポストロフィが使える

```
*Main> :r
[1 of 1] Compiling Main             ( sec1/fn.hs, interpreted )
Ok, one module loaded.
*Main> doubleSmallNumber' 10
21
*Main> doubleSmallNumber' 1000
1001
*Main>
```

リスト内包表記

```
*Main> boomBangs [1..15]
["BOOM!","BOOM!","BOOM!","BOOM!","BOOM!","BOOM!","BOOM!","BOOM!","BOOM!","BANG!","BANG!","BANG!","BANG!","BANG!","BANG!"]
```

問題

- 3辺はすべて整数
- 各辺の長さは 10 以下
- 周囲の長さは 24 に等しい

```
[(a,b,c) | c <- [1..10], b <- [1..c], a <- [1..b], a^2 + b^2 == c^2, a+b+c == 24]
```