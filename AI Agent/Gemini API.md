[Large language models](https://www.cloudflare.com/learning/ai/what-is-large-language-model/) (LLMs) are the fancy-schmancy AI technology that has been making all the waves in the AI world in recent years. Products like:

- ChatGPT
- Claude
- Cursor
- Google Gemini

... are all powered by LLMs. For the purposes of this course, you can think of an LLM as a smart text generator. It works just like ChatGPT: _you give it a prompt, and it gives you back some text that it believes answers your prompt_. We're going to use [Google's Gemini API](https://ai.google.dev/gemini-api/docs/pricing) to power our agent in this course. It's reasonably smart, but more importantly for us, _it has a free tier_.

Again, the free-tier rate limits on the Gemini API have been [drastically reduced](https://www.reddit.com/r/GeminiAI/comments/1pg4et5/google_reduces_api_rate_limits_for_free_tier/) as of December 2025. We recommend [using a paid account](https://ai.google.dev/gemini-api/docs/billing) if possible to avoid running into these limits. The total cost incurred during this course should be minimal (~$1–2).

Be aware that all API calls, including those made during testing, will add to your usage of model requests and tokens. If you stay on the free tier and exhaust your quota, you'll need to wait for it to reset (typically 24 hours) before continuing. Regenerating your API key will not reset your quota.

## Tokens

You can think of tokens as the currency of LLMs. They're the way that LLMs measure how much text they have to process. Tokens are [_roughly_ 4 characters](https://help.openai.com/en/articles/4936856-what-are-tokens-and-how-to-count-them) for most models. It's important when working with LLM APIs to understand how many tokens you're using.

Our usage will be quite modest – hopefully within the free-tier limits of the Gemini API – but we'll still monitor how many tokens are consumed during our requests.

## Assignment

1. Create an account on [Google AI Studio](https://aistudio.google.com/) if you don't already have one.
    
2. Click the "Create API Key" button. Here are the [docs](https://ai.google.dev/gemini-api/docs/api-key) if you get lost.
    
    If you already have a GCP account and a project, you can create the API key in that project. Otherwise, AI Studio will walk you through creating a new project before generating the key.
    
3. Copy the API key and paste it into a new `.env` file in your project directory. The file should look like this:
    
    ```sh
    GEMINI_API_KEY='your_api_key_here'
    ```
    
4. Add the `.env` file to your `.gitignore`.
    
    We _never_ want to commit API keys, passwords, or other sensitive information to Git.
    
5. Update the `main.py` file. When the program starts, load the environment variables from the `.env` file using the `dotenv` library, and read the API key:
    
    ```py
    import os
    from dotenv import load_dotenv
    
    load_dotenv()
    api_key = os.environ.get("GEMINI_API_KEY")
    ```
    
6. If the environment variable wasn't found – i.e., if `api_key` is `None` – raise a `RuntimeError` with a helpful message.
    
7. Import the `genai` library and use the API key to create a new instance of a [Gemini client](https://googleapis.github.io/python-genai/#create-a-client):
    
    ```py
    from google import genai
    
    client = genai.Client(api_key=api_key)
    ```
    
8. Use the [`client.models.generate_content()` method](https://googleapis.github.io/python-genai/#generate-content) to get a response from the [`gemini-2.5-flash` model](https://ai.google.dev/gemini-api/docs/models)! You'll need to use two _named_ parameters:
    
    - `model`: The model name, `gemini-2.5-flash` (this one is still available on the free tier, albeit with increasingly strict limits)
    - `contents`: The prompt to send to the model (a string). For now, **hard-code this prompt exactly**:
        
        ```text
        "Why is Boot.dev such a great place to learn backend development? Use one paragraph maximum."
        ```
        
9. The `generate_content` method returns a [`GenerateContentResponse` object](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentResponse). **Print the [`.text`property](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentResponse.text) of the response** to see the model's answer.
    

If everything is working as intended, you should be able to run your code and see the model's response in your terminal!