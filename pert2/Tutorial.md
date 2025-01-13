# Tutorial Lengkap NPM Packages

## Langkah 1: Buat Personal Access Token (PAT)

### Buka Pengaturan GitHub:

Masuk ke GitHub, lalu buka **Settings > Developer settings > Personal Access Tokens > Tokens (classic)**.

### Buat Token Baru:

1. Klik **Generate new token (classic)**.
2. Berikan nama token, atur scopes:
   - `read:packages`
   - `write:packages`
   - `repo` (jika repositori privat).

### Simpan Token:

Salin token yang dihasilkan dan buat file `.npmrc` dan bikin seperti dibawah ini:
- //npm.pkg.github.com/:_authToken="Ganti Dengan Token Yang Disalin Tanpa Petik"
@"Ganti Dengan Username/Nama Github Tanpa Petik":registry=https://npm.pkg.github.com

## Langkah 2 :

### WSL
1. `sudo apt update && sudo apt upgrade -y`
2. `sudo apt install -y nodejs npm`
3. verifikasi version : `npm -v`
4. `npm init -y`
5. Konfigurasi package.json :
- `{
  "name": "@(ganti dengan nama/username github tanpa kurung)/(ganti dengan nama repositorynya tanpa kurung)",
  "version": "1.0.0",
  "description": "Pada Repositories kali ini hanya akan ada markdown yang berisikan tutorial untuk Github, menginstall dan mengatur berbagai konfigurasi serta dokumentasi terkait penggunaan GitHub.",
  "keywords": [
    "tutorial"
  ],
  "main": "index.js",
  "scripts": {
    "postinstall": "echo 'Pergunakan dengan bijak ^_^'"
  },
  "author": "(ganti dengan nama/username github)",
  "license": "MIT",
  "dependencies": {
    "@(ganti dengan nama/username github tanpa kurung)/(ganti dengan nama repositorynya tanpa kurung)": "^(ganti versionnya tanpa kurung dengan contoh 1.0.0)"
  }
}`
6. `npm run build`
7. `npm publish --registry=https://npm.pkg.github.com`

## Cara Mengambil NPM Packages :
- Dipastikan direktori harus ada `.npmrc` -Nya
- `npm install @(ganti dengan nama/username github tanpa kurung)/(ganti dengan nama repositorynya tanpa kurung)@(ganti versionnya tanpa kurung dengan contoh 1.0.0)`