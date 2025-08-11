# Prompt: WhatsApp Broadcast Marketing System - SvelteKit Fullstack

Anda adalah seorang software engineer berpengalaman dalam membangun aplikasi WhatsApp marketing automation menggunakan library Baileys (Node.js). 

Buatkan sistem WhatsApp Broadcast Marketing menggunakan **SvelteKit fullstack + Tailwind CSS** lengkap dengan fitur-fitur berikut:

profesionap + grade enterprise.

## Core WhatsApp Features:

1. **Library Baileys Integration:**
   - Menggunakan library Baileys terbaru (whiskeysockets/baileys) dengan MultiFileAuthState untuk penyimpanan sesi login
   - Support multiple WhatsApp sessions (multi-device)
   - Auto reconnect jika koneksi terputus, kecuali logout permanen

2. **Contact & Message Management:**
   - Upload daftar nomor dari file CSV/TXT (1 nomor per baris, format internasional tanpa tanda +)
   - Import contacts dengan validasi nomor (hanya kirim ke nomor yang diawali 62 dan memiliki panjang minimal 10 digit)
   - Hapus duplikat nomor sebelum kirim
   - Support template pesan dari database atau file `message.txt`

3. **Media Support:**
   - Kirim gambar/foto promosi yang diupload via UI atau file `promo.jpg`
   - Support format JPG, PNG, WebP dengan compress otomatis
   - Preview media sebelum kirim

4. **Smart Sending System:**
   - Jeda random antar pengiriman (3–6 detik, bisa dikonfigurasi)
   - Queue system untuk pengiriman bertahap
   - Pause/resume campaign
   - Scheduling untuk kirim di waktu tertentu

5. **Logging & Monitoring:**
   - Real-time progress tracking di UI
   - Logging ke database dan file `logs.txt`
   - Status setiap pesan: berhasil/gagal/pending
   - Export laporan campaign (CSV, PDF)

6. **QR Code & Authentication:**
   - Generate QR code di web UI untuk login WhatsApp
   - Session management via web dashboard
   - Multi-user support dengan role-based access

## SvelteKit Fullstack Architecture:

7. **Frontend UI (Modern & Responsive):**
   - Dashboard untuk monitoring campaign
   - Contact management (upload, edit, delete, group)
   - Campaign builder dengan drag-drop message editor
   - Real-time status updates menggunakan Server-Sent Events (SSE)
   - File upload dengan drag-drop support
   - Dark/light mode toggle

8. **Backend API Structure:**
   - `/api/whatsapp/connect` - Connect WhatsApp session
   - `/api/whatsapp/disconnect` - Disconnect session
   - `/api/campaign/create` - Create new campaign
   - `/api/campaign/start` - Start campaign
   - `/api/campaign/pause` - Pause/resume campaign
   - `/api/contacts/upload` - Upload contact list
   - `/api/media/upload` - Upload media files

9. **Database Integration:**
   - Prisma ORM dengan PostgreSQL/SQLite
   - Models: Users, Campaigns, Contacts, Messages, Sessions
   - Migration scripts included

## Advanced Features:

10. **AI Integration:**
    - AI-powered message optimization menggunakan Claude/OpenAI
    - Auto-generate marketing message dari prompt
    - A/B testing untuk pesan dengan AI analytics
    - Smart contact segmentation

11. **Analytics & Reporting:**
    - Campaign performance dashboard
    - Delivery rate, open rate, response rate tracking
    - Export reports (PDF, Excel, CSV)
    - Real-time charts menggunakan Chart.js/D3

12. **Security & Rate Limiting:**
    - JWT authentication
    - API rate limiting untuk prevent spam
    - WhatsApp API compliance (hindari ban)
    - User permissions (admin, operator, viewer)

13. **Deployment Ready:**
    - Docker support dengan docker-compose
    - Environment configuration (.env)
    - Railway deployment config
    - Vercel/Netlify deployment untuk frontend

## Technical Requirements:

14. **Technology Stack:**
    - **Frontend:** SvelteKit + Tailwind CSS + TypeScript
    - **Backend:** SvelteKit server routes (Node.js)
    - **Database:** Prisma + PostgreSQL (Neon.tech support)
    - **WhatsApp:** @whiskeysockets/baileys
    - **UI Components:** Lucide icons, headless UI components
    - **Real-time:** Server-Sent Events (SSE) atau WebSocket

15. **File Structure Requirement:**
    ```
    src/
    ├── lib/
    │   ├── components/
    │   │   ├── ui/           # Reusable UI components
    │   │   ├── whatsapp/     # WhatsApp specific components
    │   │   └── dashboard/    # Dashboard components
    │   ├── server/
    │   │   ├── whatsapp.js   # Baileys integration
    │   │   ├── campaign.js   # Campaign management
    │   │   └── database.js   # Database operations
    │   ├── stores/           # Svelte stores for state management
    │   └── utils/            # Helper functions
    ├── routes/
    │   ├── +layout.svelte
    │   ├── +page.svelte      # Landing page
    │   ├── dashboard/        # Main dashboard
    │   ├── campaign/         # Campaign management
    │   ├── contacts/         # Contact management
    │   └── api/              # API endpoints
    ```

16. **Configuration Files:**
    - `.env.example` dengan semua environment variables
    - `numbers.txt` example file
    - `message.txt` template example
    - `docker-compose.yml` untuk development
    - `README.md` dengan instruksi lengkap

## Output yang Diinginkan:

1. **Complete SvelteKit Project** dengan semua file siap pakai
2. **Working Baileys Integration** yang sudah terintegrasi dengan UI
3. **Modern Dashboard** dengan real-time monitoring
4. **Deployment Instructions** untuk Railway, Vercel, dan Docker
5. **API Documentation** lengkap dengan contoh request/response
6. **User Manual** untuk operator dan admin

## Penekanan Penting:

- **UI/UX harus modern dan intuitif** setara aplikasi enterprise
- **Real-time updates** untuk semua campaign progress
- **Mobile responsive** dan touch-friendly
- **Error handling** yang robust dan user-friendly
- **Performance optimized** untuk handle ribuan kontak
- **Scalable architecture** siap untuk growth
- **Security first** dengan proper authentication & authorization

Tolong buatkan seluruh project lengkap dengan semua file yang diperlukan, siap deploy dan digunakan untuk bisnis WhatsApp marketing profesional.

### Bonus Features (jika memungkinkan):
- Integration dengan CRM (webhook support)
- Multi-language support
- Backup/restore campaign data
- Template marketplace
- White-label customization
- Advanced scheduling (timezone support)
- Auto-reply bot integration

Saya ingin sistem ini menjadi **solusi WhatsApp marketing terlengkap** dengan SvelteKit yang bisa bersaing dengan tools komersial di pasaran.
