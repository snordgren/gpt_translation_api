# gpt_translation_api

ChatGPT is now competent enough to translate between languages. This is a simple 
proof-of-concept Python API that uses the [ChatGPT](https://platform.openai.com/docs/guides/chat)
API to translate between languages.

## Usage
### Installation
```bash
poetry install
echo 'OPENAI_API_KEY=YOUR_API_KEY' > .env
```

### Running the server locally
```bash
poetry run uvicorn main:app --reload
```

### Testing the server with cURL
```bash
curl --header "Content-Type: application/json" --request POST --data '{"text":"Watch out, stormtroopers!", "context":"The author is paraphrasing a Star Wars scene. Stormtroopers are called Stormtroopers in Spanish, too.", "language":"Spanish"}' http://localhost:8000/translate
```
