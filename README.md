# Work Station Rule

## Server使用規範

表單網址: https://reurl.cc/8q3EQj

1. 借用server前, 請先確定表單有無登記
2. 無法臨時自行借用，請勿占用 GPU 資源，須先登記 (會被 Shutdown )
3. 所有資料放在自己的家目錄(`/mnt/data0/<user-name>`)
4. 一個帳號不得超過 100 G (SSD)

Note:
1. 借用後請先確認表單有無登記到
2. cuda 目前支援 11.4

## 連線至工作站

如需申請帳號，請尋找對應工作站的管理員  

### 各工作站的IP

| Name |  IP   | Port  |
| :----: | ---- | ---- |
| 3090 Server | 140.113.228.124 | 10101 |
| 2080 Tis Server | 140.113.228.124 | 10102 |

## 常用指令

### 更改登入預設的shell設定


```bash
chsh -s /bin/bash
```

### 查看目前GPU的使用狀況

```bash
nvtop
```

### 使用特定GPU運行程式

```bash
CUDA_VISIBLE_DEVICES=<GPU_NUM> python <file_name>.py

# example: use 3-th GPU to perform training
CUDA_VISIBLE_DEVICES=3 python train.py

# example: use 3, 4, 5 three cards to perform training  
CUDA_VISIBLE_DEVICES=3,4,5 python train.py  
```
