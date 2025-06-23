# ❌ No-as-a-Service

<p align="center">
  <img src="https://raw.githubusercontent.com/hotheadhacker/no-as-a-service/main/assets/imgs/naas-with-no-logo-bunny.png" width="800" alt="No-as-a-Service Banner" width="70%"/>
</p>


Ever needed a graceful way to say “no”?  
This tiny API returns random, generic, creative, and sometimes hilarious rejection reasons — perfectly suited for any scenario: personal, professional, student life, dev life, or just because.

Built for humans, excuses, and humor.

<!-- GitAds Sponsorship Badge -->
<p align="center">
  <a href="https://docs.gitads.dev/">
    <img src="https://gitads.dev/assets/images/sponsor/camos/camo-3.png" alt="Sponsored by GitAds" />
  </a>
</p>

<p align="center">
  This project is <strong>sponsored by <a href="https://docs.gitads.dev/docs/getting-started/publishers">GitAds</a></strong>.<br>
  You can get your GitHub repository sponsored too — <a href="https://docs.gitads.dev/docs/getting-started/publishers">create your account now</a>.
</p>

---

## 🚀 API Usage

**Base URL**
```
https://naas.isalman.dev/no
```

**Method:** `GET`  
**Rate Limit:** `120 requests per minute per IP`

### 🔄 Example Request
```http
GET /no
```

### ✅ Example Response
```json
{
  "reason": "This feels like something Future Me would yell at Present Me for agreeing to."
}
```

Use it in apps, bots, landing pages, Slack integrations, rejection letters, or wherever you need a polite (or witty) no.

---

## 🌐 Language Support

No-as-a-Service supports multiple languages based on the `Accept-Language` header:

### Example Request with Language Preference
```http
GET /no
Accept-Language: fr
```

### Currently Supported Languages
- English (en) - Default
- German (de)
- French (fr)
- Portugês (pt)

### Contributing Translations
We welcome contributions for new languages! Simply create a new JSON file in the `reasons` directory:
1. Name it using the 2-letter language code (e.g., `es.json` for Spanish)
2. Add your creative rejection phrases as a JSON array
3. Submit a pull request

## 🛠️ Self-Hosting

Want to run it yourself? It’s lightweight and simple.

### 1. Clone this repository
```bash
git clone https://github.com/hotheadhacker/no-as-a-service.git
cd no-as-a-service
```

### 2. Install dependencies
```bash
npm install
```

### 3. Start the server
```bash
npm start
```

The API will be live at:
```
http://localhost:3000/no
```

You can also change the port using an environment variable:
```bash
PORT=5000 npm start
```

---

## 📁 Project Structure

```
no-as-service/
├── index.js            # Express API
├── reasons.json        # 1000+ universal rejection reasons
├── package.json
└── README.md
```

---

## 📦 package.json

For reference, here’s the package config:

```json
{
  "name": "no-as-service",
  "version": "1.0.0",
  "description": "A lightweight API that returns random rejection or no reasons.",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "author": "hotheadhacker",
  "license": "MIT",
  "dependencies": {
    "express": "^4.18.2",
    "express-rate-limit": "^7.0.0"
  }
}
```

---

## 👤 Author

Created with creative stubbornness by [hotheadhacker](https://github.com/hotheadhacker)

---

## 📄 License

MIT — do whatever, just don’t say yes when you should say no.
