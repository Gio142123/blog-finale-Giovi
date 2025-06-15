# blog-finale-Giovi # 📝 Blog Multiutente – `blog-finale`

Un'applicazione backend per la gestione di un **blog multiutente** con funzionalità di:
- Registrazione/Login
- Recupero password
- Creazione e modifica post
- Like, commenti, tagging
- Ricerca nei post
- Profili utente pubblici

---

## 🚀 Tecnologie utilizzate

- Node.js
- Express.js
- MongoDB + Mongoose
- JWT (autenticazione)
- Bcrypt (hashing password)
- Jest + Supertest (testing)
- Dotenv (configurazione ambienti)

---

## 🔧 Installazione

Clona il repository e installa le dipendenze:

```bash
git clone 
cd blog-finale
npm install
```

Crea un file `.env` nella root con queste variabili:

```env
PORT=3000
MONGO_URI=mongodb://localhost:27017/blogdb
JWT_SECRET=supersegreto
```

---

## ▶️ Avvio in locale

```bash
npm run dev
```

---

## 🧪 Esecuzione test

Crea anche un `.env.test` (con un database separato):

```env
MONGO_URI=mongodb://localhost:27017/blog_test
JWT_SECRET=testsegreto
```

Poi:

```bash
npm test
```

---

## 📚 API principali

| Metodo | Endpoint               | Descrizione                     |
|--------|------------------------|---------------------------------|
| POST   | `/api/auth/register`   | Registra nuovo utente          |
| POST   | `/api/auth/login`      | Login utente                   |
| POST   | `/api/auth/forgot`     | Richiesta reset password       |
| POST   | `/api/posts`           | Crea un nuovo post             |
| GET    | `/api/posts`           | Lista tutti i post             |
| GET    | `/api/posts/:id`       | Dettagli di un singolo post    |
| POST   | `/api/posts/:id/like`  | Metti o togli like             |
| POST   | `/api/posts/:id/comment` | Aggiungi commento           |
| GET    | `/api/users/:id`       | Vedi profilo utente pubblico   |

---

## 🧩 Struttura cartelle

```
blog-finale/
├── models/
├── controllers/
├── routes/
├── middlewares/
├── tests/
├── .env
├── server.js
├── README.md
```

---

## 📌 Autore

Progetto sviluppato da [Tuo Nome] durante il corso *Junior Full Stack Developer* – TNV Academy (2024/2025).

---

## ✅ TODO

- [ ] Refactoring codice
- [ ] Deployment (facoltativo)
- [ ] Aggiunta documentazione API (es. Swagger)
