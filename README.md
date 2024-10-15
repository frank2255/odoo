# odoo當發票開立後，發送訊息到 slack channel(先固定 channel 即可)

發送訊息的按鈕<br/>
![image](https://github.com/user-attachments/assets/76517587-60b9-4f51-b818-70c477762902)

並對以下位置的account_move_send做添加
src/odoo/addons/account/wizard/account_move_send.py
