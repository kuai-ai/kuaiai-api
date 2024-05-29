安装openai的Node.js库
``` 
npm install openai  
```
运行以下代码
```
const { Configuration, OpenAIApi } = require("openai");

const configuration = new Configuration({
  apiKey: "您的访问码",
  basePath: "https://api.kuaiai.app/v1"
});
const openai = new OpenAIApi(configuration);

const chatCompletion = await openai.createChatCompletion({
  model: "gpt-3.5-turbo",
  messages: [{role: "user", content: "Hello world"}],
});
console.log(chatCompletion.data.choices[0].message.content);
```
正常运行打印如下
``` 
Hello there! How can I assist you today ? 
```
