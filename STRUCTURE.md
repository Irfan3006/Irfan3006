# Struktur Proyek Toko Aldi Sembako Landing Page

```
toko-aldi-sembako-landing/
├── index.html                          # Halaman utama landing page
├── .gitignore                         # File yang diabaikan oleh Git
├── .nojekyll                          # Menonaktifkan Jekyll processing di GitHub Pages
├── robots.txt                         # File robots untuk SEO crawler
├── sitemap.xml                        # Sitemap XML untuk SEO
├── README.md                          # README profil GitHub asli
├── README-TOKO.md                     # Dokumentasi lengkap proyek landing page
├── STRUCTURE.md                       # Dokumentasi struktur file (this file)
│
├── assets/                            # Folder aset
│   ├── css/
│   │   └── styles.css                # Custom CSS dengan desain minimalis clean
│   │
│   ├── js/
│   │   └── script.js                 # JavaScript untuk AOS, smooth scroll, utilities
│   │
│   └── images/                       # Aset gambar dan ikon
│       ├── favicon.svg               # Favicon SVG (modern)
│       ├── favicon.png               # Favicon PNG 32x32
│       ├── apple-touch-icon.png      # Apple touch icon 180x180
│       ├── og-image.jpg              # Open Graph image 1200x630
│       ├── hero-illustration.svg     # Ilustrasi hero section
│       ├── payment-cash.svg          # Ikon pembayaran Cash
│       └── payment-qris.svg          # Ikon pembayaran QRIS

```

## 📄 Penjelasan File

### Root Level Files

#### `index.html`
File HTML utama yang berisi seluruh konten landing page dengan:
- HTML5 semantik
- Bootstrap 5.3.3 via CDN
- AOS (Animate On Scroll) library
- Animate.css untuk animasi
- Bootstrap Icons
- SEO meta tags lengkap
- Open Graph & Twitter Card metadata
- JSON-LD structured data (LocalBusiness schema)

**Sections:**
1. Navigation - Fixed top navbar
2. Hero - Headline, subheadline, CTA buttons, payment badges
3. Press & Reviews - Liputan Medium dan ulasan Google Maps
4. About - Pengalaman belanja (paragraf panjang)
5. Operating Hours - Jadwal buka Senin-Minggu
6. Location - Alamat lengkap + Google Maps embed
7. Promo - Placeholder untuk promo
8. Footer - Kontak dan links

#### `.gitignore`
Daftar file dan folder yang diabaikan oleh Git:
- OS files (macOS .DS_Store, Windows Thumbs.db)
- Editor configs (.vscode, .idea)
- Dependencies (node_modules, .venv)
- Build outputs
- Temporary files

#### `.nojekyll`
File kosong yang memberitahu GitHub Pages untuk tidak menggunakan Jekyll static site generator. Diperlukan agar struktur folder dan aset tetap seperti yang diinginkan.

#### `robots.txt`
Memberitahu search engine crawler file mana yang boleh diakses. Saat ini allow semua dan mengarahkan ke sitemap.xml.

#### `sitemap.xml`
Sitemap XML untuk membantu search engines mengindex halaman website dengan lebih baik.

#### `README-TOKO.md`
Dokumentasi lengkap proyek landing page termasuk:
- Penjelasan fitur
- Teknologi yang digunakan
- Cara deploy ke GitHub Pages
- Panduan customization
- Troubleshooting

#### `STRUCTURE.md`
Dokumentasi ini - menjelaskan struktur file dan folder.

### Assets Folder

#### `assets/css/styles.css`
Custom CSS dengan:
- CSS variables untuk warna tema (primary, secondary, accent)
- Override Bootstrap classes
- Custom navbar styling
- Hero section dengan gradient background
- Card hover effects (hover-lift)
- Schedule list styling
- Address info styling
- Back to top button
- Responsive breakpoints
- Accessibility focus states
- Print styles
- Smooth transitions

**Design Philosophy:**
- Minimalis clean: latar putih, ruang putih luas
- Aksen hijau/teal (#2D9C7F, #1A7A5E, #45B39D)
- Bayangan lembut (soft shadows)
- Typography nyaman dibaca

#### `assets/js/script.js`
Custom JavaScript untuk:
- Inisialisasi AOS (Animate On Scroll)
- Smooth scroll untuk anchor links internal
- Back to top button functionality (show/hide on scroll)
- Dynamic year di footer (copyright)

**Dependencies:**
- AOS library (via CDN)
- Bootstrap 5 JS (via CDN)

#### `assets/images/`
Folder berisi semua aset visual:

**favicon.svg** (32x32)
- SVG favicon dengan huruf "A" (Aldi)
- Warna background: #2D9C7F
- Text putih, bold

**favicon.png** (32x32)
- PNG fallback untuk favicon
- Generated dengan Pillow

**apple-touch-icon.png** (180x180)
- Icon untuk perangkat Apple (iPhone/iPad home screen)
- Generated dengan Pillow

**og-image.jpg** (1200x630)
- Open Graph image untuk social media sharing
- Dimensions sesuai standar Facebook/Twitter
- Menampilkan "Toko Aldi Sembako"
- Generated dengan Pillow

**hero-illustration.svg**
- Ilustrasi SVG custom untuk hero section
- Menampilkan shopping cart dengan desain minimalis
- Gradient warna hijau/teal
- Floating animation via CSS

**payment-cash.svg**
- Icon SVG untuk metode pembayaran Cash
- Desain bill/uang dengan circle accent
- Warna: #2D9C7F gradient

**payment-qris.svg**
- Icon SVG untuk metode pembayaran QRIS
- Desain QR code stylized
- Warna: #0066CC (biru)

## 🎨 Desain & Branding

### Palet Warna
```css
--primary-color: #2D9C7F;      /* Teal/Hijau utama */
--secondary-color: #1A7A5E;    /* Hijau tua */
--accent-color: #45B39D;       /* Teal terang */
--text-dark: #2C3E50;          /* Text gelap */
--text-muted: #6C757D;         /* Text muted abu */
--light-bg: #F8F9FA;           /* Background terang */
```

### Typography
- **Font Family**: Inter (Google Fonts)
- **Weights**: 300, 400, 500, 600, 700
- **Fallback**: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif

### Spacing & Layout
- **Container**: Bootstrap container responsif
- **Grid**: Bootstrap 12-column grid system
- **Gutters**: Bootstrap default (g-4 untuk section spacing)
- **Section Padding**: py-5 (3rem vertical padding)

### Icons
- **Library**: Bootstrap Icons 1.11.3
- **Usage**: Inline dengan teks, decorative untuk cards
- **Color**: Mengikuti context (primary, success, etc.)

## 🚀 Teknologi Stack

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Custom styles + Bootstrap override
- **JavaScript (ES6+)** - Vanilla JS untuk interactivity

### Frameworks & Libraries
- **Bootstrap 5.3.3** - CSS framework via CDN
- **AOS 2.3.1** - Animate On Scroll library
- **Animate.css 4.1.1** - CSS animations
- **Bootstrap Icons 1.11.3** - Icon library
- **Google Fonts** - Inter typeface

### SEO & Performance
- **Meta Tags** - Title, description, keywords
- **Open Graph** - og:* tags untuk social sharing
- **Twitter Card** - twitter:* tags
- **JSON-LD** - Structured data (LocalBusiness)
- **Sitemap.xml** - XML sitemap
- **Robots.txt** - Search crawler instructions
- **Preconnect** - Resource hints untuk CDN
- **DNS-prefetch** - DNS prefetch untuk performance
- **Lazy Loading** - Images dan iframe

## 📱 Responsive Breakpoints

```css
/* Mobile-first approach */
< 768px   : Mobile devices
768-992px : Tablet devices
> 992px   : Desktop devices
```

### Adaptasi per Device
- **Mobile**: Single column layout, stacked cards, hamburger menu
- **Tablet**: 2-column grid untuk cards, collapsed navbar
- **Desktop**: Multi-column layout, full navbar, optimal spacing

## ♿ Accessibility

### Implementasi
- **Semantic HTML**: Header, nav, section, article, footer
- **ARIA labels**: aria-label untuk link dan button
- **Alt text**: Semua gambar memiliki alt text deskriptif
- **Focus states**: Visible outline untuk keyboard navigation
- **Color contrast**: Memenuhi WCAG AA standard
- **Heading hierarchy**: Proper H1-H6 structure

## 🔍 SEO Features

### On-Page SEO
✅ Title tag dengan keywords lokal
✅ Meta description informatif
✅ Meta keywords (sembako, Banguntapan, Bantul, Yogyakarta)
✅ H1-H6 heading structure
✅ Alt text pada semua gambar
✅ Internal linking (anchor links)
✅ Clean URL structure

### Technical SEO
✅ Semantic HTML5
✅ Mobile responsive
✅ Fast load time (CDN, optimization)
✅ HTTPS ready
✅ Sitemap.xml
✅ Robots.txt
✅ Structured Data (JSON-LD)

### Local SEO
✅ LocalBusiness schema
✅ Address markup
✅ Geo coordinates
✅ Phone number
✅ Opening hours
✅ Payment methods
✅ Google Maps embed

## 📊 Performance Optimization

### Techniques Used
- **CDN**: Bootstrap, AOS, fonts dari CDN tercepat
- **Preconnect**: Resource hints untuk CDN
- **DNS-prefetch**: Early DNS resolution
- **Lazy loading**: Images dan iframe Maps
- **Minification**: Production CSS/JS akan di-minify
- **Compression**: Server akan compress dengan gzip/brotli
- **Caching**: Browser caching untuk static assets

### File Sizes (Approximate)
- HTML: ~30KB (uncompressed)
- CSS: ~12KB (uncompressed)
- JS: ~3KB (uncompressed)
- Images: Optimized SVG/PNG (<100KB total)

## 🔄 Update & Maintenance

### Cara Update Konten
1. Edit `index.html` untuk text/content changes
2. Edit `assets/css/styles.css` untuk styling changes
3. Edit `assets/js/script.js` untuk behavior changes
4. Replace images di `assets/images/` untuk visual updates

### Git Workflow
```bash
git add .
git commit -m "Update: [deskripsi perubahan]"
git push origin main
```

### GitHub Pages Auto-Deploy
- Push ke branch `main` otomatis trigger rebuild
- Wait 1-2 menit untuk changes live
- Check di https://irfan3006.github.io/toko-aldi-sembako-landing/

## 📞 Informasi Kontak

**Toko Aldi Sembako**
- Alamat: Jl. Janti Gg. Harjuna No. 45, Banguntapan, Bantul, DIY 55198
- Telepon: +62 812-3397-4201
- WhatsApp: https://wa.me/6281233974201
- Jam Buka: 06.30 - 23.00 (Setiap Hari)
- Koordinat: -7.79021, 110.408922

---

**Last Updated**: October 30, 2024
**Version**: 1.0.0
**Developer**: Created for Toko Aldi Sembako
