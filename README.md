
<img width="1440" alt="Screen Shot 2022-03-16 at 2 03 54 PM" src="https://user-images.githubusercontent.com/75461281/158668313-91b4e96d-ca8f-4786-90db-6369a6e84056.png">
### the Date object JavaScript
date and time are a object in javascript with myriad of properties and methods attached to them. We can create a date object with object constructor, new, like so:
`
new Date();
`
This js clock is built with with using the getHours, getMinutes and geSecond method. 
The process is simple. In the html, I created a div with a class of clock. In my js file we first reference the clock class via querySelector like so:
```
const clock = document.querySelector('.clock');
```
I then created a function, I calle it click, as a clock clicks, with no parameters, and to start a new date object stored a variable, called now:
```
const tick = () => {
  const now = new Date();
};
```
I needed to increase the now object every second for my clock to work, I decided to do it through setInterval method, where I bring in the tick function called every second like so:   
```
setInterval(now, 1000);
```
My next step was to include hours, minutes and seconds in the click function, I acheived it by using the getHours, getMinute and getSecond method, and saving them in a each variables on now like so:
```
const h = now.getHours();
const m = now.getMinutes();
const s = now.getSeconds();

```
My final task was to out put the time in the browse. I acheived it creating three sapn tags and using string literal and innerHTML and attaching it to the clock div to out put the time I am getting from my tick function:
```
cont html = `
<span>${h}</span>
<span>${m}</span>
<span>${s}</span>
`;
clock.innerHTML = html;
};
```