# Dokumentasi Praktik ETL menggunakan Knime

# Business Understanding
Data yang digunakan berupa data rekap beberapa pertandingan game dota 2 pada very high skill. Data
dikumpulkan pada periode patch 7.22h sampai 7.22g. Dari data game tersebut didapatkan kombinasi dari 2
hero dota pada satu tim dan didapatkan presentasi kemenangan. Data tersebut dapat menunjukan kombinasi
hero dalam sebuah tim yang lagi trending. Dimana hero dengan kecocokan pola permainan dapat mendukung
tim unggul dan memenangkan sebuah pertandingan.

# Data Understanding
jumlah baris : 1438 baris
jumlah kolom : 4 kolom

1. berisikan nama hero pada sebuah tim di pertandingan
2. berisikan nama hero pada sebuah tim di pertandingan
3. presentasi kemenangan dari jika 2 hero diatas dalam satu tim dari beberapa pertandingan
4. jumlah pertandingan 2 hero tersebut bertemu dalam satu tim

# Data Preparation

1. Load data dari csv yang sudah menggunakan file reader ada pada gambar load_data_csv.png.
2. Data di split menjadi 2 bagian menggunakan 2 column spliter. Data berdasarkan pada kolom hero 
pertama, dan data pada kolom hero kedua yang ada pada gambar column_spliter.png.
3. kemudian dibuatkan tabel DB sesuai dengan kolom yang sudah di split menggunakan DB Tabel Creator
yang ada pada gambar db_tabel_creator.png.
4. isi data dimasukan kedalam tabel DB yang sudah dibuat menggunakan DB Writer yang ada pada gambar
db_writer.png.

# Modelling

1. dua tabel terpisah pada db digabung menjadi satu menggunakan Joiner yang dapat dilihat pada gambar
joiner.png.
2. Joiner menggunakan seting node yang dapat dilihat pada gambar joiner_node.png

# Evaluation

Hasil join dari kedua tabel pada DB telah berhasil yang kemudian akan di write kembali kedalam
csv dan tabel baru pada DB untuk melihat hasil join kedua tabel tersebut. Hasil join berhasil 
ditandai dengan lampu hijau yang menyala dibawah node.

# Deployment

1. Hasil dari join tabel di write kedalam csv menggunakan CSV Writer. Data tabel otomatis terbuat dan
tersimpan sesuai dengan lokasi dan nama file yang telah kita setel. Bagan dapat dilihat pada gambar 
csv_write.png
2. Hasil dari join tabel juga ditulis dengan mengguanakn tabel baru pada DB. Dengan menggunakan DB
Tabel Creator tabel terbuat secara otomatis sesuai dengan data tabel yang ada. Kemudian data ditulis
kedalam tabel menggunakan DB Writer. 

