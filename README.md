# Youtube Chat only CSS
This repository is trying to explain basic youtube chat style manipulation only using css.

## Cara Menggunakan contoh:
  1. Buka halaman file.
  2. klik raw
     ![image](https://github.com/miftahers/youtube-chat-css/assets/82572402/ec774c40-079c-4685-b712-648ad216d929)
  3. Copy semua tulisan
  4. Tempel di OBS


## ENGLISH

### Font Imports
```css
@import url("https://fonts.googleapis.com/css?family=Changa One");
@import url("https://fonts.googleapis.com/css?family=Imprima");
```
These lines import two Google Fonts, "Changa One" and "Imprima," which will be used for text styling later in the code.

### Background and Transparency
```css
body {
  overflow: hidden;
  background-color: rgba(0,0,0,0);
}
yt-live-chat-renderer {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer,
yt-live-chat-text-message-renderer[is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="owner"],
yt-live-chat-text-message-renderer[author-type="owner"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="moderator"],
yt-live-chat-text-message-renderer[author-type="moderator"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="member"],
yt-live-chat-text-message-renderer[author-type="member"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-author-chip #author-name {
  background-color: transparent !important;
}
```
These lines set the background colors to be transparent or semi-transparent for various elements within the live chat interface, such as the chat messages, author names, and chat container.

### Text Styling
```css
yt-live-chat-renderer * {
  text-shadow: ...;
  font-family: "Imprima";
  font-size: 18px !important;
  line-height: normal !important;
}
```
These lines apply text styling, including font, size, and shadow to various elements within the chat interface. It uses the "Imprima" font and sets a text shadow.

### Padding and Margins
```css
yt-live-chat-text-message-renderer,
yt-live-chat-legacy-paid-message-renderer {
    padding-left: 4px !important;
    padding-right: 4px !important;
}
yt-live-chat-paid-message-renderer #header {
    padding-left: 4px !important;
    padding-right: 4px !important;
}
yt-live-chat-text-message-renderer #author-photo,
yt-live-chat-paid-message-renderer #author-photo,
yt-live-chat-legacy-paid-message-renderer #author-photo {
  width: 24px !important;
  height: 24px !important;
  border-radius: 24px !important;
  margin-right: 6px !important;
}
```
These lines adjust padding, margins, and avatar size for various elements within the chat interface to control spacing and layout.

### Hide Elements
```css
yt-live-chat-header-renderer,
yt-live-chat-message-input-renderer {
  display: none !important;
}
yt-live-chat-moderation-message-renderer {
  display: none !important;
}
yt-live-chat-ticker-renderer,
yt-live-chat-ticker-renderer {
  display: none !important;
}
yt-live-chat-viewer-engagement-message-renderer {
  display: none !important;
}
yt-live-chat-banner-manager {
  display: none !important;
}
yt-live-chat-action-panel-renderer,
yt-live-chat-renderer #action-panel {
  display: none !important;
}
yt-reaction-control-panel-overlay,
yt-reaction-control-panel-overlay-view-model,
yt-reaction-control-panel-view-model {
  display: none !important;
}
yt-live-chat-viewer-engagement-message-renderer {
  display: none !important;
}
```
These lines hide various elements or components of the YouTube Live Chat interface, such as the header, message input, moderation messages, banners, action panels, and more.

### Text Color and Font for Different Roles
```css
yt-live-chat-text-message-renderer #author-name,
yt-live-chat-text-message-renderer #author-name::after {
  color: #cccccc !important;
  font-family: "Changa One";
  font-size: 20px !important;
  line-height: 20px !important;
}
```
These lines set the color, font, and size for the channel names in the chat, using the "Changa One" font.

### Message Styling
```css
yt-live-chat-text-message-renderer #message,
yt-live-chat-text-message-renderer #message * {
  color: #ffffff !important;
  font-family: "Imprima";
  font-size: 18px !important;
  line-height: normal !important;
  letter-spacing: normal !important;
}
```
These lines style the chat messages, including text color, font, size, line height, and letter spacing.

### SuperChat and Paid Messages Styling
```css
yt-live-chat-paid-message-renderer #author-name,
yt-live-chat-legacy-paid-message-renderer #event-text,
yt-live-chat-legacy-paid-message-renderer #event-text *,
yt-live-chat-paid-message-renderer #purchase-amount,
yt-live-chat-paid-message-renderer #purchase-amount *,
yt-live-chat-legacy-paid-message-renderer #detail-text,
yt-live-chat-legacy-paid-message-renderer #detail-text * {
  color: #ffffff !important;
  font-family: "Imprima";
  font-size: 18px !important;
  line-height: 18px !important;
}
```
These lines apply styling to SuperChat and paid messages, including text color, font, and size.

## BAHASA INDONESIA

### Impor Font
```css
/* Impor Font Google */
@import url("https://fonts.googleapis.com/css?family=Changa One");
@import url("https://fonts.googleapis.com/css?family=Imprima");
```
Baris-baris ini mengimpor dua jenis font dari Google, yaitu "Changa One" dan "Imprima," yang akan digunakan untuk mengganti tampilan teks nanti dalam kode.

### Warna Latar Belakang dan Transparansi
```css
/* Warna latar belakang dan transparansi */
/* Mengatur warna latar belakang menjadi transparan untuk berbagai elemen chat */
body {
  overflow: hidden;
  background-color: rgba(0,0,0,0);
}
yt-live-chat-renderer {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer,
yt-live-chat-text-message-renderer[is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="owner"],
yt-live-chat-text-message-renderer[author-type="owner"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="moderator"],
yt-live-chat-text-message-renderer[author-type="moderator"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="member"],
yt-live-chat-text-message-renderer[author-type="member"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-author-chip #author-name {
  background-color: transparent !important;
}
```
Baris-baris ini mengatur warna latar belakang agar menjadi transparan atau setengah transparan untuk berbagai elemen dalam antarmuka chat langsung YouTube, seperti pesan chat, nama pengirim, dan kontainer chat.

### Gaya Teks
```css
/* Gaya Teks */
/* Mengatur bayangan teks, jenis font, ukuran, dan ukuran garis untuk berbagai elemen chat */
yt-live-chat-renderer * {
  text-shadow: -2px -2px #000000, ... ; /* Bayangan teks untuk elemen-elemen */
  font-family: "Imprima"; /* Menetapkan jenis font */
  font-size: 18px !important; /* Menetapkan ukuran font */
  line-height: normal !important; /* Menetapkan tinggi baris */
}
```
Baris-baris ini mengatur gaya teks, termasuk jenis font, ukuran, dan bayangan teks untuk berbagai elemen dalam antarmuka chat.

### Padding dan Margin
```css
/* Akses padding dan margin */
/* Mengubah padding dan margin untuk elemen-elemen tertentu */
yt-live-chat-text-message-renderer,
yt-live-chat-legacy-paid-message-renderer {
    padding-left: 4px !important;
    padding-right: 4px !important;
}
yt-live-chat-paid-message-renderer #header {
    padding-left: 4px !important;
    padding-right: 4px !important;
}
yt-live-chat-text-message-renderer #author-photo,
yt-live-chat-paid-message-renderer #author-photo,
yt-live-chat-legacy-paid-message-renderer #author-photo {
  width: 24px !important;
  height: 24px !important;
  border-radius: 24px !important;
  margin-right: 6px !important;
}
```
Baris-baris ini mengatur padding, margin, dan ukuran avatar untuk berbagai elemen dalam antarmuka chat untuk mengontrol jarak dan tata letak.

### Menyembunyikan Elemen
```css
/* Menyembunyikan elemen */
/* Menyembunyikan berbagai elemen atau komponen antarmuka chat YouTube */
yt-live-chat-header-renderer,
yt-live-chat-message-input-renderer {
  display: none !important;
}
yt-live-chat-moderation-message-renderer {
  display: none !important;
}
yt-live-chat-ticker-renderer,
yt-live-chat-ticker-renderer {
  display: none !important;
}
yt-live-chat-viewer-engagement-message-renderer {
  display: none !important;
}
yt-live-chat-banner-manager {
  display: none !important;
}
yt-live-chat-action-panel-renderer,
yt-live-chat-renderer #action-panel {
  display: none !important;
}
yt-reaction-control-panel-overlay,
yt-reaction-control-panel-overlay-view-model,
yt-reaction-control-panel-view-model {
  display: none !important;
}
yt-live-chat-viewer-engagement-message-renderer {
  display: none !important;
}
```
Baris-baris ini menyembunyikan berbagai elemen atau komponen dari antarmuka chat langsung YouTube, seperti header, input pesan, pesan moderasi, banner, panel aksi, dan lainnya.

### Warna Teks dan Jenis Font untuk Peran yang Berbeda
```css
/* Warna teks dan jenis font untuk peran yang berbeda */
/* Menetapkan warna teks, jenis font, dan ukuran untuk nama saluran dalam chat menggunakan jenis font "Changa One" */
yt-live-chat-text-message-renderer #author-name,
yt-live-chat-text-message-renderer #author-name::after {
  color: #cccccc !important;
  font-family: "Changa One";
  font-size: 20px !important;
  line-height: 20px !important;
}
```
Baris-baris ini mengatur warna, jenis font, dan ukuran untuk nama saluran dalam chat, menggunakan jenis font "Changa One."

### Gaya Pesan
```css
/* Gaya Pesan */
/* Menyesuaikan pesan chat, termasuk warna teks, jenis font, ukuran, tinggi baris, dan jarak huruf */
yt-live-chat-text-message-renderer #message,
yt-live-chat-text-message-renderer #message * {
  color: #ffffff !important;
  font-family: "Imprima";
  font-size: 18px !important;
  line-height: normal !important;
  letter-spacing: normal !important;
}
```
Baris-baris ini mengatur gaya pesan chat, termasuk warna teks, jenis font, ukuran, tinggi baris, dan jarak huruf.
Tentu! Berikut adalah penjelasan dalam Bahasa Indonesia sebelum kode CSS lengkap:

### Impor Font
```css
/* Impor Font Google */
@import url("https://fonts.googleapis.com/css?family=Changa One");
@import url("https://fonts.googleapis.com/css?family=Imprima");
```
Baris-baris ini mengimpor dua jenis font dari Google, yaitu "Changa One" dan "Imprima," yang akan digunakan untuk mengganti tampilan teks nanti dalam kode.

### Warna Latar Belakang dan Transparansi
```css
/* Warna latar belakang dan transparansi */
/* Mengatur warna latar belakang menjadi transparan untuk berbagai elemen chat */
body {
  overflow: hidden;
  background-color: rgba(0,0,0,0);
}
yt-live-chat-renderer {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer,
yt-live-chat-text-message-renderer[is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="owner"],
yt-live-chat-text-message-renderer[author-type="owner"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="moderator"],
yt-live-chat-text-message-renderer[author-type="moderator"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-text-message-renderer[author-type="member"],
yt-live-chat-text-message-renderer[author-type="member"][is-highlighted] {
  background-color: transparent !important;
}
yt-live-chat-author-chip #author-name {
  background-color: transparent !important;
}
```
Baris-baris ini mengatur warna latar belakang agar menjadi transparan atau setengah transparan untuk berbagai elemen dalam antarmuka chat langsung YouTube, seperti pesan chat, nama pengirim, dan kontainer chat.

### Gaya Teks
```css
/* Gaya Teks */
/* Mengatur bayangan teks, jenis font, ukuran, dan ukuran garis untuk berbagai elemen chat */
yt-live-chat-renderer * {
  text-shadow: -2px -2px #000000, ... ; /* Bayangan teks untuk elemen-elemen */
  font-family: "Imprima"; /* Menetapkan jenis font */
  font-size: 18px !important; /* Menetapkan ukuran font */
  line-height: normal !important; /* Menetapkan tinggi baris */
}
```
Baris-baris ini mengatur gaya teks, termasuk jenis font, ukuran, dan bayangan teks untuk berbagai elemen dalam antarmuka chat.

### Padding dan Margin
```css
/* Akses padding dan margin */
/* Mengubah padding dan margin untuk elemen-elemen tertentu */
yt-live-chat-text-message-renderer,
yt-live-chat-legacy-paid-message-renderer {
    padding-left: 4px !important;
    padding-right: 4px !important;
}
yt-live-chat-paid-message-renderer #header {
    padding-left: 4px !important;
    padding-right: 4px !important;
}
yt-live-chat-text-message-renderer #author-photo,
yt-live-chat-paid-message-renderer #author-photo,
yt-live-chat-legacy-paid-message-renderer #author-photo {
  width: 24px !important;
  height: 24px !important;
  border-radius: 24px !important;
  margin-right: 6px !important;
}
```
Baris-baris ini mengatur padding, margin, dan ukuran avatar untuk berbagai elemen dalam antarmuka chat untuk mengontrol jarak dan tata letak.

### Menyembunyikan Elemen
```css
/* Menyembunyikan elemen */
/* Menyembunyikan berbagai elemen atau komponen antarmuka chat YouTube */
yt-live-chat-header-renderer,
yt-live-chat-message-input-renderer {
  display: none !important;
}
yt-live-chat-moderation-message-renderer {
  display: none !important;
}
yt-live-chat-ticker-renderer,
yt-live-chat-ticker-renderer {
  display: none !important;
}
yt-live-chat-viewer-engagement-message-renderer {
  display: none !important;
}
yt-live-chat-banner-manager {
  display: none !important;
}
yt-live-chat-action-panel-renderer,
yt-live-chat-renderer #action-panel {
  display: none !important;
}
yt-reaction-control-panel-overlay,
yt-reaction-control-panel-overlay-view-model,
yt-reaction-control-panel-view-model {
  display: none !important;
}
yt-live-chat-viewer-engagement-message-renderer {
  display: none !important;
}
```
Baris-baris ini menyembunyikan berbagai elemen atau komponen dari antarmuka chat langsung YouTube, seperti header, input pesan, pesan moderasi, banner, panel aksi, dan lainnya.

### Warna Teks dan Jenis Font untuk Peran yang Berbeda
```css
/* Warna teks dan jenis font untuk peran yang berbeda */
/* Menetapkan warna teks, jenis font, dan ukuran untuk nama saluran dalam chat menggunakan jenis font "Changa One" */
yt-live-chat-text-message-renderer #author-name,
yt-live-chat-text-message-renderer #author-name::after {
  color: #cccccc !important;
  font-family: "Changa One";
  font-size: 20px !important;
  line-height: 20px !important;
}
```
Baris-baris ini mengatur warna, jenis font, dan ukuran untuk nama saluran dalam chat, menggunakan jenis font "Changa One."

### Gaya Pesan
```css
/* Gaya Pesan */
/* Menyesuaikan pesan chat, termasuk warna teks, jenis font, ukuran, tinggi baris, dan jarak huruf */
yt-live-chat-text-message-renderer #message,
yt-live-chat-text-message-renderer #message * {
  color: #ffffff !important;
  font-family: "Imprima";
  font-size: 18px !important;
  line-height: normal !important;
  letter-spacing: normal !important;
}
```
Baris-baris ini mengatur gaya pesan chat, termasuk warna teks, jenis font, ukuran, tinggi baris, dan jarak huruf.

### Gaya SuperChat dan Pesan Berbayar
```css
/* Gaya SuperChat dan Pesan Berbayar */
/* Menyesuaikan gaya SuperChat dan pesan berbayar, termasuk warna teks dan jenis font */
yt-live-chat-paid-message-renderer #author-name,
yt-live-chat-legacy-paid-message-renderer #event-text,
yt-live-chat-legacy-paid-message-renderer #event-text *,
yt-live-chat-paid-message-renderer #purchase-amount,
yt-live-chat-paid-message-renderer #purchase-amount *,
yt-live-chat-legacy-paid-message-renderer #detail-text,
yt-live-chat-legacy-paid-message-renderer

 #detail-text * {
  color: #ffffff !important;
  font-family: "Imprima";
  font-size: 18px !important;
  line-height: 18px !important;
}
```
Baris-baris ini mengatur gaya SuperChat dan pesan berbayar, termasuk warna teks dan jenis font.

Kode CSS ini disesuaikan untuk mengubah tampilan dan perilaku berbagai elemen dalam antarmuka chat langsung YouTube, memungkinkan Anda untuk membuat pengalaman chat yang unik dan personal.
