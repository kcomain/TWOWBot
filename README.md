<p align="center"><img width="350" src="https://cdn.discordapp.com/attachments/187311902085349376/187745473723891713/TWOWBot.png"></p>
<h1 align="center">TWOWBot</h1>

A simple bot for hosting miniTWOWs on [Discord](https://discordapp.com) which you can invite from [here](https://discordapp.com/oauth2/authorize?client_id=222869815650418690&scope=bot).

[![Discord](https://discordapp.com/api/guilds/303616392710586373/widget.png)](https://discord.gg/t58ukQW)

### About TWOWBot
#### This bot is being developed by:
* Bottersnike #3605
* hanss314 #0128
* Noahkiq #0493
#### The main bot is being hosted by:
* Bottersnike #3605

---
### How to use TWOWBot:
#### Hosting an mTWOW:
The host of an mTWOW has a coupple of commands for them to use:
* `set_prompt` will set the prompt for the round.
* `responses` will send you a DM listing all of the responses so far.
* `start_voting` will then close responses and allow people to vote.
* Finally, `results` will end the round and show results
* You can also use `transfer` to make someone else the host of the mTWOW.
#### Participating in an mTWOW:
When you are participating, you also have some commands you can use:
* `respond`, when in a DM, allows you to respond to a prompt.
* `vote`, when in a DM, will first generate your voting slide, and then allow you to vote on it.
#### Other useful commands:
There are a few commands that are useful to know:
* `prompt` will show you the current prompt.
* `round` and season will tell you the round and season number respectively.
* `id` will get you the channel identifier for that mTWOW. This is needed when responding or voting.

---
### All commands:
| command | brief description |
| ------- | ----------------- |
| `round` | Get the current round number. |
| `sudo` | Run a command ignoring every check. |
| `evaluate` | Run some code. |
| `vote` | Vote on the responses. |
| `die` | Disconnects the bot. |
| `respond` | Respond to the current prompt. |
| `say` | Get te bot to say something. |
| `help` | This help message :D
| `ping` | Ping the bot. |
| `id` | Get the server ID used in voting. |
| `role_ids` | Get all of the role ids for the server. |
| `about` | Get info about the bot. |
| `me` | Get info about yourself. |
| `prompt` | Get the current prompt. |
| `how` | Get instructions on hosting a mTWOW. |
| `season` | Get the current season number. |
| `register` | Setup channel initially
| `show_config` | Sends the config file for this channel. |
| `set_times` | Set timer for next events.` | Events are voting and results. |
| `set_prompt` | Set the prompt for this round. |
| `start_voting` | Start voting. |. |
| `transfer` | Transfer ownership of this mTWOW. |
| `results` | End this round and show results. |
| `delete` | Delete the mTWOW. |
| `responses` | List all responses this round. |

To get inpepth help into any of these commands including what arguments they require and who can use them, use the `help` command.

### How to host the bot:
Hosting TWOWBot is relatively simple. To download it and get it set up follow:
```sh
$ git clone https://github.com/HTSTEM/TWOW_Bot TWOWBot
$ cd TWOWBot
$ git checkout yaml
$ sudo python3 -m pip install -U git+https://github.com/Rapptz/discord.py@rewrite
$ sudo python3 -m pip install ruamel.YAML
$ cp config.yml.template config.yml
$ chmod +x *.sh
$ cd server_data
$ cp servers.yml.template servers.yml
```
You will then need to edit `config.yml` with your information. Your bot token can be found [here](https://discordapp.com/developers/applications/me),
the developers section should have your ID in it, and then anyone else that might need full control of the bot,
for example, any alt accounts you have. The host should have your ID in it.

Once you've configured the bot, you can start it using:
```sh
$ . ./run_bot_python3.sh
```
This will start it in a loop, so if the bot crashes, it will start back up. If you want to only run it once, use:
```sh
$ python3 bot.py
```
