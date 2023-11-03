import requests
import json
import random
import time


def get_context():
    context_list = [
        "&mine",
        "&eat salmon 2"
    ]
    # text = random.choice(context_list)
    text = context_list[0]

    return text


def chat(chanel_list,authorization_list):
    for authorization in authorization_list:
        header = {
            "Authorization": authorization,
            "Content-Type": "application/json",
            "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36",
        }
        for chanel_id in chanel_list:
            msg = {
                "content": get_context(),
                "nonce": "82329451214{}33232234".format(random.randrange(0, 1000)),
                "tts": False,
            }
            url = "https://discord.com/api/v9/channels/{}/messages".format(chanel_id)
            try:
                res = requests.post(url=url, headers=header, data=json.dumps(msg))
                print(res.content)
            except:
                pass
            continue
        time.sleep(random.randrange(1, 3))


if __name__ == "__main__":
    chanel_list = ["997788347806269534"]
    authorization_list = ["OTk3Nzg3MDIzNjUxOTE3ODU1.GLOE07.-5murqsDVuH2JKr7Xy0syX_4OKFPLwtWIz7X-4"]
    while True:
        try:
            chat(chanel_list,authorization_list)
            # sleeptime = random.randrange(10, 30)
            sleeptime = 60
            time.sleep(sleeptime)
        except:
            break
