# Youtube Chat only CSS
This repository is trying to explain basic youtube chat style manipulation only using css.

## Cara Menggunakan contoh:
  1. Buka halaman file.
  2. klik raw
     ![image](https://github.com/miftahers/youtube-chat-css/assets/82572402/ec774c40-079c-4685-b712-648ad216d929)
  3. Copy semua tulisan
  4. Tempel di OBS

Anda dapat mengelompokkan bagian-bagian kode tersebut ke dalam beberapa kategori agar lebih mudah dimengerti. Berikut pengelompokan kode tersebut:

**Pengaturan Font dan Latar Belakang:**
```css
/* Mengimpor Font */
@import url("https://fonts.googleapis.com/css?family=Baloo");
@import url("https://fonts.googleapis.com/css?family=Buda");

/* Warna Latar Belakang */
body {
  overflow: hidden;
  background-color: rgba(0,0,0,1); /* Warna latar belakang utama */
}

/* Latar Belakang Transparan pada Chat */
yt-live-chat-renderer {
  background-color: transparent !important;
}
```

**Penanda pada Pesan Teks:**
```css
yt-live-chat-text-message-renderer::after {
  /* Garis samping kiri pesan teks biasa */
}

yt-live-chat-text-message-renderer[author-type="owner"]::after {
  /* Garis samping kiri pesan teks pemilik channel */
}

yt-live-chat-text-message-renderer[author-type="moderator"]::after {
  /* Garis samping kiri pesan teks moderator */
}

yt-live-chat-text-message-renderer[author-type="member"]::after {
  /* Garis samping kiri pesan teks anggota */
}
```

**Gaya Tampilan Chat:**
```css
/* Gaya Nama Pengirim */
yt-live-chat-author-chip #author-name {
  background-color: transparent !important;
}

/* Efek Shadow pada Teks */
yt-live-chat-renderer * {
  /* Efek bayangan pada teks */
  text-shadow: -2px -2px #000000, ...
  /* Pengaturan font dan ukuran teks */
  font-family: "Baloo";
  font-size: 18px !important;
  line-height: normal !important;
}
```

**Pengaturan Padding, Avatar, dan Badges:**
```css
/* Padding Samping */
yt-live-chat-text-message-renderer,
yt-live-chat-legacy-paid-message-renderer {
    padding-left: 20px !important;
  padding-right: 4px !important;
}

yt-live-chat-paid-message-renderer #header {
    padding-left: 20px !important;
  padding-right: 4px !important;
}

/* Avatar Pengirim */
yt-live-chat-text-message-renderer #author-photo,
yt-live-chat-paid-message-renderer #author-photo,
yt-live-chat-legacy-paid-message-renderer #author-photo {
  width: 24px !important;
  height: 24px !important;
  border-radius: 24px !important;
  margin-right: 6px !important;
}

/* Sembunyikan Badges */
yt-live-chat-text-message-renderer #author-badges {
  vertical-align: text-top !important;
}
```

**Gaya Timestamp, Badges, Nama Channel, dan Pesan:**
```css
/* Timestamp */
yt-live-chat-text-message-renderer #timestamp {
  display: inline !important;
  color: #999999 !important;
  font-family: "Buda";
  font-size: 16px !important;
  line-height: 16px !important;
}

/* Badges */
yt-live-chat-text-message-renderer #author-name[type="owner"],
yt-live-chat-text-message-renderer #author-name.owner,
yt-live-chat-text-message-renderer yt-live-chat-author-badge-renderer[type="owner"] {
  color: #ffd600 !important;
}

yt-live-chat-text-message-renderer #author-name[type="moderator"],
yt-live-chat-text-message-renderer #author-name.moderator,
yt-live-chat-text-message-renderer yt-live-chat-author-badge-renderer[type="moderator"] {
  color: #5e84f1 !important;
}

yt-live-chat-text-message-renderer #author-name[type="member"],
yt-live-chat-text-message-renderer #author-name.member,
yt-live-chat-text-message-renderer yt-live-chat-author-badge-renderer[type="member"] {
  color: #0f9d58 !important;
}

/* Nama Channel Pengirim */
yt-live-chat-text-message-renderer #author-name {
  color: #cccccc !important;
  font-family: "Baloo";
  font-size: 20px !important;
  line-height: 20px !important;
}

/* Pesan Teks */
yt-live-chat-text-message-renderer #message,
yt-live-chat-text-message-renderer #message * {
  color: #ffffff !important;
  font-family: "Baloo";
  font-size: 18px !important;
  line-height: normal !important;
  letter-spacing: normal !important;
}
```

**Sembunyikan atau Gaya Tampilan Khusus:**
```css
/* Sembunyikan Pesan Moderasi */
yt-live-chat-moderation-message-renderer {
  display: none !important;
}

/* Gaya Pesan Berbayar */
yt-live-chat-paid-message-renderer {
  margin: 4px 0 !important;
}

yt-live-chat-legacy-paid-message-renderer {
  background-color: #0f9d58 !important;
  margin: 4px 0 !important;
}

/* Sembunyikan Tautan (Links) dalam Pesan */
yt-live-chat-text-message-renderer a,
yt-live-chat-legacy-paid-message-renderer a {
  text-decoration: none !important;
}

/* Sembunyikan Pesan yang Telah Dihapus */
yt-live-chat-text-message-renderer[is-deleted],
yt-live-chat-legacy-paid-message-renderer[is-deleted] {
  display: none !important;
}
```

**Pengaturan Pesan Ticker dan Lainnya:**
```css
/* Gaya Tampilan Pesan Ticker */
yt-live-chat-ticker-renderer {
  background-color: transparent !important;
  box-shadow: none !important;
}

/* Gaya Teks dalam Pesan Ticker */
yt-live-chat-ticker-paid-message-item-renderer,
yt-live-chat-ticker-paid-message-item-renderer *,
yt-live-chat-ticker-sponsor-item-renderer,
yt-live-chat-ticker-sponsor-item-renderer * {
  color: #ffffff !important;
  font-family: "Baloo";
}

/* Sembunyikan Panel Aksi dan Reaksi */
yt-live-chat-action-panel-renderer, 
yt-live-chat-renderer #action-panel {
  display: none !important;
}

/* Sembunyikan Panel Kontrol Reaksi */
yt-reaction-control-panel-overlay,
yt-reaction-control-panel-overlay-view-model,
yt-reaction-control-panel-view-model {
  display: none !important;
}

/* Sembunyikan Pesan Viewer Engagement */
yt-live-chat-viewer-engagement-message-renderer {
  display: none !important;
}
```

Semoga pengelompokan ini membantu Anda memahami kode CSS tersebut dengan lebih baik. Kode tersebut digunakan untuk mengkustomisasi tampilan chat pada video YouTube.
