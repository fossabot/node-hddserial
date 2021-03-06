[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fihabhamad%2Fnode-hddserial.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fihabhamad%2Fnode-hddserial?ref=badge_shield)

Retrieve hdd serial number in Linux,Windows,MacOS.

**Features:**
-----
works on `Linux`,`Windows`,`MacOS`

Testing
-----
Windows : [windows 7,windows 10,Server 2008,2012]

Linux   : [ubuntu 16.10,CentOS 7.5]

MacOS   : [MacOS Sierra 10.12]

Usage
-----

```
npm install --save hddserial
```

```JavaScript
var hddserial = require('hddserial');
```
Examples
--------------
     
    .one(hdd-index, callback) → string 
     //hdd-index numaric value 0 equals first hdd on pc or os hdd you can use .first
    .first(callback) → string  
    .all(callback)        → { array of strings index of array = index of hdd }

---
Retrieves the HDD Serial Number for index 1 HDD {sdb on linux}.

```JavaScript
hddserial.one(1,function (err, serial) {
  console.log("hdd serial for first hdd : %s", serial);  
});
```
Output String
```
→ hdd serial for hdd with index 1 : N31FNPH8
```
Retrieves the HDD Serial Number  for index 0 or first HDD {sda on linux}.
```JavaScript
hddserial.first(function (err, serial) {
  console.log("hdd serial for first hdd : %s", serial);  
});
```
Output String
```
→ hdd serial for first hdd : 5L09TDHA
```
Retrieves all HDD Serials Number {sda,sdb,sdc on linux}.

```JavaScript
hddserial.all(function (err, serial) {
  console.log(serial);  
});
```
Output array
```JavaScript
['5L09TDHA','N31FNPH8','6YD3W4E9']
```


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fihabhamad%2Fnode-hddserial.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fihabhamad%2Fnode-hddserial?ref=badge_large)