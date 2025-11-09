# Gemini 2.5 Flash — API Integration (Node.js + Express)

Ringkasan singkat  
Proyek ini menunjukkan integrasi **Google Gemini 2.5 Flash** ke dalam RESTful API menggunakan **Node.js** dan **Express**. Mendukung input multimodal: **text**, **image**, **document**, dan **audio**.

## Cara pakai (singkat)
1. Clone:
```bash
git clone https://github.com/maarsyaf/gemini-ai-api-project.git
cd your-repo
```
2. Install:
```bash
npm install
```
3. Buat `.env`:
```
API_KEY=your_gemini_api_key_here
PORT=3000
```
4. Jalankan:
```bash
npm start
```
API berjalan di `http://localhost:3000`.

## Endpoint (intinya)
- `POST /generate-text`  
  Body JSON: `{ "prompt": "..." }`
- `POST /generate-from-image`  
  Form-data: file image
- `POST /generate-from-document`  
  Form-data: file dokumen (pdf/docx)
- `POST /generate-from-audio`  
  Form-data: file audio

## Contoh cepat
Text:
```bash
curl -X POST http://localhost:3000/generate-text   -H "Content-Type: application/json"   -d '{"prompt":"Ringkaskan artikel ini"}'
```
Image:
```bash
curl -X POST http://localhost:3000/generate-from-image   -F "file=@/path/to/image.png"
```

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
