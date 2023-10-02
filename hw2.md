# 甘特圖
### Mermaid
```mermaid
gantt
    title Mission Time

    section 1
    研礙計畫           :a1, 2023-10-02, 1d
    section 2
    任務分配     :after a1  , 4d
    section 3
    取得硬體     :after a1  , 17d
    section 4
    程式開發      :a4, 2023-10-7  , 70d
    section 5
    安裝硬體     :a5, after a4   ,10d
    section 6
    程式測試    :a6, after a4   ,4d
    section 7
    撰寫使用手冊    :a7, after a5 ,25d
    section 8
    轉換檔案     :after a5  , 20d
    section 9
    系統測試     :a9,after a6 , 25d
    section 10
    使用者訓練     :a10, after a7 and a8 , 20d
    section 11
    使用者測試     :after a9 and a10 , 25d
 



```


```
# PERT 圖
```graphviz
digraph {
node[shape=record];
rankdir="LR";
    no1 [label = "研擬計畫 | 編號:1 | 開始:第1天 | 結束:第1天 | 需時:1天"]
    no2 [label = "任務分配 | 編號:2 | 開始:第2天 | 結束:第:6天 | 需時:4天"]
    no3 [label = "取得硬體 | 編號:3 | 開始:第2天 | 結束:第19天 | 需時:17天"]
    no4 [label = "程式開發 | 編號:4 | 開始:第3天 | 結束:第73天 | 需時:70天"]
    no5 [label = "安裝硬體 | 編號:5 | 開始:第4天 | 結束:第14天 | 需時:10天"]
no6 [label = "程式測試 | 編號:6 | 開始:第5天 | 結束:第35天 | 需時:30天"]
no7 [label = "撰寫使用手冊 | 編號:7 | 開始:第6天 | 結束:第31天 | 需時:25天"]
no8 [label = "轉換檔案 | 編號:8 | 開始:第6天 | 結束:第26天 | 需時:20天"]
no9 [label = "系統測試 | 編號:9 | 開始:第7天 | 結束:第32天 | 需時:25天"]
no10 [label = "使用者訓練 | 編號:10 | 開始:第8天 | 結束:第28天 | 需時:20天"]
no11 [label = "使用者測試 | 編號:11 | 開始:第10天 | 結束:第35天 | 需時:25天"]
    no1->no2
    no1->no3
    no2->no4
    no3->no4
    no4->no5
    no4->no6
    no6->no7
    no6->no8
    no7->no10
    no5->no6
    no8->no9
    no10->no9
    no9->no11
}
```
```

```
# 關鍵路徑
關鍵路徑:1->2->4->6->9->11
