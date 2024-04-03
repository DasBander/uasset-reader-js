# UAsset Reader JS ( Modified for Node.js )
Read and extract informations of `.uasset` files from Unreal Engine in javascript.
This is a modified version to work with Node.js.
Originally created by https://github.com/blueprintue/uasset-reader-js.


## How to use
###Installation
```js
npm i --save https://github.com/DasBander/uasset-reader-js.git
```


###Usage
```js
//Include uasset-reader-js
const UAssetReader  = require('uasset-reader-js');

//Define Asset Reader
const AssetReader = new UAssetReader.ReaderUasset();

//Load Asset into buffer
const LoadedFile = await fs.readFile("<PathToAssetFile>");

//Convert Buffer into Uint8 Byte Array
const bytes = new Uint8Array(LoadedFile);

//Read Data from UAsset. Returns complete asset data with Thumbnails.
const Asset = AssetReader.analyze(bytes, false);
```

