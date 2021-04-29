# void.db
<a href="https://voiddevs.org/dc" target="_blank"><img src="https://img.devsforum.net/tr/img/h1Z2X3.png" alt="Join our discord" width="256"></a><br>
**Support:** [https://voiddevs.org/dc](https://voiddevs.org/dc) <br>
**NPM:** [npmjs.com/package/void.db](https://www.npmjs.com/package/void.db)<br>

```js
const Database = require("void.db");
const db = new Database("./db.json");

db.set('serverStatus', { status: 'Online' })
/*
"serverStatus": {
  "status": "Online"
}
*/
db.add("money_claudette", 500)
/* 
  "money_claudette": 500
*/
db.push("serverSettings", { whitelist: "on", playerCount: "24" })
/*
"serverSettings": [
    {
      "whitelist": "on",
      "playerCount": "24"
    }
  ]
*/
db.has("money_claudette") // true
db.has("money_iclaudette") // false

db.get("money_claudette")
// => 500

db.sub("money_claudette", 100)
// => 400

db.fetch("serverStatus")
// => { status: "Online" }

db.get("serverStatus")
// => { status: "Online" }

db.delete("serverStatus")
// => {}

db.all()
/*
{
  money_claudette: 500,
  serverSettings: [ { whitelist: 'on', playerCount: '24' } ]
}
*/

db.clear()
// {}
```
## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://voiddevs.org/dc) address.*
- `npm i void.db`
#   v o i d . d b 
 
 
