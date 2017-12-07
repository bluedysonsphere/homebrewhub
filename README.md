# [Homebrew Hub](https://gbhh.avivace.com)

Contribute to the games database [here](https://github.com/dmg01/database)

## Deploy

### Backend
**Requisites**: node, mongodb

Clone the repo
```
git clone https://github.com/dmg01/showcase
```

Edit the configuration

- `config/database.js` mongodb instance details
```javascript
module.exports = {
    'url' : 'mongodb://localhost:27018/database'
};
```

- `config/email.js` SMTP email server configuration
```javascript
module.exports = {
    // Email
    'host' : '',
    'port' : 465,
    'secure' : true,
    'user' : '',
    'pass' : '',
    'domain' : "",
    'sender' : '"HomebrewHub" <no-reply@host.com>',
};
```

Start mongodb server
```
cd showcase
mkdir database
mongod --dbpath=database --port 27018
```

Node things
```
cd showcase
npm install
npm start
```

Your instance is live at `localhost:8080/`

### Frontend

`views` folder. Based on Bootstrap `v4.0.0-beta.2`.