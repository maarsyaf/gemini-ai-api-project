# Gemini 2.5 Flash — API Integration (Node.js + Express)

Proyek ini menunjukkan integrasi **Google Gemini 2.5 Flash** ke dalam RESTful API menggunakan **Node.js** dan **Express**. Mendukung input multimodal: **text**, **image**, **document**, dan **audio**.

## Cara pakai (singkat)
1. Clone:
```bash
git clone https://github.com/maarsyaf/gemini-ai-api-project.git
cd your-repo

```
2. Install:
```bash
npm install express dotenv @google/genai multer

```
3. Buat `.env`:
```
API_KEY=your_gemini_api_key_here
PORT=3000
```
4. Jalankan:
```bash
node index.js
nodemon index.js

```
API berjalan di `http://localhost:3000`.

## Implementasi singkat
- Gunakan **dotenv** untuk API key.
- Gunakan **multer** untuk upload file (direktori `uploads/`).
- Konversi file ke format kompatibel Gemini (inlineData / MIME).
- Hapus file sementara setelah proses (`fs.unlinkSync()`).
- Gabungkan `prompt + file` sebagai input ke method seperti `generateContent()`.

## Tujuan
Submission Hacktiv8: membuktikan kemampuan membangun API multimodal yang memanfaatkan Google Gemini 2.5 Flash untuk menganalisis, mendeskripsikan, atau mentranskrip konten dunia nyata.

## Tech
- Node.js, Express  
- Multer  
- dotenv  
- Gemini 2.5 Flash
