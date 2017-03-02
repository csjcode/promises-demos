# promises-demos
Demos of Javascript Promises

### Game Example

* Set up an html page with a button that says "Click me"
* add a scritp tag with a console.log("Game has started");
* remove console.log
* Add this:
```javascript
document.querySelector('button').addEventListener('click',()=>{
  ++counter;
});

setTimeout(()=>{
  if (counter > 5){
    alert(`You won! ${counter} clicks`);
  } else {
    alert('You lost!')
  }
},2000);
```
* How can we do all this in a single function?
* Declare a function startGame and place all code in it.
* To make a promise:
```javascript
return new Promise((resolve,reject)=>{
  setTimeout(()=>{
    if (counter > 5){
      resolve();
    } else {
      reject();
    }
  },2000);
});

startGame().then(() => alert('You win!'))
  .catch(() => alert('You lost!'));
```
