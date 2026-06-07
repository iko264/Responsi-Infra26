# Analisis perbaikan
## Permasalahan 1

### Gejala
gejala pertama saat saya langsung build up semua gagal

### Penyebab
terdapan kesalahan ketik yang disengaja pada file docker-compose.yml

- yaml: line 5, column 8: mapping values are not allowed in this context
```
service
DB_PASS = wrongpassword
```
- service "db" refers to undefined volume db-data
```
database-data;
```
- salah path web3 -> web33
```
/web33
```
- web 2 dan 3 tidak ada frontend 
```

- backend
```
- kesalahan db di web1
```
DB_HOST = mysql
```
### Solusi
perbaiki menjadi seperti ini
```
service:

DB_PASSWORD = student123

db-data;

/web3
```
lalu tambah front end di sebelum backend web 2 dab 3
```
- backend
- frontend
```
lalu di db web 1 rubah menjadi seperti ini
```
DB_HOST = db
```

---

## Permasalahan 2

### Gejala
apche: not found
### Penyebab
terdapat kesalahan tusilan pada file dockerfile di beberapa folder web
```
FROM php:8.2-apach 
FROM php:8.2-apche
```
### Solusi
memperbaiki menjadi 
```
FROM php:8.2-apache
```
disetiap file dockerfile yang salah

---
## permasalahan 3
### gejala
unknown directive "``nginx"
### penyebab
terdapat `3x diawal dan akhir dan ada nginx nya setelah itu
### solusi 
hapus `3x dan nginx



