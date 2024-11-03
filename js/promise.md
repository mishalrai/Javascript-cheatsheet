## Promise.withResolvers
Easier ways to work with promise


```javascript

function fetchData(url) {
    const { promise, resolve, reject } = Promise.withResolvers();

    fetch(url)
        .then(response => {
            // Check if the response is okay (status 200-299)
            if (response.ok) {
                return response.json(); // Parse JSON if response is okay
            } else {
                // Reject the promise if the response is not okay
                reject(new Error('API Invocation failed'));
            }
        })
        .then(data => {
            // Resolve the promise with the data
            resolve(data);
        })
        .catch(error => {
            // Catch and reject the promise if there is a network error
            reject(error);
        });

    return promise;
}

```


## Promise cancel 
In javascript don't have promise cancel function but we can throught the error on cancel method like below

```javascript

const cancellablePromise = () => {
    const { promise, resolve, reject } = Promise.withResolvers();

    promise.cancel = () => {
        reject("the promise got cancelled");
    };
    return promise;
};

```