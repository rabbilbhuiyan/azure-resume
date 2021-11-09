# azure-resume
My own azure resume, following [Azure cloud guru project video.](https://www.youtube.com/watch?v=ieYrBWmkfno&t=1380s&ab_channel=ACloudGuru)

# First steps
- creating project structure
- For that first create a new git repo and clone it to local machine
- Also clone the [a cloud guru](https://github.com/ACloudGuru-Resources/acg-project-azure-resume-starter) repo to local machine
- copy the front end and back end folder from a cloud guru repo to your own repo
- frontend folder contains the static website
  - create a file called main.js
  - main.js contains visitor counter code

```js
const getVisitCount = () => {
  let count = 30;
  fetch(functionApi).then(response => {
    return response.json()
```