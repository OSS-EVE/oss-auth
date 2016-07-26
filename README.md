## EVE Online - OSS Auth

### Requirements:
- Meteor
```
curl https://install.meteor.com/ | sh
```

### Getting started
1. clone this
2. Create settings.json in root (content see below)
3. Run Meteor (see below)

#### Build Production:
./build.sh

#### Run Development:

    meteor --settings settings.json

Open localhost:3000


#### 3rd Party API:

https://github.com/OSS-EVE/ejabberdauth
https://github.com/OSS-EVE/nodebb-plugin-oss-auth



#### settings.json content:

isDev prevents cronJobs.

```
{
  "isDev": 1, 
  "allianceID": "alliance id",
  "api": {
    "keyID": "keyid with standings access",
    "vCode": "vcode of said key",
    "characterID": "character to use standings from"
  },
  "email": {
    "smtp": "smtp://user:pw@mail.bos.gs:25",
    "from": "The OSS - AUTH <auth@bos.gs>"
  },
  "public": {
    "publicJabber": 1,
    "publicVoice": 0
  },
  "access": {
    "AUTH_JABBER": 1,
    "AUTH_VOICE": 2,
    "AUTH_FORUM": 4
  },
  "forum": {
    "categories": {
      "ops": 19
    },
    "url": "https://forum.oss.rocks/api/v1/topics"
  }
}

```
