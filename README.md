# Server使用規範
表單網址: https://reurl.cc/QWRxL9
1. 借用server前, 先確定表單有無登記
2. 無法臨時自行借用，須先登記 (會被Shutdown)
3. 所有資料放在自己的家目錄(/mnt/data0/user)
4. 一個帳號不得超過 100 G (SSD)

Note:
1. 借用後請先確認表單有無登記到
2. cuda 目前支援 11.4

# 連線至工作站
如需申請帳號，請尋找對應工作站的管理員  
### 各工作站的IP
IP: 140.113.228.124(兩張卡的IP都一樣)  
Port:   
NVIDIA GeForce RTX 2080 Ti: 10102  
NVIDIA GeForce RTX 3090: 10101  

# 常用指令
### 更改登入預設的shell設定
chsh -s /bin/bash  
### 查看目前GPU的使用狀況
nvtop  
### 使用特定GPU運行程式
CUDA_VISIBLE_DEVICES=<GPU_NUM> python <file_name>.py  
舉例: CUDA_VISIBLE_DEVICES=3 python train.py  
