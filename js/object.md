## Object



### Add and update the object key value

```javascript
    let user = {name: 'Mishal', cast: 'Rai', address: 'Bhimshengola'};

    // To add new property
    user = {...user, country: 'Nepal'};
    console.log(user);

    // To update property value
    user = {...user, name: 'Priya'}
    console.log(user)

```


### Delete key from the object

```javascript
    let user = {name: 'Mishal', cast: 'Rai', address: 'Bhimshengola'}

    const {name, ...updatedUser} = user;
    console.log(updatedUser);

```

Dynamically remove

```javascript
    let user = {name: 'Mishal', cast: 'Rai', address: 'Bhimshengola'};

    const key = 'name';
    const {[key]:_, ...updatedUser} = user;

    console.log(updatedUser, 'updated user data') 
```


