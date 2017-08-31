# ES6 Promise #

```
const getOrders = () => 
new Promise((resolve, reject) => {
	const isActive = true;
  if (isActive) {
  	return resolve('Active');
  }
  else {
  	return reject('Closed');
  }
});

const result = getOrders()
	.then((data) => {
  	console.log(data);
  });
```
