# Panduan Deployment Toko Aldi Sembako Landing Page

## 📋 Checklist Pre-Deployment

✅ Struktur file lengkap (index.html, assets/, robots.txt, sitemap.xml)  
✅ .gitignore sudah di-setup  
✅ .nojekyll sudah dibuat untuk GitHub Pages  
✅ Meta tags SEO lengkap (title, description, keywords)  
✅ Open Graph & Twitter Card metadata  
✅ JSON-LD structured data (LocalBusiness)  
✅ Favicon dan icons sudah dibuat  
✅ Responsive design tested  
✅ Aksesibilitas (alt text, aria labels)  

## 🚀 Cara Deploy ke GitHub Pages

### Step 1: Commit & Push ke GitHub

```bash
# Pastikan berada di branch feat-toko-aldi-landing-init
git status

# Add semua file
git add .

# Commit dengan pesan jelas
git commit -m "feat: Inisialisasi landing page Toko Aldi Sembako

- Tambah index.html dengan HTML5 semantik
- Implementasi Bootstrap 5.3.3, AOS, Animate.css
- Struktur assets (css, js, images)
- SEO advanced (meta tags, OG/Twitter Card, JSON-LD)
- Payment methods (Cash & QRIS)
- Google Maps embed
- Responsive design untuk mobile/tablet/desktop
- Aksesibilitas (ARIA labels, alt text)
- Sitemap.xml & robots.txt
"

# Push ke remote
git push origin feat-toko-aldi-landing-init
```

### Step 2: Merge ke Branch Main

```bash
# Checkout ke main
git checkout main

# Merge dari feature branch
git merge feat-toko-aldi-landing-init

# Push ke remote main
git push origin main
```

### Step 3: Aktivasi GitHub Pages

1. Buka repository di GitHub
2. Pergi ke **Settings** → **Pages** (menu sebelah kiri)
3. Di bagian **Source**:
   - Branch: Pilih `main`
   - Folder: Pilih `/ (root)`
4. Klik **Save**
5. Tunggu 1-2 menit untuk deployment selesai
6. URL akan muncul: `https://<username>.github.io/<repo-name>/`

### Step 4: Verifikasi Deployment

Cek apakah semua elemen berfungsi:

- [ ] Halaman utama terbuka dengan benar
- [ ] Navigation berfungsi (smooth scroll)
- [ ] CTA WhatsApp mengarah ke https://wa.me/6281233974201
- [ ] Google Maps embed tampil
- [ ] Animasi AOS berjalan
- [ ] Payment icons (Cash & QRIS) tampil
- [ ] Footer dengan tahun dinamis
- [ ] Back to top button muncul saat scroll
- [ ] Responsive di mobile/tablet/desktop
- [ ] Favicon tampil di browser tab
- [ ] Console browser tidak ada error

## 🔧 Penyesuaian URL

Jika nama repository atau username berbeda, update URL di:

### 1. `index.html`
Cari dan ganti semua instance:
```html
https://irfan3006.github.io/toko-aldi-sembako-landing/
```
Dengan:
```html
https://<your-username>.github.io/<your-repo-name>/
```

Lokasi yang perlu diupdate:
- Line 17: `og:url`
- Line 20: `og:image`
- Line 26: `twitter:url`
- Line 29: `twitter:image`
- Line 32: `canonical` link
- Line 33: `sitemap` link
- Line 74: JSON-LD `url`
- Line 75: JSON-LD `image`

### 2. `sitemap.xml`
Update URL di:
```xml
<loc>https://<your-username>.github.io/<your-repo-name>/</loc>
```

### 3. `robots.txt`
Update sitemap URL:
```
Sitemap: https://<your-username>.github.io/<your-repo-name>/sitemap.xml
```

### 4. README Files
Update link demo di README.md dan README-TOKO.md

## 📱 Test di Berbagai Device

### Desktop
- Chrome
- Firefox
- Safari
- Edge

### Mobile
- Chrome Mobile
- Safari iOS
- Samsung Internet

### Tablet
- iPad Safari
- Chrome Tablet

## 🔍 SEO Validation

### Google Rich Results Test
1. Buka: https://search.google.com/test/rich-results
2. Paste URL website Anda
3. Verifikasi LocalBusiness structured data valid

### Facebook Sharing Debugger
1. Buka: https://developers.facebook.com/tools/debug/
2. Paste URL website Anda
3. Verifikasi Open Graph metadata

### Twitter Card Validator
1. Buka: https://cards-dev.twitter.com/validator
2. Paste URL website Anda
3. Verifikasi Twitter Card preview

### Google PageSpeed Insights
1. Buka: https://pagespeed.web.dev/
2. Paste URL website Anda
3. Check performance score (target: >90)

## 🎯 Post-Deployment Tasks

### 1. Google Search Console
- Tambahkan property website
- Submit sitemap.xml
- Verifikasi ownership

### 2. Google My Business
- Claim business listing
- Update dengan URL website
- Sync jam operasional

### 3. Analytics (Opsional)
Jika ingin tracking visitor, tambahkan:
- Google Analytics 4
- Facebook Pixel (jika ada ads)

### 4. Social Media
Update bio/profil dengan link website:
- WhatsApp Business status
- Facebook page
- Instagram bio

## 🔐 Security Checklist

✅ HTTPS enabled (GitHub Pages default)  
✅ No sensitive data di repository  
✅ rel="noopener noreferrer" pada external links  
✅ Content Security Policy headers (optional)  

## 📊 Monitoring

### Metrics to Track
- Page load time
- Mobile usability
- Core Web Vitals
- Search ranking for keywords:
  - "toko sembako banguntapan"
  - "sembako bantul"
  - "toko sembako jalan janti"

### Monthly Review
- Check broken links
- Update promo section
- Review analytics data
- Update content jika perlu

## 🆘 Troubleshooting

### Issue: Website tidak muncul setelah deploy
**Solution:**
- Tunggu 5-10 menit
- Hard refresh browser (Ctrl+Shift+R)
- Check GitHub Pages settings
- Pastikan .nojekyll ada

### Issue: CSS/JS tidak load
**Solution:**
- Periksa paths relatif di index.html
- Clear browser cache
- Check CDN URLs masih valid

### Issue: Maps tidak tampil
**Solution:**
- Check iframe src URL
- Pastikan Google Maps API accessible
- Check console untuk CORS errors

### Issue: Animasi tidak berjalan
**Solution:**
- Periksa AOS library loaded (check Network tab)
- Pastikan script.js terpanggil
- Check console errors

### Issue: WhatsApp link tidak berfungsi
**Solution:**
- Format harus: https://wa.me/6281233974201
- Jangan ada spasi atau karakter aneh
- Test di mobile dan desktop

## 📞 Support

Jika ada masalah teknis:
1. Check dokumentasi di README-TOKO.md
2. Review STRUCTURE.md untuk detail file
3. Periksa console browser untuk errors
4. Contact developer via WhatsApp

---

## 🎉 Selamat!

Jika semua checklist di atas sudah ✅, maka landing page Toko Aldi Sembako sudah **live** dan siap menerima pengunjung!

**Live URL:** `https://<username>.github.io/<repo-name>/`

**Next Steps:**
1. Share URL ke customer via WhatsApp
2. Update Google My Business
3. Post di social media
4. Monitor traffic & feedback

---

**Created:** October 30, 2024  
**Version:** 1.0.0  
**Stack:** HTML5 + Bootstrap 5.3.3 + AOS + Animate.css
