# **Pertemuan pertama**

pada pertemuan pertama mengenal sebuah fitur dalam github yaitu `Releases`

## Apa itu Releases?

Rilisan **memungkinkan pengguna mengunduh dan menyebarkan kode sumber proyek Anda sebagai satu paket dengan file biner dan catatan rilis** . Catatan rilis menjelaskan setiap perubahan, penyempurnaan, dan fitur baru yang terdapat dalam rilis. Rilisan bergantung pada tag git.

## Bagaimana cara menambahkan Releases pada Repo?

- [Non Linux](https://github.nih.gov/about/features/releases)
- **Linux** :
  - **Membuat/Memperbarui :**
    - `git tag -a v1.0.0 -m "Initial release"`
    - `git push origin v1.0.0`
  - **Menghapus :**
    - `git tag -d v1.0.0`
    - `git push --delete origin v1.0.0`
