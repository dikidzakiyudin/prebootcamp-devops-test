# Pre-Test Bootcamp DevOps

## knowledge base

1. Apa yang anda ketahui tentang DevOps?
2. Apa yang anda ketahui tentang Infrastructure?
3. Apa yang anda ketahui tentang server, sebutkan implementasi berserta contohnya?
4. Mengapa server dibutuhkan dalam pengembangan/development suatu software?
5. Apa yang anda ketahui mengenai Virtualisasi dan Container?
6. Mengapa teknology container saat ini sangat populer?
7. Apa yang anda ketahui tentang Orchestration Container System?

Cara pengerjaan, silahkan update file ini tulis jawabanya di bawah ini

1.sebuah prinsip developer untuk mengkoordinasikan antar tim yaitu tim development dengan tim operations dengan efektif dan efisien.

2.layanan yang yang di berikan sesuai permintaan di salah satu infrastruktur TI komputasi awan,  termasuk sumber daya perangkat keras dengan teknologi virtualisasi (CPU/memori/penyimpanan) melalui Internet.

3.yang saya ketahhui tentang server Server yaitu sistem komputer yang menyediakan sumber daya untuk penyimpanan data. Misalnya menampilkan website, mengirim email, dan lainnya.

4.karena jika ada server system tidak akan berjalan karna server penydia layanan di dalam sovware

5.yang saya ketahui tentang Virtualisasi yaitu sebuah proses berbasis software atau virtual, representasi dari sesuatu, baik itu aplikasi virtual, server, ruang penyimpanan, dan koneksi. Virtualisasi juga salah satu cara yang paling efektif untuk mengurangi ongkos IT sekaligus meningkatkan efisiensi untuk segala macam bisnis.

sedangkan untuk Container yaitu suatu alternative teknologi yang dapat di pergunakan untuk memvirtualisasi komputer system. Dengan mempergunakan Container kita dapat mengemas komputer programing menjadi suatu unit yang standard sehingga semua dependensi dari aplikasi dapat di ikut sertakan dalam kemasan tersebut.

6.karena container mulai populer seiring dengan meningkatnya pola pikir bahwa data sangat penting untuk sebuah organisasi. Seiring dengan berkembangnya teknologi, bisnis kini mulai beralih ke era aplikasi untuk memudahkan adaptasi dan resnos terhadap permintaan pelanggan.

7.yang saya ketahui tentang Orchestration Container System yaitu mengotomatiskan penerapan, pengelolaan, penskalaan, dan jaringan kontainer.

## Task 1 (Virtualization)

- Buatlah sebuah VM dengan kententuan
  - username: `<github_user>` contoh `dimasm93`
  - hostname: `<email_without_at>` contoh `dimas.tabeldata.com`
  - OS: `ubuntu-20.04` atau `centos-7`
- Install webserver `nginx`
- Buatlah web profile temen-temen kemudian deploy ke webserver nginx tersebut yang telah di deploy
  
(kirimkan hasil screenshotnya simpan dalam folder `screenshot` dengan nama `task1.png`)

## Task 2 (Container)

Jika saya memiliki architecture seperti berikut:

![container-apps](docs/images/01-container.png)

Dimana berikut adalah configurasi docker image:

1. Backend container
  - image: `dimmaryanto93/udemy-springboot-app:latest`
  - port: `8080`
  - env: 
    - `DATABASE_HOST`: `<ip-domain-db>`
    - `DATABASE_PORT`: `5432` 
    - `DATABASE_NAME`: `<db-name>`
    - `DATABASE_PASSWORD`: `<db-password>`
    - `APPLICATION_PORT`: `8080`
  need:
    - Database PostgreSQL v14.2
2. Frontend container
  - image: `dimmaryanto93/udemy-angular-app:latest`
  - port: `80`
  - env:
    - `APPLICATION_PORT`: `80`
    - `NGINX_ROOT_DOCUMENT`: `/var/www/html`
    - `BACKEND_HOST`: `<ip-backend-apps>`
    - `BACKEND_PORT`: `<port-backend-apps>`
    - `BACKEND_CONTEXT_PATH`: `/`
  - need:
    - Backend container

Silahkan buat docker-compose filenya, kemudian simpan dalam folder `tasks` dengan nama `docker-compose.yaml`

