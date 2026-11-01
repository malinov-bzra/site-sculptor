# site-sculptor

A small side project where you change a website by just telling an AI what you want. You get a preview first and then decide: keep it or throw it away.

I'm still learning web development, so this is a work in progress. It's rough in some places and I'm adding stuff step by step.

## What it does right now

- You write what you want to change in normal language
- The AI rebuilds the page and shows you a preview
- You click **Accept** (it gets saved) or **Reject** (nothing changes)
- Your saved page is still there when you reload
- You can add your own images and use them in your requests ("image 1 as header")
- It runs with a local AI on your own computer, so no account, no API key, no cost

## How to try it

You need a local AI program. I use [LM Studio](https://lmstudio.ai).

1. In LM Studio, download a model (bigger is better, around 7B or more worked okay for me)
2. Go to the local API settings and start the server
3. Turn on **CORS**, otherwise the browser blocks the requests
4. Look up the address LM Studio shows (mine is `http://localhost:1235/v1`, the port can be different for you)
5. Download this repo and open `index.html` in your browser
6. Open **Settings** at the bottom, paste the address and click **Test connection**
7. Type what you want to change and hit the button

Other programs like Ollama should work too, as long as they offer an OpenAI-compatible API.

## What I want to add next

- [ ] A real backend (Node.js + Express)
- [ ] Login, so everyone can have their own page
- [ ] Database (SQLite)
- [ ] Version history with an undo button
- [ ] Some tests
