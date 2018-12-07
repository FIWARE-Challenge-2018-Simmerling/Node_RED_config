FIWAREChallenge
===============

FIWARE Challenge 2018 Vienna

### About

This is a Node Red configuration project for the FIWARE Challenge hackathon, which took place in December 2018 in Vienna.
This configuration fetches data from the Vienna City live data portal and pushes it to a local FIWARE Orion.
In parallel, the configuration is able to register a subscription at Orion, so that whenever the live data actually changes,
orion calls the registered callback API.

### Installation

1. Clone the parallel Node Red fork:

```
git clone --recurse-submodules https://github.com/FIWARE-Challenge-2018-Simmerling/node-red.git
```

Supposedly you would not need this way but use Node RED Project dependencies, but I didn't have time
to figure out how to do that.  (If you do, please make a PR.)

2. Initialise the resulting Node RED instance
```
cd node-red
npm install
cd nodes/node-red-contrib-fiware
npm install
cd ../..
npm run build
```

3. Launch the Node RED instance
```
npm start
```

Open Node RED in your browser at the designated URL, e.g. `http://127.0.0.1:1880`.

Note that the exact URL may be different, especially if you have earlier Node RED configuration.

4. Add this repo to your Node RED projects

* Open the menu from the upper right hand corner
* Select Projects->Open
* Select Clone repository
* Fill in this repo URL, e.g. `https://github.com/FIWARE-Challenge-2018-Simmerling/Node_RED_config.git`
* Change the project name to something more useful, e.g. "FIWARE2018"
* For the Credentials encryption key, give `FIWARE2018`
* Click Clone Repository

The project will load.  

5. Change the authentication token

To actually run the demo, you have to manually change the authentication token in "Add authentication".  To do that, you need to have have a `client_id` and `client_secret` to the `https://smartdata.wien/api/v1/access_token` service.

### License

This code has been explicitly placed in public domain.  You may use it in whatever way you want to.
