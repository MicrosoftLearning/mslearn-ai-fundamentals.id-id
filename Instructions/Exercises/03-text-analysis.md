---
lab:
  title: Menganalisis teks di portal Azure AI Foundry
---

# Menganalisis teks di portal Azure AI Foundry

Azure AI Bahasa mencakup Analitik Teks, dengan kemampuan seperti pengenalan entitas, ekstraksi frasa kunci, ringkasan, dan analisis sentimen. Misalnya, agen perjalanan fiktif Margie's Travel mendorong pelanggan untuk mengirimkan ulasan tentang masa inap di hotel. Anda dapat menggunakan layanan Bahasa untuk mengekstrak entitas bernama, mengidentifikasi frasa kunci, meringkas teks, dan banyak lagi.

Dalam latihan ini, Anda akan menggunakan Bahasa Azure AI di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk menganalisis ulasan hotel. 

Latihan ini memakan waktu sekitar **20** menit.

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Cuplikan layar beranda portal Azure AI Foundry.](./media/ai-foundry-portal.png)

1. Gulir ke bagian bawah halaman, dan pilih petak **Jelajahi Layanan Azure AI**.

    ![Cuplikan layar petak Jelajahi Layanan Azure AI.](./media/ai-services.png)

1. Di halaman Layanan Azure AI, pilih petak **Bahasa + Penerjemah**.

    ![Cuplikan layar petak Bahasa + Penerjemah.](./media/language-tile.png)

1. Di halaman **Bahasa + Penerjemah**, pilih **Coba playground Bahasa**. Kemudian, saat diminta, buat proyek baru dengan pengaturan berikut:
    - **Nama proyek**: *Masukkan nama yang valid untuk proyek Anda.*
    - **Pengaturan tingkat lanjut**:
        - **Langganan**: *Langganan Azure Anda*
        - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
        - **Wilayah**: *Pilih wilayah **AI Foundry yang direkomendasikan***
        - **AI Foundry atau Azure OpenAI** *Buat sumber daya Azure AI Foundry baru dengan nama yang valid*

1. Pilih **Buat**. Tunggu proyek Anda dibuat. Proses ini memerlukan waktu beberapa menit.

1. Ketika proyek dibuat, Anda akan dibawa ke playground **Bahasa** (jika tidak, di panel tugas di sebelah kiri, pilih **Playground** dan buka playground Bahasa dari sana.)

    Playground bahasa adalah antarmuka pengguna yang memungkinkan Anda mencoba beberapa kemampuan Azure AI Bahasa.  

## Menggunakan Azure AI Bahasa untuk menganalisis teks

Azure AI Bahasa menawarkan berbagai kemampuan analisis teks.

### Mengekstrak entitas bernama dengan Azure AI Bahasa di portal Azure AI Foundry

*Entitas bernama* adalah kata-kata yang menggambarkan orang, tempat, dan objek dengan nama yang tepat. Mari kita gunakan kemampuan ekstraksi entitas bernama Azure AI Bahasa untuk mengidentifikasi jenis informasi dalam ulasan.

1. Di playground Bahasa, pilih **Ekstrak informasi**. Kemudian pilih petak **Ekstrak entitas bernama**. 

1. Di bawah *Sampel*, masukkan tinjauan berikut:

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. Pilih **Jalankan**. Tinjau output.

    ![Cuplikan layar antarmuka Ekstrak entitas bernama di playground Bahasa.](./media/entity-extraction.png)

    Perhatikan di bagian *Detail* bagaimana entitas yang diekstrak dilengkapi dengan informasi tambahan seperti jenis dan skor keyakinan. Skor keyakinan mewakili kemungkinan bahwa jenis yang diidentifikasi benar-benar termasuk dalam kategori tersebut.

### Mengekstrak frasa kunci dengan Azure AI Bahasa di portal Azure AI Foundry

*Frasa kunci* adalah bagian informasi terpenting dalam teks. Mari kita gunakan kemampuan ekstraksi frasa kunci Azure AI Bahasa untuk menarik informasi penting dari ulasan.

1. Di playground Bahasa, pilih **Ekstrak informasi**. Lalu pilih petak **Ekstrak frasa kunci**. 

1. Di bawah *Sampel*, masukkan tinjauan berikut:

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. Pilih **Jalankan**. Tinjau output.

    ![Cuplikan layar antarmuka Ekstrak frasa kunci di playground Bahasa.](./media/key-phrases.png)

    Perhatikan berbagai frasa yang diekstrak di bagian *Detail* . Frasa ini harus berkontribusi paling besar terhadap arti teks.

### Meringkas teks dengan Azure AI Bahasa di portal Azure AI Foundry
 
Mari kita lihat kemampuan ringkasan Azure AI Bahasa.

1. Di playground Bahasa, pilih **Ringkas informasi**, lalu pilih petak **Ringkas teks**.

1. Di bawah *Sampel*, masukkan tinjauan berikut:
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. Pilih **Jalankan**. Tinjau output.

    ![Cuplikan layar antarmuka Ringkas teks di playground Bahasa.](./media/summarize-text.png)

    Perhatikan *Ringkasan ekstraktif* dalam *Detail* yang memberikan skor peringkat untuk kalimat yang paling penting.

### Menganalisis sentimen dalam teks

Analisis sentimen adalah tugas umum saat menganalisis teks seperti ulasan hotel.

1. Di playground Bahasa, pilih **Klasifikasikan teks**. Lalu pilih petak **Analisis sentimen**.

1. Di bawah *Sampel*, masukkan tinjauan berikut:
    
    ```
    Disappointing Stay at The City Hotel
    The City Hotel, London
    9/5/2018
    My experience at The City Hotel in London was far from pleasant. The constant noise from nearby train tracks made it nearly impossible to sleep, with vibrations felt throughout the building. The rooms were outdated, dusty, and poorly maintained—dripping faucets, squeaky beds, and broken fixtures were just the beginning. Sound insulation was nonexistent, so every conversation from neighboring rooms was clearly audible. While the location near public transport was convenient and the staff were friendly, these positives couldn't make up for the overall discomfort and lack of value. I wouldn’t recommend this hotel to anyone seeking a restful or enjoyable stay.
    ```

1. Pilih **Jalankan**. Tinjau output.

    ![Cuplikan layar antarmuka Analisis sentimen di playground Bahasa.](./media/sentiment-analysis.png)

    Perhatikan bahwa analisis menghasilkan skor sentimen keseluruhan dan skor individu untuk setiap kalimat.

## Mendeteksi bahasa dan menerjemahkan teks

Azure AI Bahasa memungkinkan Anda mendeteksi bahasa pengantar teks. Selain itu, Azure AI Penerjemah memungkinkan Anda menerjemahkan teks dari satu bahasa ke bahasa lain dengan mudah.

### Mendeteksi bahasa

Mari kita mulai dengan mendeteksi bahasa pengantar ulasan.

1. Di panel **Klasifikasikan Teks**, pilih petak **Deteksi bahasa**.

1. Di bawah *Sampel*, masukkan tinjauan berikut:
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. Pilih **Jalankan**. Tinjau output.

    ![Cuplikan layar antarmuka Di bahasa komputer di playground Bahasa.](./media/detect-language.png)

    Perhatikan bahwa bahasa yang digunakan terdeteksi sebagai bahasa Prancis. 

### Terjemahkan teks

Mari kita terjemahkan ulasan dalam bahasa Prancis ke bahasa Inggris.

1. Di bagian atas halaman, gunakan tautan **&larr;** (kembali) di sebelah judul halaman **Playground Bahasa** untuk melihat semua playground yang tersedia.
1. Di daftar playground, buka **Playground Penerjemah**.
1. Di playground Penerjemah, pilih **Terjemahan teks**.
1. Di panel **Konfigurasikan**, pilih opsi bahasa berikut ini:
    - **Terjemahkan dari**: Prancis
    - **Terjemahkan ke**: Inggris
1. Di bawah *Sampel*, masukkan tinjauan dalam bahasa Prancis:
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. Pilih **Terjemahkan**. Tinjau output.

    ![Cuplikan layar antarmuka Terjemahan teks di playground Penerjemah.](./media/text-translation.png)

    Perhatikan bahwa ulasan dalam bahasa Prancis diterjemahkan ke bahasa Inggris.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com)dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih **Hapus grup sumber daya**, lalu **masukkan nama grup sumber daya** untuk mengonfirmasi. Grup sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman layanan Bahasa](https://learn.microsoft.com/azure/ai-services/language-service/overview).
