---
lab:
  title: Menjelajahi AI generatif dengan Microsoft Copilot
---
# Menjelajahi AI generatif dengan Microsoft Copilot

Dalam latihan ini Anda akan menjelajahi AI generatif dengan Microsoft Copilot. 

## Masuk ke Microsoft Copilot

1. Buka [copilot.microsoft.com](https://copilot.microsoft.com?azure-portal=true) dan masuk dengan akun Microsoft pribadi Anda.

1. Microsoft Copilot menggunakan AI generatif untuk meningkatkan hasil pencarian Bing. Artinya, tidak seperti pencarian saja, yang mengembalikan konten yang ada, Microsoft Copilot dapat menyusun respons baru berdasarkan pemodelan bahasa alami dan informasi web.  

1. Menuju bagian bawah layar, Anda akan melihat jendela **Tanyakan apa pun** kepada saya. Saat Anda memasukkan perintah ke jendela, Copilot menggunakan seluruh utas percakapan untuk mengembalikan respons. Misalnya, mari kita coba mengajukan serangkaian pertanyaan tentang bepergian.

## Menggunakan perintah untuk menghasilkan respons

1. Ketik perintah: `What are 3 pros and cons of traveling in the winter?`. Anda akan melihat *Pencarian untuk: ...* dan *Menghasilkan ...* muncul sebelum respons. Model ini menggunakan respons yang dicari sebagai informasi dasar untuk menghasilkan respons asli. Perhatikan bahwa akhir respons berisi tautan ke sumbernya. 

![Cuplikan layar respons Copilot terhadap permintaan perjalanan dengan tiga poin untuk pro dan tiga poin untuk kontra.](./media/generative-ai/bing-copilot-response-traveling.png) 

> **Catatan**: Jika Anda tidak melihat pesan **Menghasilkan...* atau respons daftar poin, Anda belum bisa melihat Salinan dalam tindakan. Anda perlu kembali ke menu masuk dan menyambungkan akun saat ini yang Anda gunakan dengan akun pribadi. 
 
1. Ketik perintah: `Find me 3 more pros`. Apa yang Anda maksud dengan permintaan ini adalah bahwa Anda ingin melihat 3 alasan positif lagi untuk bepergian di musim dingin yang belum terdaftar. Perhatikan bahwa dengan perintah ini, Anda meminta Copilot untuk melakukan dua hal yang tidak dilakukan pencarian saja: gunakan respons obrolan sebelumnya untuk mengecualikan apa yang dikembalikan dalam respons baru, dan menggunakan topik obrolan sebelumnya tanpa secara eksplisit menyatakannya. 

1. Ketik perintah: `Where are 3 places I can go to find fewer crowds?`. 

    > **Catatan**: Perhatikan bahwa meskipun Copilot dapat memberikan respons terkait, copilot dapat menghilangkan "memori" sebelumnya dari utas percakapan saat berlanjut. Akibatnya, respons yang Anda dapatkan mungkin tidak terkait langsung dengan perjalanan di musim dingin. Ini sebagian besar berkaitan dengan batasan input token. Ketika obrolan "mengingat" bagian percakapan sebelumnya, itu karena telah menyimpan sejumlah token dari percakapan. Saat token baru diperkenalkan melalui perintah dan respons baru Anda, obrolan akan melepaskan token yang lebih lama. 

1. Tombol **Topik** Baru di samping jendela obrolan berguna. Mengkliknya akan menghapus utas percakapan sebelumnya sehingga respons topik baru Anda tidak didasarkan pada topik sebelumnya. **Gunakan ikon Topik** Baru di samping jendela obrolan untuk menghapus riwayat pesan Anda. 

## Coba pembuatan gambar

1. Sekarang mari kita lihat contoh pembuatan gambar. Ketik perintah: `Create an image of an elephant eating a hamburger`. Perhatikan bahwa pesan *yang akan saya coba buat...* muncul sebelum Copilot mengembalikan respons. 

    ![Cuplikan layar gajah makan hamgburger.](./media/generative-ai/dall-e-elephant.png)

    Yang penting, perhatikan bahwa respons mungkin terlihat mirip tetapi tidak sama. Ini karena respons bervariasi.  

1. Dalam respons, ada teks di bagian bawah yang berbunyi "Didukung oleh DALL-E". Pertimbangkan bagaimana DALL-E didasarkan pada model bahasa besar saat input bahasa alami Anda menghasilkan gambar. 

1. Kembali ke obrolan Copilot dengan mengklik ikon Microsoft Bing di sudut kanan atas layar. 

## Coba pembuatan kode

1. Sekarang mari kita lihat contoh pembuatan kode dan terjemahan. Ketik perintah: `Use Python to create a list`. 

1. Ketik perintah: `Translate that into C#`. Perhatikan bagaimana Anda tidak perlu menentukan "itu" apa yang diketahui Copilot untuk merujuk ke riwayat percakapan.

## Tugas bonus

1. Ketik perintah: `What are 3 examples of generative AI helping people?`. Anda dapat menggunakan ini sebagai cara untuk bertukar pikiran ide salinan Anda sendiri!  
