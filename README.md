# Aplikasi Absensi Menggunakan QR Code via Webcam Berbasis Desktop (Java NetBeans & MySQL)

Aplikasi ini adalah sistem absensi berbasis desktop yang memanfaatkan **QR Code** melalui **Webcam**, dibangun menggunakan **Java Swing** untuk antarmuka pengguna dan **MySQL** sebagai basis data.
Cocok digunakan untuk tugas akhir/skripsi, proyek sistem informasi, maupun implementasi absensi digital di sekolah.

> **Catatan:** File yang dibagikan di sini adalah versi demo. Jika ingin mendapatkan versi lengkap, dapat dibeli di [LYNK.ID KidouCode](https://lynk.id/kidoucode).

---

#### **Teknologi**
- [MySQL 8.0.40](https://downloads.mysql.com/archives/get/p/25/file/mysql-installer-community-8.0.40.0.msi)  
- [JDK 11](https://www.oracle.com/id/java/technologies/javase/jdk11-archive-downloads.html)  

Untuk menjalankan versi demo, cukup menggunakan **JDK 11**, karena database sudah di-host secara online.  
Namun, koneksi ke database mungkin mengalami keterlambatan.

---

#### **Library / Dependensi**

- **Timing Framework**
 - `TimingFramework-0.55.jar` → Library untuk animasi berbasis waktu di Java Swing, berguna untuk membuat transisi, efek fade, dan pergerakan elemen UI.  

- **Chart**
 - `jcommon-1.0.23.jar` → Library pendukung JFreeChart yang menyediakan utilitas umum untuk pengolahan data, formatting, dan struktur pendukung grafik.  
 - `jfreechart-1.0.19.jar` → Library untuk membuat berbagai jenis grafik (bar, line, pie, area, dll) di Java Swing atau aplikasi desktop lainnya.  

- **DatePicker**
- `miglayout-core.jar` → Versi inti MigLayout yang digunakan oleh DatePicker untuk penataan layout.  
- `miglayout-swing.jar` → Implementasi MigLayout untuk komponen Swing, mempermudah pengaturan tata letak DatePicker.  
- `swing-datetime-picker-1.2.3.jar` → Komponen Swing untuk memilih tanggal dan waktu (date & time picker).  

-**FlatLaf (Java Look and Feel)**
- `flatlaf-3.5.2-sources.jar` → Source code untuk FlatLaf (Look and Feel modern di Java).  
- `flatlaf-3.5.2.jar` → FlatLaf core, library Look and Feel modern dan minimalis untuk aplikasi Java Swing.  
- `flatlaf-extras-3.5.2.jar` → Add-on untuk FlatLaf seperti font customization, color palette, dan icon set tambahan.  
- `flatlaf-fonts-roboto-2.137.jar` → Font Roboto khusus untuk FlatLaf.  
- `flatlaf-intellij-themes-3.2.5.jar` → Tema tambahan yang menyerupai IntelliJ IDEA untuk FlatLaf.  
- `jsvg-1.4.0.jar` → Library untuk menampilkan gambar SVG di aplikasi Swing.  

- **Hashing**
- `jbcrypt-0.4.jar` → Library untuk melakukan hashing password menggunakan algoritma BCrypt.  

- **Jasper Report**
- `commons-beanutils-1.9.4.jar` → Utility untuk memanipulasi properti JavaBean (digunakan JasperReports).  
- `commons-collections4-4.4.jar` → Struktur data tambahan untuk koleksi Java (digunakan JasperReports).  
- `commons-digester-1.7.jar` → Parser XML berbasis aturan (rule-based XML parser) untuk JasperReports.  
- `commons-logging-1.3.0.jar` → Library logging generik yang digunakan JasperReports.  
- `groovy-4.0.16.jar` → Bahasa scripting Groovy, digunakan JasperReports untuk ekspresi dinamis.  
- `jasperreports-6.20.6.jar` → Core JasperReports untuk membuat laporan PDF, XLS, HTML, dll.  
- `jasperreports-fonts-7.0.1.jar` → Font tambahan untuk laporan JasperReports.  
- `opendf-1.3.3.0.jar` → Library untuk mengelola OpenDocument Format (ODF) di JasperReports.  

- **MigLayout**
- `miglayout-core-5.3.jar` → Core MigLayout untuk pengaturan tata letak fleksibel di Java.  
- `miglayout-swing-5.3.jar` → Implementasi MigLayout untuk komponen Swing.  

- **Modal Dialog**
- `modal-dialog-2.1.0.jar` → Library untuk membuat dialog kustom (popup) di Swing.  
- `modal-dialog-demo-2.1.0.jar` → Contoh implementasi modal dialog untuk referensi.  

- **MySQL Driver**
- `mysql-connector-j-8.0.31.jar` → Driver JDBC untuk koneksi Java dengan database MySQL.  

- **QR Code Scanner**
- `core-3.5.3.jar` → Library inti ZXing untuk pengolahan QR code.  
- `javase-3.5.3.jar` → Implementasi ZXing untuk aplikasi berbasis Java SE (QR code scanner di Swing).  

- **Webcam**
- `bridj-0.6.2-windows-only.jar` → Jembatan native code untuk akses hardware webcam di Windows.  
- `slf4j-api-1.6.2.jar` → API logging generik (diperlukan oleh webcam-capture).  
- `slf4j-log4j12-1.6.2.jar` → Implementasi SLF4J untuk log4j.  
- `webcam-capture-0.3.12.jar` → Library utama untuk menangkap gambar atau video dari webcam di Java Swing.  

---

#### **Fitur Utama**
- Input Data Teacher
- Input Data Class
- Input Data Student
- Absensi menggunakan QR Code (via webcam)
- Absensi manual (tanpa scan)
- Laporan absensi berdasarkan rentang tanggal (periode)

---

#### **Arsitektur Proyek (Package)**
- **Config** : Menangani konfigurasi koneksi aplikasi dengan database.  
- **DAO** : Implementasi logika akses data ke database, termasuk penerapan antarmuka service.  
- **Form** : Mengatur dan menampilkan data dalam bentuk tabel.  
- **Form Input** : Mengatur tampilan dan fungsi form untuk input data.  
- **Icon & Img** : Menyimpan ikon dan gambar yang digunakan aplikasi.  
- **Main** : Mengatur tampilan dan logika menu utama aplikasi.  
- **Model** : Mewakili struktur entitas sesuai tabel database.
- **Service** : Menyimpan logika bisnis untuk operasi CRUD, menghubungkan DAO dan UI.  
- **TableModel** : Model tabel khusus untuk `JTable`.  
- **Theme** : Menangani tema warna, gaya, dan layout aplikasi.  
- **Util** : Berisi fungsi-fungsi utilitas umum.  
- **Report** : Menyimpan file .jrxml dan .jasper.

---

#### **Instalasi & Menjalankan Aplikasi**

**1. Clone Repository**
```sh
git clone https://github.com/kidoucode/apps-absensi-qrcode-via-webcam-desktop.git
```

**2. Masuk ke Direktori Proyek** :

```sh
cd apps-absensi-qrcode-via-webcam-desktop
```

**3. Jalankan Aplikasi** :
```sh
java -jar AppsAbsensi_QRCode.jar
```
Atau Anda bisa langsung mengklik file JAR untuk menjalankan demo aplikasi ini.

**4. Login ke Aplikasi** :
```sh
Username : admin
Password : admin
```
Terima kasih

