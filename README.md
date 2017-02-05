# json
wawho json data stock
--------
## whats this?
role is my json data stock folder

## Usage
fetch or xhr access
```js
fetch().then((d)=>{ console.log(d) });
getJson().then((d)=>{ console.log(d) });
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
