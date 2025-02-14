 
### Single Command install | BETA 
i will release the final version soon!
just copy and run and send tokens when it ask for them :

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Diana-Cl/CFW-BOT/refs/heads/main/install.sh)"
```

### LAZY INSTALL
1. Register for a free account on [PythonAnywhere](https://www.pythonanywhere.com).
2. Obtain the required API keys:
   - Telegram Bot token from BotFather
   - Cloudflare API key from Cloudflare dashboard (make sure to select "Edit Cloudflare Workers template" and grant necessary permissions, all of them should have EDIT permission)
   - Telegram UserID you can obtain it from here https://t.me/useridinfobot or any similar bot you know
   - Cloudflare Account id, you can find it from right side of overview page or worker page in cloudflare
4. in your Dashboard section Select Files and and Click on "Open Bash Console Here"
5.  Clone this repository:

```bash
 git clone https://github.com/NiREvil/CFW-BOT.git
```

6. Navigate to the project directory:

 ```bash
 cd CFW-BOT
 ```

7. Make `requirement.sh` executable:
 ```bash
 chmod +x requirement.sh
 ```

8. Run `requirement.sh`:
 ```bash
 ./requirement.sh
 ```

"If you encounter errors running requirement.sh on PythonAnywhere , simply close the console (using `exit` command) , go to file manager and open it and  save it (use `ctrl+s` ) without changing any thing. thats it! now you can run it"
another solution is converting it using dos2unix 
since PythonAnyWhere does not support that you can use this simple python code 'dos2unix.py'
you can run this to solve the issue:

```bash
 python3 dos2unix.py
 ```

10. Run `install.py` and provide the required API tokens when prompted:
 ```bash
 python3 install.py
 ```

11. Start the bot:
 ```bash
 python3 cfw.py
 ```

### ADVANCED INSTALL

1. install requirements:
 ```bash
 pip install telebot
 pip install pytelegrambotapi --upgrade
 pip install qrcode[pil]
 pip install requests
 pip install python-dotenv
 ```

2. install NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

3. set nvm settings
``` bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads NVM
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads NVM bash completion
```
4. start nvm and install wrangler
```bash
nvm install 16.17.0
nvm use 16.17.0
npm install wrangler@latest
npx wrangler --version
```
5. set .env file variables


| Variable             | Description                                            |
|----------------------|--------------------------------------------------------|
| CLOUDFLARE_API_TOKEN | Cloudflare API token with Worker edit permission       |
| BOT_TOKEN            | Telegram bot token obtained from BotFather             |
| ACCOUNT_ID           | Cloudflare account ID                                  |
| ADMIN_USER_ID        | Numeric Telegram user ID for admin authentication      |
| IP_API               | use this as refrence https://raw.githubusercontent.com/NiREvil/CFW-BOT/main/ips.txt|

6.remember to set cloudflare account id in workertemp.txt 


### How To Use the Bot
At this stage, you have two options for entering the IP address in the CFW-BOT:

1- Using a Cloudflare clean IP: This type of IP will make you have good download speed and ping, but sites that use Cloudflare's CDN will not load for you. The method of finding a clean IP is explained here. [link to article](https://github.com/NiREvil/CFW-BOT/blob/main/CFW_Worker_Sub.md)

2- Using a proxyIP: This type of IP may have about ten percent lower speed compared to Cloudflare IP's, and it may be filtered after one or two months, forcing you to change it. However, the advantage is that all sites, even those behind Cloudflare, open easily and without problems. I have written here an easy and fast way to find proxyIP. [link to article](https://github.com/NiREvil/vless/blob/main/sub/ProxyIP.md)


### Note
This bot is designed to be lightweight and inexpensive to run, making it accessible for everyone. Enjoy creating Xray links hassle-free!


### Disclaimer

I want to acknowledge the work of others and clarify that the `index.js` and `subworker.js` file is not my original work. It has been edited solely to ensure compatibility with the bot. 

### Credits
[2ri4eUI](https://github.com/2ri4eUI) \& [cmlio](https://github.com/cmliu)

This project is just the beginning, and there is potential for it to evolve further. The extent to which it progresses depends on how much it is liked and used. Your feedback and contributions are appreciated!

