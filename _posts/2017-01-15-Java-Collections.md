---
layout: post
title: Java Collections
subtitle: 
---

## Overview
 - List: 順序通りに並べて格納(中身の重複OK)

 - Set: 順序がバラバラ(中身の重複OUT)

- Map: ペアで対応づけて格納
 
### ArrayList
 
要素を格納する:
 
| return  | method     | meaning                       |
|---------|------------|-------------------------------|
| boolean | add(~)     | リストの最後に要素を追加      |
| void    | add(int,~) | リストのint番目に要素を挿入   |
| ~       | set(int,~) | リストのint番目の要素を上書き |

要素を取り出す:

| return   | method   | meaning                 |
|----------|----------|-------------------------|
| boolean~ | get(int) | int番目の要素を取り出す |

リストを調査する:

| return  | method      | meaning                      |
|---------|-------------|------------------------------|
| int     | size()      | 格納されている要素数を返す   |
| boolean | isEmpty()   | 要素数がゼロであるか判定     |
| boolean | contains(~) | 指定要素が含まれているか判定 |
| int     | indexOf(~)  | 指定要素が何番目にあるか検索 |

イテレータを返す:

| return      | method     | meaning                            |
|-------------|------------|------------------------------------|
| Iterator<~> | iterator() | 要素を順に処理するイテレータを返す |

要素を削除する:

| return | method      | meaning                 |
|--------|-------------|-------------------------|
| void   | clear()     | 要素を全て削除する      |
| ~      | remove(int) | int番目の要素を削除する |


```java
Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++){
            arr[i] = sc.nextInt();
        }
        
        int numNegative = 0;
        for(int j=0; j<n; j++){
            int temp = 0;
            for(int k=j; k<n; k++){
                temp = temp + arr[k];
                if(temp<0){
                    numNegative ++;
                }
            }
        }
        System.out.print(numNegative);
```
