markdown
<h1 align="center">
  <strong>💫 Chat WebUI  🤖💫</strong>
</h1>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/Toy-97/Chat-WebUI">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/Toy-97/Chat-WebUI">
  <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/Toy-97/Chat-WebUI">
  <img alt="GitHub Release" src="https://img.shields.io/github/v/release/Toy-97/Chat-WebUI">
  <img alt="GitHub License" src="https://img.shields.io/github/license/Toy-97/Chat-WebUI">
</p>




**🚀 Fully Offline Chat User Interface for Large Language Models**

![image](https://github.com/user-attachments/assets/39b795a5-f7e4-4b55-bf6b-6d380587e452)


Chat WebUI is an open-source, locally hosted web application that puts the power of conversational AI at your fingertips. With a user-friendly and intuitive interface, you can effortlessly interact with text, document and vision models and access a range of useful built-in tools to streamline your workflow.



## ✨ Key Features

* 🎨 **Inspired by ChatGPT**: Experience the same intuitive interface, now with expanded capabilities
* 🔄 **Multi-Model Support**: Seamlessly switch between text and vision models to suit your needs
* 🔗 **OpenAI Compatible**: Compatible with all OpenAI API endpoints, ensuring maximum flexibility
* 🧠 **Supports Reasoning Models**: Harness the power of reasoning models for your tasks
* 📤 **Chat Exporting**: Easily export your chat using JSON or Markdown format.
* 🛠️ **Smart Built-in Tools**:
  * 🔍 **Web Search**: Instantly find relevant information from across the web
  * 📺 **YouTube Video Summarizer**: Save time with concise summaries of YouTube videos
  * 📄 **Webpage Summarizer**: Extract key points from webpages and condense them into easy-to-read summaries
  * 🧪 **arXiv Paper Summarizer**: Unlock insights from academic papers with LLM-powered summarization



## ⚡ Installation

1. Clone the repository:
```

git clone https://github.com/Toy-97/Chat-WebUI.git

```
2. Navigate to the project directory:
 ```

cd Chat-WebUI

```
3. Install dependencies:
```

pip install -r requirements.txt

```
4. Run the application:
```

python app.py

```

### 🏃‍♂️ Running the Application

1. Open a web browser and navigate to `http://localhost:5000`
2. Press setting button at the top right corner and setup Base URL and API Key
3. Select model at top left side of screen
4. Start chatting! 💬

*If you are using Local LLM make sure to start the endpoint first before running app.py*


# 🧩 Features

### 🛠️ Smart Built-in Tools
Chat WebUI comes with a range of built-in tools that can be used to perform various tasks, such as:
  
1. 🔍 Online web search
2. 📺 YouTube video summarization
3. 🧪 arXiv paper and abstract summarization
4. 📄 Webpage text extraction


To use these tools, simply add `@s` to the start of your query. For example:
```

@s latest premier league news

```
The tool will automatically call the right function based on the link you provide. For example, this will extract the website text:
```

@s Summarize this page https://www.promptingguide.ai/techniques/cot

```

### 📺 YouTube Summarizer
You can include a YouTube URL in your query to obtain a summary of the video. For example:


```

@s what is this video about? https://www.youtube.com/watch?v=b4x8boB2KdI

```
![image](https://github.com/user-attachments/assets/704e2f19-ee01-4b43-a314-eae8c3df04cb)
The order of your query and URL does not matter, for example this will work too:


```

@s https://www.youtube.com/watch?v=b4x8boB2KdI what is this video about? 

```
Alternatively, you can simply provide the URL to utilize the built-in prompt:
```

@s https://www.youtube.com/watch?v=b4x8boB2KdI

```
This will employ the built-in prompt to generate a concise summary of the video.

### 🧪 arXiv Paper/Abstract Summarizer
Include an arXiv URL in your query to receive a brief summary of the paper or abstract:
```

@s explain this paper to me https://arxiv.org/pdf/1706.03762

```
Abstract URLs are also supported:
```

@s simply explain this abstract https://arxiv.org/abs/1706.03762

```

You can also paste the link to utilize the built-in prompt:

```

@s https://arxiv.org/abs/1706.03762

```
This will employ the built-in prompt to generate a concise summary of the paper or abstract.

### 📄 Webpage Scraper
If the link is not a YouTube or arXiv URL, the application will attempt to extract the text from the webpage:
```

@s summarize this into key points https://www.promptingguide.ai/techniques/cot

```
This also has built-in prompt that you can use by simply pasting the url:
```

@s https://www.promptingguide.ai/techniques/cot

```

### 🔍 Online Web Search
If you do not include a URL in your query, the application will perform a web search using the built-in prompt:
```

@s latest released movies

```
For optimal results, format your query in a manner similar to a Google search. You can find the reference URL used in the command prompt window.

### 🧠 Deep Query
Deep Query function has been changed in v1.1. Now pressing it will send thinking tag to the backend to force the model to think. For example the `</think>` tag.

You can set specific start tag and end tag for thinking models in additional settings. 

This should ensure future compatibility for various reasoning model in the future.

Make sure to set your start tag and end tag in additional settings before using reasoning model. 

![image](https://github.com/user-attachments/assets/0de5380f-8b52-441f-8783-5a0bea89bf14)

### ⚙️ Additional Settings
You can adjust model parameters by clicking the Additional Settings button (⚙️) next to the main Settings icon in the top-right corner.

Inside, you’ll find four preset buttons:
- 🎯 Precise – temperature = 0
- ⚖️ Balanced – temperature = 0.5
- 🎨 Creative – temperature = 1

Alternatively, choose Custom and enter your own sampler settings as comma-separated key=value pairs, for example:
```
temperature=0, top_p=0.3, reasoning_effort=high
```
![image](https://github.com/user-attachments/assets/6419e366-93b3-4def-8387-0c569fc38167)




### 🔒 Private Chat
Toggle it if you want to chat without saving it to conversation history. \
\
![image](https://github.com/user-attachments/assets/6505d914-bf4e-4405-9a98-ee85ca8aa24d)

### 📤 Export Button
There is export button that will appear when you hover at the bottom left corner. This allows you to export your chat using JSON or Markdown format.

![image](https://github.com/user-attachments/assets/be796691-09d7-434b-84c0-f80389d68da3)






### 🧩 Quirks
You can drag and drop images and any text documents into the chat window. RAG is currently not supported, so all text document files will use the full text as context.


## 🤝 Contributing

Contributions are welcome! If you'd like to contribute to the project, please fork the repository and submit a pull request.

## 📄 License

Open-source and freely available under the [MIT License](https://opensource.org/licenses/MIT). Check the [LICENSE](LICENSE) file for specifics.
