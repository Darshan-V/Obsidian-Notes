- [ ] need to optimise big code
- [ ] presence of lot of conditionals 
- [ ] presence of lot of unwanted dependancy states
- [ ] remainder: using router but was mentioned not to use
- [ ] extract buttons / create a common button 
[[Learned while building Game Cafe bookings app/TODOS]]


### slot response format 
```js 
import React, { useState } from "react";

  

const scheduleData = [

{

jwt: "asdfasdfasfd",

priceTier: {

name: "GOLD",

pricePerHour: 50,

pricePerHalfHour: 30,

colorTag: "#FFFE33",

},

slots: [

[

[

["PC1", "09:00 AM", "10:00 AM"],

["PC2", "10:00 AM", "11:00 AM"],

],

[["PC3", "09:00 AM", "11:00 AM"]],

],

[[["PC1", "11:00 AM", "01:00 AM"]], [["PC2", "11:00 AM", "01:00 AM"]]],

],

},

];

  

const ScheduleSwitchPCsComponent: React.FC = () => {

const getSlotClickHandler = (i: number, j: number) => () => {

console.log(scheduleData[i].slots[j]);

};

  

return (

<div>

{scheduleData.map(({ priceTier, slots }, i) => {

return (

<div key={i}>

<p>{priceTier.name}</p>

  

<div>

{slots.map((slot, j) => {

const from = slot[0][0][1];

const to =

slot[0].length > 1

? slot[0][slot[0].length - 1][2]

: slot[0][0][2];

  

return (

<div key={i} onClick={getSlotClickHandler(i, j)}>

{from} - {to}

</div>

);

})}

</div>

</div>

);

})}

</div>

);

};

  

export default ScheduleSwitchPCsComponent;
```