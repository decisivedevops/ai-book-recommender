<p align="center">
    <h1 align="center">📚💡 AI Book Recommender</h1>
</p>
<p align="center">
  <img src="./assets/book-recommender.jpg" width="300" height="300"/>
</p>


## tl;dr **📝**

> You give your favorite books, the script fetches books information such as title, genres, and synopsis. All this info is passed to ChatGPT using a prompt template to get the book recommendations.

## Table of Contents **🗂️**
<!--ts-->
* [<g-emoji class="g-emoji" alias="books" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f4da.png">📚</g-emoji>AI Book Recommender](#-ai-book-recommender)
   * [tl;dr <strong><g-emoji class="g-emoji" alias="memo" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f4dd.png">📝</g-emoji></strong>](#tldr-)
   * [Table of Contents <strong><g-emoji class="g-emoji" alias="card_index_dividers" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f5c2.png">🗂️</g-emoji></strong>](#table-of-contents-️)
   * [Description <strong><g-emoji class="g-emoji" alias="books" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f4da.png">📚</g-emoji></strong>](#description-)
   * [Usage <g-emoji class="g-emoji" alias="hammer_and_wrench" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f6e0.png">🛠️</g-emoji>](#usage-️)
      * [Requirements <strong><g-emoji class="g-emoji" alias="gear" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2699.png">⚙️</g-emoji></strong>](#requirements-️)
      * [Getting Started <g-emoji class="g-emoji" alias="rocket" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f680.png">🚀</g-emoji>](#getting-started-)
   * [Configuration <g-emoji class="g-emoji" alias="gear" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2699.png">⚙️</g-emoji>](#configuration-️)
   * [Contributing <g-emoji class="g-emoji" alias="wave" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f44b.png">👋</g-emoji>](#contributing-)
   * [License <g-emoji class="g-emoji" alias="scroll" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f4dc.png">📜</g-emoji>](#license-)

<!-- Created by https://github.com/ekalinin/github-markdown-toc -->
<!-- Added by: abhinav, at: Sat May 20 17:29:13 IST 2023 -->

<!--te-->
## Description **📚**

The AI Book Recommender 🤖📚 works by interacting with two main components: Goodreads 📖 for fetching book data, and OpenAI's ChatGPT 🧠 for generating recommendations.

   - **Goodreads 📖:** We're using Goodreads to fetch details about your favorite books 📚, including the book title 🏷️, author 🖋️, genres 🏷️, and synopsis 📝. The script then extracts this data and uses it to generate personalized book recommendations 🎯.

   - **OpenAI's ChatGPT 🧠:** We're using ChatGPT to generate book recommendations based on the book data fetched from Goodreads 📖. We feed ChatGPT with a conversation context 🗨️ where the user talks about their favorite books (the data fetched from Goodreads). The AI then responds with book recommendations 📚 in a conversational manner.

## Usage 🛠️

### Requirements **⚙️**

- Python 3.7 and above 🐍
- An OpenAI API key 🔑
- Git 📚

> [Here](PREREQUISITES.md) is detailed explanation for installing all the dependencies 🧩.

### Getting Started 🚀

1. Clone this repository on your local machine.

 ```bash
 git clone https://github.com/decisivedevops/ai-book-recommender.git
 ```

2. Navigate to the repository.

 ```bash
 cd ai-book-recommender/
 ```

3. Create a Python virtual environment and activate it.

 ```bash
 python3 -m venv venv
 source venv/bin/activate
 ```

4. Install the necessary dependencies.

 ```bash
  pip install -r requirements.txt
 ```

5. Rename the `sample.config.toml` file to `config.toml`:

 ```bash
 mv sample.config.toml config.toml
 ```

6. Open the `config.toml` file and update your OpenAI API key in the appropriate field.

7. Update your favorite books info in the `config.toml` file. Follow the provided format and add the titles and authors of your favorite books.

 ```toml
 [books]
 favorites = """
 Book Title, Author
 Book Title, Author
 Book Title, Author
 """
 ```

8. Run the `main.py` script:

 ```
 python3 main.py
 ```

9. The script gives reading recommendations based on your favorite books. The suggestions are also saved in the `logs` folder.

## Configuration ⚙️

The configuration file, `config.toml`, has various settings used by the script:

- OpenAI settings, including the model name, temperature, and API key 🌡️.
- A list of your favorite books 📚.
- Message templates used when interacting with ChatGPT 💌.

## Contributing 👋

Contributions are welcome. If you find a bug 🐞 or have an idea for an improvement or new feature, please raise an issue or submit a pull request.

## License 📜

AI Book Recommender is open source and available under the [MIT License](LICENSE).
