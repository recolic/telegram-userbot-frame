# Naive framework to create your telegram user-bot easily

## How to create your userbot

Easy. Just create `modules/mod_your_toy.py` and enjoy:

```python
def handle_msg_txt(tg, chat_id, sender_id, msg_id, is_outgoing, message_text):
    print(f"[example_mod] handle_msg_txt: chat={chat_id} sender={sender_id} msg={msg_id} is_outgoing={is_outgoing} text={message_text!r}")
    if not is_outgoing:
        tg.send_message(chat_id=chat_id, text="Hey I just got your message!")
    return False
```

For more details, refer to our doc [modules/mod_example.py](modules/mod_example.py) and examples [./mod_examples](./mod_examples).

## How to install and run

You need a Linux/MacOS device, and then install **python3 and python-telegram** on it. For example, if you are using ubuntu, you should run this:

```
sudo apt install python3 python3-pip
sudo pip3 install python-telegram
```

And then copy the `watchdog.py` onto your device. Modify the following lines at the top of the file. Refer to [Telegram Official Document](https://core.telegram.org/api/obtaining_api_id#obtaining-api-id) about how to get `api_id` and `api_hash`.

```
YOUR_QUESTION = 'Your verification question here'
YOUR_ANSWER = 'Your expected answer here'
TELEGRAM_API_ID = 'Change This!'
TELEGRAM_API_HASH = 'Change This!'
TELEGRAM_PHONE = 'Phone number of your telegram account'
```

Now you just need to run the modified `watchdog.py` 24 hours a day. Note that you need to input the SMS code on the first login.
