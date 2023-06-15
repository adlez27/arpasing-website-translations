Note to translator: The current translation may be outdated and have missing content. Please check the English version below for reference.

---

# Tutorial Pembuatan Voicebank

Tutorial ini membahas cara rekaman dan OTO.

Meskipun kamu bisa rekaman dengan software apa saja, rekaman menggunakan OREMO jauh lebih mudah. Jika kamu tidak terbiasa, anggap ini sebagai kesempatan untuk belajar. Dan jika kamu berencana mengedit sampel, lakukan setelah rekaman.

Download resmi: [OSDN]()
Wine wrapper unduk Mac OS: [UTAForum]()
Terjemahan Inggris OREMO Mac: [UTAForum]()
(Aku merekomendasikan wine wrapper karena OREMO Mac tidak punya kotak comment.)

Jika kamu benar-benar tidak bisa menggunakan OREMO, rujuklah proposal PDF dalam unduhan ARPAsing dari situs Mr. Hua,. Scroll ke bawah untuk melihat reclist, dan beri nama tiap file dengan nomor pasangannya.

Untuk memulai, download reclist default terbaru dari [halaman reclist](). Kamu bisa memilih versi dengan atau tanpa indeks.


Jika kamu menggunakan reclist dengan indeks:
- Folder Berisi file reclist, file comment OREMO, dan file index.</
- Reclist mulai dari nomor 000 sampai 334
- OREMO comment file membantumu melihat fonem/kata sebenarnya yang berhubungan dengan masing-masing nomor.
- File index akan digunakan oleh Moresampler sebagai referensi saat OTO generating.

Jika kamu menggunakan reclist tanpa indeks:
- Folder berisi file reclist dan file comment OREMO.
- Reclist berisi fonem Arpabet.
- File comment OREMO membantumu melihat kata yang berhubungan dengan fonem
- Tidak ada file indeks karena Moresampler bisa membaca nama file dengan apa adanya.

Buat folder untuk voicebankmu dan copy-paste index.csv & OREMO-comment.txt ke sana. Buka reclist di OREMO, atur folder tujuan, dan mulailah merekam.

Kamu bisa merekam dengan/tanpa paduan BGM. Jika kamu menggunakan panduan BGM, aku sarankan untuk menggunakan BGM CVVC yang pendek seperti BGM CVVChinese atau VCCV English BGM.

File OREMO-comment akan memberi gambaran cara pengucapan dalam bentuk kalimat dan Arpabet. [Artikel pendek ini]() menjelaskan cara membaca dan melafalkan arpabet. Aslinya ini lumayan gampang! Jika kamu sudah sudah familiar dengan sistem fonetik lan seperti PaintedCZ atau X-SAMPA, rujuk grafik di [halaman ini]().

Selain string vokal, masing-masing string cuma punya 1 tipe huruf vokal. ketiga silabel akan berima.

Nyanyikan ketiga silabel dengan nada sama tanpa jeda seperti VCV. Jika ada "q"  atau tanda petik, itu berarti jeda singkat/glottal stop (contoh: akhiran 'k' dalam 'tokek').

Kamu bisa download voicebank yang ada di [direktori voicebank]() untuk referensi rekaman.

**UNTUK MULTIPITCH:** Di folder utama voicebank, pastikan ada pitch tanpa sufiks dalam .OTO. Pastikan pitch lain ada dalam subfoldernya sendiri.
Jangan menambahkan sufiks ke nama file karena Moresampler tidak bisa membuat .OTO dari nama file yang tidak tertera dalam index.csv.

**UNTUK SAMPEL EKSTRA:** Sampel tambahan yang bukan standar ARPAsing harus diletakkan dalam subfolder lain supaya mereka dapat memiliki file oto.ini yang terpisah. Hal ini akan memungkinkan ARPAsing Assistant untuk hanya membaca file oto.ini utama dengan entri OTO ARPAsing standar.

Lanjut ke OTO! Cukup drag & drop folder ke moresampler.exe untuk membuat file OTO dasar.

Ketik 3 lalu enter untuk memilih ARPAsing.
Saat diminta memberi nama duplikat, masukkan y/yes. Kapanpun ada kemiripan lirik dari sampel berbeda, seperti [s t], Moresampler akan memberi akhiran angka untuk membedakannya. (contoh: [s t2], [s t3], .dst)
Kamu juga bisa memasukkan suffix/akhiran. Harap diingat bahwa huruf kanji dan panah tidak bisa dimasukkan, jadi kamu harus menggunakan suffix seperti "S" atau "A#3".
(Jika kamu ingin menggunakan karakter spesial, gunakan placeholder, buka file oto.ini lalu 'Find + Replace'  Placeholder dengan suffix yang ingin kamu pakai.)

Jika kamu menggunakan Mac atau Linux, kamu harus menggunakan wine untuk menjalankan Moresampler. Buka terminal di folder tempat moresampler.exe, dan ketik:
"wine moresampler.exe / jalur / ke / voicebank".
Jika tidak bisa, jalankan Moresampler di windows atau minta teman yang punya Windows untuk membuatkan OTO dasar untukmu.

Sekarang OTO dasar sudah jadi, saatnya merapikan. Setiap entri OTO adalah difon, dua fonem. Umumnya, fonem pertama menyambung nada sebelumnya, sedangkan fonem kedua adalah fonem utama. Untuk OTO, pertama-tama cari daerah yang sesuai dengan fonem pertama, lalu lanjut ke fonem kedua.

## Fonem pertama

Mencakup offset berwarna biru dan overlap.

**[-]**

Jumlah overlap sama sekali tidak penting untuk bagian ini, karena not ini selalu muncul pada awal kalimat tepat setelah rest. Satu-satunya hal yang penting adalah not ini mencakup area sunyi.

**[c]**
*Plosive tanpa suara (p t k)*
Jika ini adalah fonem pertama dalam string, geser offset sehingga overlap berakhir sekitar 15msec sebelum konsonan.
Jika tidak, pindahkan offset ke akhir fonem di depannya. Pastikan fonem didepannya tidak terdengar lalu geser overlap sekitar 15msec sebelum konsonan.

*Plosive bersuara dan Affricate (b d g ch jh)*
Jika ini adalah fonem pertama dalam string, gerakkan offset sehingga overlap berakhir di tempat konsonan dimulai.
Jika ada fonem lain sebelum ini, pindahkan offset ke akhir fonem sebelumnya. Pastikan fonem sebelumnya tidak terdengar lalu geser overlap ke awal konsonan.

*Fricative, nasal, dan liquid (f v th dh s z sh zh hh m n ng l r)*
Geser offset ke awal konsonan dimulai. Untuk 'r', lihat bagian 'glides' untuk lebih lanjut.

*Glides/ Luncuran (y w)*
Konsonan ini sulit dilihat secara normal. Alihkan tampilan audio ke tampilan spectogram dengan mengklik tombol [s]. Konsonan ini hanyalah perubahan frekuensi(kerasnya suara) ke tingkat lebih kuat yang artinya, konsonan tersebut berada di area yang paling terang dalam spectogram.
Pindahkan offset ke tempat konsonan dimulai, lalu letakkan overlap di tempat yang konsisten sebelum perubahan frekuensi. Preutterance akan berakhir setelah perubahan.

**[v]**

Secara default, overlap sampel ini harus ada pada jumlah tertinggi. Jika jumlahnya ternyata sangat kecil, menggeser overlap sektiar 50ms akan cukup membantu.

Pindahkan offset awal sehingga daerah antaranya dan overlap berada di tingkat yang konsisten.

For diphthongs, the overlap should cover the area before the vowel changes.

## Fonem kedua

Harap diingat bahwa preutterance harus ditempatkan di akhir fonem pertama dan awal fonem kedua. Ini juga mencakup area pink, putih, dan biru.

**[c]**
*Stops (p b t d k g ch jh)*
Pastikan ada sunyi sesaat sebelum konsonan. Geser garis pink ke awal daerah sunyi dan cutoff ke akhir daerah sunyi. Ya, kita tidak memasukkan konsonannya. Karena dalam .UST not ini akan diikuti not yang MEMILIKI konsonan. Hal ini akan meberikan transisi yang mulus tanpa suara konsonan ganda.

*Frikatif (f v th dh s z sh zh hh)*
Tutupi seluruh konsonan dengan warna pink sampai tepat di dekat akhir konsonan. Geser cutoff ke area yang sama lalu tinggalkan sedikit celah. Tanpa celah ini, resampler tidak akan bisa merendernya. Namun, kita juga tidak ingin konsonan ini dipanjangkan.

Jika ada area sunyi setelah konsonan, masukkan mereka ke dalam area putih.

*Nasal, liquid dan luncuran (m n ng l r y w)*
Geser area pink ke tempat konsonan mulai stabil dan konsisten. Gunakan cutoff untuk menghapus konsonan yang memudar. Konsonan ini aman untuk dipanjangkan.

**[v]**
Geser area pink ke tempat vokal mulai stabil dan konsisten. Gunakan cutoff untuk menghapus vokal yang memudar. Area putih akan menjadi bagian not yang dipanjangkan, untuk memastikan hasil terdengar bagus.

Untuk difon antar huruf vokal, letakkan preutterance di akhir perubahan huruf vokal

Untuk Diftong, letakkan cutoff sebelum perubahan huruf vokal

**[-]**
Tutupi semua daerahdengan warna pink, sampai hanya ada sunyi di area putih.

Dan itu dia, voicebankmu sudah selesai. Jika kamu belum punya gambar untuk VBmu, Partial akan membuatkanmu secara gratis di [thread ini](). Kirimkan vb yang sudah dirilis ke direktori. Selamat bersenang-senang, semoga beruntung!

---

# Voicebank Creation Tutorial

This tutorial covers both recording and OTOing.

While you can use whatever you like to record, it will be much, much easier to use OREMO. If you're currently unfamiliar with how to use it, see this as an opportunity to learn how. If you plan to do sample processing, you'll have to do it after recording.  
Official download: [OSDN]()  
Wine wrapper for macOS: [UTAForum]()  
Mac native English translation: [UTAForum]()  
(I recommend the wine wrapper, because the mac native version doesn't have the comment box.)

To begin, download the latest default reclist from [the reclist page](). You can choose either the version with or without the index. If not using OREMO, the version without the index will be much easier to read.

If you are using the list with the index:
- The folder contains a reclist file, OREMO comment file, and index file.
- The reclist is numbers 000 to 334.
- The OREMO comment file allows you to see the actual phonemes or words that correspond with each number.
- The index file is for moresampler to reference when generating the OTO.

If you are using the list without the index:
- The folder contains a reclist file and OREMO comment file.
- The reclist contains arpabet phonemes.
- The OREMO comment file allows you to see the words that correspond with the phonemes.
- No index file is necessary, because moresampler can read the file names as-is.

Set up a folder for your voicebank, and copy+paste OREMO-comment.txt (and index.csv if applicable) into your new folder. In OREMO, open the reclist. Set the destination folder to your new folder.

You can record with or without guideBGM. If you want to use guideBGM, I recommend using a short one made for CVVC reclists, such as the CVVChinese BGMs or the VCCV English BGMs.

Note to translator: These next two lines were written for english speakers.

The comment file will tell you how to pronounce it approximately using words, and precisely using arpabet phonemes. [This short article]() will explain how to read and pronounce arpabet. It's actually pretty straightforward! If you're already familiar with another phonetic system like PaintedCZ's system or X-SAMPA, refer to the chart on [this page]().
Other than vowel strings, each string only has 1 type of vowel. All three syllables will rhyme.

Note to translator: Please write a new section here about how to properly pronounce English phonemes, for people who may be unfamiliar with them.

Sing the 3 syllables consecutively, as if recording VCV. If at any point there is a "q" in the phonetics (or an apostrophe in the words) it means a brief pause (a glottal stop).
For reference, you can download existing voicebanks from the [voicebank directory]().

**FOR MULTIPITCH:** The main voicebank folder must contain a pitch that does not have any suffixes. All other pitches must be placed in subfolders. When recording, do not add suffixes to the file names, or Moresampler won't be able to read the index.csv while OTOing.  
**FOR EXTRA SAMPLES:** Any extra samples that aren't standard in ARPAsing must be placed in a subfolder, so that they will have a separate oto.ini file. This enables ARPAsing Assistant to properly read the main oto.ini file with only standard ARPAsing OTO entries.

Onto OTOing! Simply drag and drop the folder onto moresampler.exe to do so.  
Enter 3 to choose arpasing. When prompted on renaming duplicates, enter y or yes. Whenever there are multiple of the same diphone, such as [s t], this will add a numeric suffix to the end of additional copies. This serves to distinguish each one from the other, as they may sound different based on the context of nearby phonemes in the string. You can also choose whether or not to include a suffix. It's not possible to use characters such as arrows or kanji, so you will have to use suffixes such as "S" or "A#3".

If you are using Mac or Linux, you will have to use wine to run Moresampler. Open terminal in the folder that moresampler.exe is in, and type "wine moresampler.exe /path/to/voicebank". If you're unable to do this, transfer your files to a windows computer, or ask a friend with Windows for help to generate it.

Now that your base OTO is generated, it's time to refine it. Every entry of the OTO is a diphone, meaning that there are only two phonemes or two sounds. In general, the first one is a connector to the previous note, while the second one is the main phoneme for the current note. To OTO, first find the section corresponding to the first phoneme, then find the section for the second phoneme.

## First phoneme

This covers the blue offset and overlap.

**[-]**  
The amount of overlap really doesn't matter for this one, because these notes always come at the beginning of a phrase, right after a rest. The only important thing is that it covers an area of silence.

**[c]**  
*Unvoiced plosives (p t k)*  
If this is the first phoneme in the string, move the offset such that the overlap ends up about 15msec before the consonant.
If there are other phonemes before this one, move the offset to where the previous one ended. Make sure you can't hear the previous one. Place the overlap about 15msec before the consonant.

*Voiced plosives and affricates (b d g ch jh)*  
If this is the first phoneme in the string, move the offset such that the overlap ends up where the consonant begins.  
If there are other phonemes before this one, move the offset to where the previous one ended. Make sure you can't hear the previous one. Place the overlap where the consonant begins.

*Fricatives, nasals, and liquids (f v th dh s z sh zh hh m n ng l r)*  
Move the offset to where the consonant begins. For 'r' in particular, you may want to refer to the glides section for help.

*Glides (y w)*  
These consonants can be difficult to see on a normal waveform. By clicking on the [s] button, you can switch to spectrogram view, which gives you another way to visualize the audio. The bright areas are the loudest frequencies. These consonants show up as a change in frequencies over time.  
Move the offset to where the consonant begins, then place the overlap where it's consistent before the change. The preutterance will end up after the change.

**[v]**  
By default, the overlap for these samples should be at a decently high amount. If it's absurdly small, moving it to around 50msec should be good.  
Move the initial offset so that the area between it and the overlap is at a consistent level.

For diphthongs, the overlap should cover the area before the vowel changes.

## Second Phoneme

For all cases, the preutterance should be placed where the first phoneme ends and second phoneme begins. This also covers the pink area, white area, and blue cutoff.

**[c]**  
*Stops (p b t d k g ch jh)*  
There should be a small bit of silence or near silence just before the consonant. Move the pink where the silence begins, and the cutoff to where the silence ends. Yes, we're not including the consonant itself. That's because, in a UST, this note would be followed by another note that DOES have the consonant. This allows for a smooth transition without an awkward double consonant sound.

*Fricatives (f v th dh s z sh zh hh)*  
Cover the entire consonant with pink until just before the end. Bring the cutoff to the same place, leaving a tiny gap. Without this gap, resamplers won't be able to render it. However, we don't want these consonants to be stretched.

If there is silence after the consonant, have the white area be silence instead.

*Nasals, liquids and glides (m n ng l r y w)*  
Move the pink to where the consonant starts being stable and consistent. Use the cutoff to remove where the consonant ends or fades out. These consonants are safe to stretch.

**[v]**  
Move the pink to where the vowel starts being stable and consistent. Use the cutoff to remove where the vowel fades out. The white area will be the sustained part of the note, which ensures that it will sound good.

For vowel-vowel diphones, place the preutterance at the end of the vowel change.

For diphthongs, place the cutoff before the vowel changes.

**[-]**  
Cover everything with pink, such that everything in white is silence.

And just like that, your voicebank is already done. Please submit any released banks to the directory. Have fun, good luck!
