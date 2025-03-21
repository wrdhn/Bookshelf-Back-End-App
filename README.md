# Bookshelf-Back-End-App
Submission Belajar Back-End Pemula dengan JavaScript By Dicoding

Bookshelf API adalah layanan berbasis RESTful API untuk mengelola daftar buku. API ini dapat digunakan untuk menyimpan, menampilkan, memperbarui, dan menghapus data buku.

## Fitur Utama

1. **Menyimpan Buku** → Endpoint untuk menambahkan buku baru.
2. **Menampilkan Semua Buku** → Endpoint untuk mendapatkan daftar buku.
3. **Menampilkan Detail Buku** → Endpoint untuk mendapatkan informasi buku berdasarkan ID.
4. **Memperbarui Buku** → Endpoint untuk mengubah data buku berdasarkan ID.
5. **Menghapus Buku** → Endpoint untuk menghapus buku berdasarkan ID.

## Teknologi yang Digunakan

- **Node.js** sebagai runtime JavaScript.
- **Hapi.js** sebagai framework backend.
- **Nanoid** untuk menghasilkan ID unik.

## Instalasi

1. Clone repositori ini:
   ```sh
   git clone https://github.com/username/bookshelf-api.git
   cd bookshelf-api
   ```
2. Instal dependensi:
   ```sh
   npm install
   ```
3. Jalankan server:
   ```sh
   npm run start
   ```
   Server akan berjalan di `http://localhost:9000`

## Endpoint API

### 1. Menyimpan Buku

- **Method:** `POST`
- **URL:** `/books`
- **Body Request:**
  ```json
  {
    "name": "Buku A",
    "year": 2010,
    "author": "John Doe",
    "summary": "Lorem ipsum dolor sit amet",
    "publisher": "Dicoding Indonesia",
    "pageCount": 100,
    "readPage": 25,
    "reading": false
  }
  ```
- **Response Berhasil (201):**
  ```json
  {
    "status": "success",
    "message": "Buku berhasil ditambahkan",
    "data": {
      "bookId": "1L7ZtDUFeGs7VlEt"
    }
  }
  ```

### 2. Menampilkan Semua Buku

- **Method:** `GET`
- **URL:** `/books`
- **Response Berhasil (200):**
  ```json
  {
    "status": "success",
    "data": {
      "books": [
        {
          "id": "Qbax5Oy7L8WKf74l",
          "name": "Buku A",
          "publisher": "Dicoding Indonesia"
        }
      ]
    }
  }
  ```

### 3. Menampilkan Detail Buku

- **Method:** `GET`
- **URL:** `/books/{bookId}`
- **Response Berhasil (200):**
  ```json
  {
    "status": "success",
    "data": {
      "book": {
        "id": "aWZBUW3JN_VBE-9I",
        "name": "Buku A",
        "year": 2011,
        "author": "Jane Doe",
        "summary": "Lorem Dolor sit Amet",
        "publisher": "Dicoding",
        "pageCount": 200,
        "readPage": 26,
        "finished": false,
        "reading": false,
        "insertedAt": "2021-03-05T06:14:28.930Z",
        "updatedAt": "2021-03-05T06:14:30.718Z"
      }
    }
  }
  ```

### 4. Memperbarui Buku

- **Method:** `PUT`
- **URL:** `/books/{bookId}`
- **Response Berhasil (200):**
  ```json
  {
    "status": "success",
    "message": "Buku berhasil diperbarui"
  }
  ```

### 5. Menghapus Buku

- **Method:** `DELETE`
- **URL:** `/books/{bookId}`
- **Response Berhasil (200):**
  ```json
  {
    "status": "success",
    "message": "Buku berhasil dihapus"
  }
  ```

## Menjalankan dalam Mode Development

Gunakan perintah berikut untuk menjalankan server dengan **nodemon**:

```sh
npm run start-dev
```

##

