# 💙 Professional TypeScript Backend Template

A **production-ready**, highly scalable Node.js backend template built with **TypeScript**, **Express**, and **Mongoose**. This architecture follows the industry-standard _"Chai aur Backend"_ pattern, enhanced with strict type safety and modern tooling.

---

![Professional TypeScript Backend Architecture](https://miro.medium.com/1*LTzl4u5pfzqaeOzhN1hblQ.png)

## 🛠 Tech Stack

- **Runtime:** Node.js (v18+)
- **Language:** TypeScript
- **Framework:** Express.js
- **Database:** MongoDB (via Mongoose)
- **Authentication:** JWT (Access & Refresh Tokens)
- **Development:** tsx (Next-gen TypeScript execution)

---

## 🚀 Quick Start

### 1. Clone & Install

```bash
git clone https://github.com/rajkishort596/Ts-Backend
cd server
npm install
```

### 2. Environment Variables

Create a `.env` file in the root directory and add the following:

```env
PORT=8000
MONGODB_URI=your_mongodb_connection_string
CORS_ORIGIN=*
ACCESS_TOKEN_SECRET=your_access_token_secret
ACCESS_TOKEN_EXPIRY=1d
REFRESH_TOKEN_SECRET=your_refresh_token_secret
REFRESH_TOKEN_EXPIRY=10d
```

### 3. Development Mode

Start the server with hot-reloading using tsx:

```bash
npm run dev
```

### 4. Build for Production

Compile TypeScript to optimized JavaScript:

```bash
npm run build
npm start
```

---

## 📂 Project Structure

```
src/
├── db/              # Database connection logic
├── models/          # Mongoose schemas & TypeScript interfaces
├── controllers/     # Request handlers (Business logic)
├── routes/          # Express route definitions
├── middlewares/     # Auth, Multer, and Error middlewares
├── utils/           # ApiError, ApiResponse, and AsyncHandler
├── types/           # Declaration merging (express.d.ts)
├── app.ts           # Express app configuration
├── constants.ts     # Constants declarations
└── index.ts         # Server entry point
```

---

## 🔑 Key TypeScript Features

1. **Declaration Merging**  
   Extended the Express `Request` interface to include the `user` object. Access `req.user` in any protected route without type errors.  
   _Location: `src/types/express.d.ts`_

2. **Mongoose Type Safety**  
   User models include custom methods like `isPasswordCorrect` and `generateAccessToken` with explicit `this` context binding.

3. **Centralized Error Handling**  
   Custom `ApiError` and `ApiResponse` classes ensure consistent API responses, even on errors.

4. **Relaxed Development**  
   `tsconfig.json` is optimized for developers transitioning from JS to TS—strict where it matters (database, auth), flexible where it's annoying (relaxed null checks).

---

## Author

s
**Made By Rajkishor Thakur**

## 🛡 License

ISC License. Feel free to use this template for your personal or commercial projects.

---

**Happy Coding!** ☕️
