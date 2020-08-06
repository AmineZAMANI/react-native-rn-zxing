
# react-native-rn-zxing

### 🔥 Finally 🔥 ... an easy way to implement an efficient QR Code scanner (Zxing based) using React native.

## Getting started

`$ npm install react-native-rn-zxing --save`

### Mostly automatic installation

`$ react-native link react-native-rn-zxing`

### Manual installation


#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.reactlibrary.RnZxingPackage;` to the imports at the top of the file
  - Add `new RnZxingPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-rn-zxing'
  	project(':react-native-rn-zxing').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-rn-zxing/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-rn-zxing')
  	```


## Usage
```javascript
import RnZxing from 'react-native-rn-zxing';

...
// Pass the callback as a parameter
RnZxing.showQrReader(this.onBarcodeScanned);

...
// Define the callback function to handle data after scan
onBarcodeScanned = (data) => {
        this.setState({data: data});
};

```
