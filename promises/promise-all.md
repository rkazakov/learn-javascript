# Promise.all #

Receive data from Promise.all in case one of the promises fail.

```
const makeRequest = (url) => {
	return new Promise((resolve, reject) => {
  	if (url) {
    	resolve(url);
    } else {
    	reject('error');
    }
  })
  .catch((err) => {
  	return err;
  });
}

const p1 = makeRequest('url1');
const p2 = makeRequest(); // fail
const p3 = makeRequest('url3');

Promise.all([p1, p2, p3])
	.then((res) => {
  	console.log('Promise.all', res);
  })
  .catch((err) => {
  	console.log('Promise.all error', err);
  });
  ```
