# Konversi VCCV ke ARPAsing

Reclist VCCV English milik PaintedCZ adalah reclist yang populer di komunitas UTAU luar negeri, dengan banyaknya Voicebank dan .UST dalam format tersebut, sekarang Voicebank dan .UST VCCV bisa dikonversikan ke dalam standar ARPAsing.

## Konversi voicebank

Struktur pengaturan voicebank VCCV asli memisahkan sampel-sampel menjadi beberapa subfolder bernama "CC-", "CV_CVC", dan seterusnya.  Semua sampel harus dipindahkan ke dalam folder utama Voicebank. Download file indesknya [di sini]() dan ganti namanya menjadi "index.csv", lalu tambahkan ke dalam folder.  
Sekarang kamu bisa drag and drop foldernya ke dalam Moresampler untuk OTO generation. Akan tetapi, **jangan menamai ulang/menomori duplikat** karena hal tersebut akan menciptakan ratusan duplikat yang menyebabkan ARPAsing Assistant tidak berfungsi dengan baik. Download [tool ini]() untuk menghapus duplikat berlebih dari OTO yang telah di-generate, jumlah maksimum duplikat yang disarankan adalah 10 - 20.

## Konversi .UST

Download [plugin ini](), unzip dan tempatkan ke folder plug-in tempat UTAU terinstall. Plug-in ini akan mengkonversi .UST dalam fonem CZ menjadi fonem Arpabet. Akan tetapi, hasil konversi tidak akan langsung sesuai Voicebank (Contoh: Not mungkin bisa memiliki lebih dari 2 fonem) sehingga kamu harus melakukan penyesuaian secara manual.  
Plugin Original oleh ChieP  
Konverter terinspirasi dari @TheIvoryShield  
Modifikasi Plug-in oleh KLAD