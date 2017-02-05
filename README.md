# json
wawho json data stock
--------
## whats this?
role is my json data stock folder

## Usage
fetch or xhr access
```js
 var f=function(e='',t=''){return e+t},
      url=f('https://raw.githubusercontent.com/wawho/json/master/','test.json')
 
 fetch(url).then(function(response) {return response.json() })
  .then(function(json){console.log('fetch',json) })
  .catch((d)=>{ console.log('err fetch',d) });
 
 getJson(url)
  .then(function(json){console.log('getJson',json) })
  .catch((d)=>{ console.log('err getJson',d) });
```
fetch is pure ES.
if !fetch
tiny function make this: getJson()
```js
var getJson = function(url){
  return new Promise(function(sol,rej){ 
   var xhr = new XMLHttpRequest();
   xhr.onreadystatechange = function(){ 
    if( this.readyState == 4){ 
     if( this.status == 200|| this.status==0) sol( this.response);
     else rej(this.response);
    }
   }
   xhr.open( 'GET',url, true );xhr.responseType = 'json';xhr.send( null );
   });//
}
```

## Note
here is json data only.
main project user kunigamaeno.
 - https://github.com/kunigamaeno/temp/
 - https://github.com/kunigamaeno/

## Other
__LIC,MIT.__
