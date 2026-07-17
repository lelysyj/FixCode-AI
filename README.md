# FixCode AI

## Deskripsi
FixCode AI adalah AI Agent berbasis IBM Bob yang membantu mahasiswa dan programmer memahami serta memperbaiki error pada kode Java, Python, C++, dan JavaScript.

## Latar Belakang
Mahasiswa dan programmer sering mengalami kesulitan memahami pesan error yang muncul saat menulis program. FixCode AI membantu menjelaskan penyebab error, memberikan solusi, contoh perbaikan kode, dan penjelasan konsep yang berkaitan.

## Target Pengguna
- Mahasiswa di bidang Informatika/TI
- Peserta bootcamp coding
- Programmer

## Fitur
- Analisis syntax error
- Analisis runtime error
- Analisis logic error
- Contoh perbaikan kode
- Penjelasan konsep pemrograman

## Teknologi
- IBM Bob
- Custom Mode (.yaml)

## Cara Menggunakan
1. Pilih mode **FixCode AI** di IBM Bob.
2. Kirim pesan error atau potongan kode.
3. AI akan memberikan:
   - Jenis Error
   - Penyebab
   - Solusi
   - Contoh Perbaikan Kode
   - Penjelasan Tambahan

## Prompt Iteration
### Versi Awal
Prompt hanya berisi instruksi untuk memperbaiki error sehingga hasil belum konsisten.

### Versi Akhir
Prompt diperbaiki dengan menambahkan:
- Persona (Senior Software Engineer)
- Format output
- Guardrails
- Batasan bahasa pemrograman
- Gaya bahasa yang mudah dipahami

## Hasil Pengujian

## Test Case 1 - Python (NameError)

**Input**
```python
print(hasil)
```

**Expected Result**
- Jenis Error: NameError
- Penyebab: Variabel `hasil` belum didefinisikan.
- Solusi: Definisikan variabel sebelum digunakan.
- Contoh Perbaikan Kode diberikan oleh AI.

**Status:** ✅ Passed

---

## Test Case 2 - Java (NullPointerException)

**Input**
```java
String nama = null;
System.out.println(nama.length());
```

**Expected Result**
- AI mengidentifikasi NullPointerException.
- Menjelaskan penyebab.
- Memberikan solusi dan contoh perbaikan.

**Status:** ✅ Passed

---

## Test Case 3 - JavaScript (ReferenceError)

**Input**
```javascript
console.log(data.nama);
```

**Expected Result**
- AI mengidentifikasi ReferenceError.
- Menjelaskan bahwa variabel `data` belum didefinisikan.
- Memberikan solusi dan contoh perbaikan.

**Status:** ✅ Passed

---

## Test Case 4 - C++

**Input**
```cpp
#include <iostream>

int main() {
    cout << "Hello";
}
```

**Expected Result**
- AI mengidentifikasi kesalahan karena `std::cout` atau `using namespace std;` belum digunakan.
- Memberikan contoh kode yang benar.

**Status:** ✅ Passed
