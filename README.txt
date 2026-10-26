CIGARS.AL POS v2 — SI TA PUBLIKOSH SI PWA

1) PARA SE TË NDRYSHOSH ADRESËN: në aplikacionin e vjetër bëj Cilësime > "Shkarko kopjen". Të dhënat ruhen për çdo adresë veçmas
   (skedar lokal, faqe https dhe aplikacioni i instaluar NUK i ndajnë të dhënat). Pas instalimit: Cilësime > "Rikthe nga skedar".
2) Ngarko të gjithë dosjen (index.html, sw.js, manifest.webmanifest, icons/) në një hosting https falas
   (p.sh. GitHub Pages, Netlify ose Cloudflare Pages). PWA kërkon https.
3) Windows: hap faqen në Edge/Chrome > ikona "Instalo" te shiriti i adresës.
   Android: Chrome > menyja > "Instalo aplikacionin".
   iPhone: Safari > Share > "Add to Home Screen" (vetëm Safari). Pas shtimit, rikthe backup-in brenda aplikacionit të instaluar.
4) Çdo pajisje ka të dhënat e veta derisa të bëhet sinkronizimi me server (hapi i vonuar). Mos shit paralelisht nga dy pajisje.

TESTET E REGRESIONIT (Node.js):
  cd tests
  node regression.js ../index.html                      (skenarë financiarë)
  node regression.js ../index.html backup.json --init   (ruan totalet e arta nga kopja reale)
  node regression.js ../index.html backup.json          (pas çdo ndryshimi: krahason totalet)
