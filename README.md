
GeoLite2-Country.mmdb upload file to home directory

Open index.js and add them


Country Blocking will not work in all countries except the one you have added
```
// ipblock.

const ipgeoblock = require("ipgeoblock-fixed");

app.use(ipgeoblock({
	geolite2: "./GeoLite2-Country.mmdb",
	blockedCountries: [ "US" ]
}, function (req, res) {
	res.statusCode = 500;
	res.redirect("https://block.hellnodes.com");
}));

```



To block all countries and allow specific countries
```

	
// ipblock.

const ipgeoblock = require("ipgeoblock-fixed");

app.use(ipgeoblock({
	geolite2: "./GeoLite2-Country.mmdb",
	allowedCountries: [ "US" ]
}, function (req, res) {
	res.statusCode = 500;
	res.redirect("https://block.hellnodes.com");
}));
```



Don't forget to download after adding.

npm install ipgeoblock-fixed



