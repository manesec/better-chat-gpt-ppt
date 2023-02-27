# better-chat-gpt-ppt

This is one of the version fork on [williamfzc/chat-gpt-ppt](https://github.com/williamfzc/chat-gpt-ppt), improved by [@manesec](https://github.com/manesec).

+ Update new version of [ChatGPT](https://github.com/acheong08/ChatGPT).
+ More info message.


## Better note

Presetup:

```bash
sudo pip3 install chat_gpt_ppt
git clone https://github.com/manesec/better-chat-gpt-ppt.git
cd better-chat-gpt-ppt
sudo python3 setup.py install -f

# install marp
wget https://github.com/marp-team/marp-cli/releases/download/v2.2.2/marp-cli-v2.2.2-linux.tar.gz -O /tmp/marp.tar.gz
cd /tmp 
tar -xf /tmp/marp.tar.gz
sudo mv /tmp/marp /bin/marp
cd -
```

## To support `*.pptx`, `.pptx` file just image like screenshot :( 
**Recommand to use `.pdf` to output.**

A lazy way to install google chrome faster.

If you like to output `*.pptx` files.

```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google*.deb
sudo apt --fix-broken install -y
sudo dpkg -i google*.deb
```

Usage:
```bash
# With html output
cgp token.txt topic.txt -m /bin/marp -o output.html

# With pdf output (recommand)
cgp token.txt topic.txt -m /bin/marp -o output.pdf

# With pptx output 
cgp token.txt topic.txt -m /bin/marp -o output.pptx
```

# chat-gpt-ppt

use ChatGPT to generate PPT automatically

> [2023-01-13] https://github.com/williamfzc/chat-gpt-ppt/issues/2 OpenAI's services are not available in my country.
>
> [2022-12-06] Currently ChatGPT has no official API. I am waiting for it to make this repo a real production.

## Show case

Some topics for presentation named `topics.txt`:

```
what's OpenAI?
how OpenAI works?
what is the future of OpenAI?
```

Easily generate a simple ppt in seconds:

```
cgp token.txt topics.txt
```

And you get a slice:

```
[  INFO ] Converting 1 markdown...
[  INFO ] C:\Users\ADMINI~1\AppData\Local\Temp\tmpt202812s => output.html
2022-12-05 16:08:24.154 | INFO     | cgp:main:82 - result saved to output.html
```

![](./example/sample.png)

And multi languages:

![](./example/sample-chi.png)

## Usage

### Install lib

```python
pip3 install chat_gpt_ppt
```

### Get your session token

https://github.com/acheong08/ChatGPT#get-your-session-token

### Install marp

Currently we use [marp](https://github.com/marp-team/marp-cli/releases/tag/v2.2.2) as our ppt renderer.
You can easily download it via the link above.

### Run

```
cgp token.txt data.txt --marp_exe /your/marp/exe/path
```

## Contribution

This is a toy project.
Feel free to hack. Only < 100 lines python code.

## License

MIT
