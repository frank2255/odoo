# odoo當發票開立後，發送訊息到 slack channel(先固定 channel 即可)

發送訊息的按鈕<br/><br/>
![image](https://github.com/user-attachments/assets/76517587-60b9-4f51-b818-70c477762902)<br/><br/>

並對以下位置的account_move_send做添加<br/><br/>
位置: src/odoo/addons/account/wizard/account_move_send.py<br/><br/>

![image](https://github.com/user-attachments/assets/c665067d-ecbe-466c-b442-3f899c4e752f)<br/><br/>

使用from slack_sdk import WebClient 及 from slack_sdk.errors import SlackApiError <br/><br/>
需要環境安裝 pip install slack-sdk<br/><br/>
在此終端輸入<br/><br/>
![image](https://github.com/user-attachments/assets/399f3cae-a033-4e0f-a287-851b1b7fe076)<br/><br/>
![image](https://github.com/user-attachments/assets/9b8747ac-8331-436d-be6c-c9e64d2feb8d)<br/><br/>

對account_move_send.py d9 開頭添加的code<br/><br/>
![image](https://github.com/user-attachments/assets/25fde662-51dc-4e89-81a9-8c8a9a19e5c1)<br/><br/>
在方法action_send_and_print添加code<br/><br/>
![image](https://github.com/user-attachments/assets/d9620410-092b-4d7f-bd4e-941da3c9b093)<br/><br/>

存account_move_send.py後,點按鈕"發送與列印"成功對slack發送訊息<br/><br/>
![image](https://github.com/user-attachments/assets/0148c68d-f2f0-42a4-86b8-493ce03b276c)<br/><br/>
