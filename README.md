## KLPSARB - The Kali Linux PSA Reddit Bot
#### A Reddit bot to automate common responses to support questions on r/linuxquestions and elsewhere

This is a bot built with PRAW, [the Python Reddit API Wrapper](https://github.com/praw-dev/praw). I decided to make it in response to the increasinly frequent posts from Linux beginners regarding Kali on r/linuxquestions and elsewhere. These posts' low quality and level of technical sophistication suggest that some new users are not aware of Kali's actual use cases, intended audience, or inherent risks when run as a daily driver/persistently installed. KLPSARB uses [bs4](https://launchpad.net/beautifulsoup) to retrieve a message from Kali's docs urging would-be users to consider if the distro is the right choice for them. It posts a short, informative reply to the OP that is meant to automate and summarize the responses from redditors that typically accompany these posts.

## Installation and Usage
Assuming you use `pip`:
```
pip -r requirements.txt
chmod +x klpsarb
./klpsarb <subreddit>
```
The script requires that the environment variables REDDIT_CLIENT_ID, REDDIT_CLIENT_SECRET, REDDIT_USERNAME, and REDDIT_PASSWORD are set.
Tested on Arch.

## TODO

- Add support for PRAW's different configuration options.
- Add support for multiple subreddits.
- Containerize it for easy cloud deployment.
