## Logging the object in command

If you are viewing log in a terminal especially if you are a backend developer then you can try `JSON.stringify(your_data, null, 2)` and use `console.log()` on the result. This will make sure that you don't get `{... value: [Object, Object]}` in the log and the log will also be formatted making it easier to read.