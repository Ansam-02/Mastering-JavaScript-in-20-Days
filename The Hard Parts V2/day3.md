# Day 3: Async JavaScript and Promises

talking about the promises and the asynchronous functions with some exercises.

## Lesson Summary

- Waht is async function and how it work.
- Web APIs, the Callback .
- Deal with the promises.
- using `setTimeOut` function and fetch().
- How to use .then block.

## Coding Example

```javascript

    function display(data){console.log(data)}
  function printHello(){console.log("Hello");}

  function blockFor300ms(){/* blocks js thread for 300ms }
  setTimeout(printHello, 0);

  const futureData = fetch('https://twitter.com/will/tweets/1')
  futureData.then(display)
  blockFor300ms()

  console.log("Me first!");

```

#### My Solution

 ### [Exercise 1](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day3-tasks/tasks.md)

```javascript
  const executeInSequenceWithCBs = (tasks, callback) => {
  const messages = [];
  
  const executeTask = (index) => {
    if (index >= tasks.length) {
      callback(messages);
      return;
    }

    const task = tasks[index];
    task((message) => {
      messages.push(message);
      executeTask(index + 1);
    });
    };

      executeTask(0);
    };

    executeInSequenceWithCBs(asyncTasks, (messages) => {
      console.log(messages);
  });
```

 ### [Exercise 2](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day3-tasks/tasks.md)

```javascript
const executeInParallelWithPromises = (apis) => {
  const requests = apis.map(api => fetch(api.apiUrl).then(response => response.json()));

  return Promise.all(requests).then(data => {
    return data.map((apiData, index) => ({
      apiName: apis[index].apiName,
      apiUrl: apis[index].apiUrl,
      apiData: apiData
    }));
  });
};

executeInParallelWithPromises(apis)
  .then(results => {
    console.log(results);
  })
  .catch(error => {
    console.error(error);
  });
```

 ### [Exercise 3](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day3-tasks/tasks.md)

```javascript

 const executeInSequenceWithPromises = (apis) => {
  return apis.reduce((promiseChain, api) => {
    return promiseChain
      .then((results) => {
        return fetch(api.apiUrl)
          .then((response) => response.json())
          .then((apiData) => {
            results.push({
              apiName: api.apiName,
              apiUrl: api.apiUrl,
              apiData: apiData,
            });
            return results;
          });
      });
  }, Promise.resolve([]));
 };

 executeInSequenceWithPromises(apis)
  .then((results) => {
    console.log(results);
  })
  .catch((error) => {
    console.error(error);
  });
```
