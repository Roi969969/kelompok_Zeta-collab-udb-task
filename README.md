# kelompok_Zeta-collab-udb-task
kelompok_Zeta-collab-udb-task

1. Deskripsi

Branch Dev 2 berisi pembuatan layanan database menggunakan PostgreSQL + Adminer. Semua penamaan database, tabel, container, dan network menggunakan identitas zeta sesuai ketentuan tugas kolaborasi.

2. Layanan yang Dibangun

zeta-postgres → Database PostgreSQL

zeta-adminer → GUI Adminer

Network: kelompok_zeta-collab-udb-task_zeta-net-postgres

3. Konfigurasi Utama

PostgreSQL

User: zeta_user

Password: zeta_pass

Database: zeta_db

Port: 5432

Adminer

URL akses: http://localhost:8082

Server: zeta-postgres

4. Struktur Database

Tabel identitas kelompok Zeta:

1. zeta_users

id (SERIAL, PK)

username (VARCHAR)

role_zeta (VARCHAR)

2. zeta_logs

id (SERIAL, PK)

activity (TEXT)

created_at (TIMESTAMP)

5. Cara Menjalankan
docker compose up -d
docker ps
docker network ls


Masuk ke database:

docker exec -it zeta-postgres bash
psql -U zeta_user -d zeta_db

6. Status Dev 2

✔ Container berjalan
✔ Network sesuai modul
✔ Database + tabel selesai
✔ Siap diintegrasikan oleh Maintainer