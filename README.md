# 在odoo建立新的branch<br/>
點選上方的build<br/><br/>
![image](https://github.com/user-attachments/assets/bacbc30b-5ca5-48b9-a33b-a4e72a09b0c8)<br/><br/>
並選其中的branch -> 點選rebuild<br/><br/>
![image](https://github.com/user-attachments/assets/8893bfea-6a55-477a-bc5c-1f5080013c08)<br/><br/>
建立成功後就能connect<br/><br/>
![image](https://github.com/user-attachments/assets/f2caf24e-cdda-4e6f-ab5b-fdd1602fdf6c)<br/><br/>



odoo當發票開立後，發送訊息到 slack channel(先固定 channel 即可)

import logging
import os
# Import WebClient from Python SDK (github.com/slackapi/python-slack-sdk)
from slack_sdk import WebClient
from slack_sdk.errors import SlackApiError

# Slack API 呼叫
client = WebClient(token="xoxb開頭的token")
logger = logging.getLogger(__name__)
channel_id = "頻道識別碼"  # 目標頻道 ID

try:
    # 發送 Slack 訊息
    slack_message = f"Account Move has been sent and printed."
    result = client.chat_postMessage(
        channel=channel_id,
        text=slack_message
    )
    logger.info(result)

except SlackApiError as e:
    logger.error(f"Error posting Slack message: {e}")

