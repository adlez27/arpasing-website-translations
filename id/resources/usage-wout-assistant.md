Note to translator: The current translation may be outdated and have missing content. Please check the English version below for reference.

---

# Tutorial Penggunaan Voicebank tanpa ARPAsing Assisstant

Tutorial ini akan menjelaskan bagaimana menggunakan ARPAsing voicebank di UTAU secara manual.

Akan lebih baik jika Voicebank yang dipakai sudah di-OTO sepenuhnya, karena pas-tidaknya timing sangat bergantung pada nilai preutterance.

Kalau kamu tidak menggunakan plugin, Kamu bisa melewati masalah timing dan fonem yang salah. Tapi kamu akan kehilangan keuntungan dari konversi dasar.

Kalau komputermu bisa pakai ARPAsing Assistant tapi kamu lebih memilih untuk tidak memakainya, kamu bisa langsung buka file .exe untuk mencari konversi kata ke arpabet. Tapi kalau kamu benar-benar tidak bisa memakainya(misalnya pengguna Mac), Kamu bisa pakai [situs ini]() untuk konversi. Kamusnya mungkin tidak sekuat yang terpasang di plugin, tapi kalau sudah terbiasa, kamu bisa mencari sendiri kata yang hilang. Jika kamu tidak terbiasa dengan Arpabet, kamu bisa merujuk [artikel ini]() atau [grafik fonem]() saat mengedit.

Masukkan lirik bahasa Inggris ke dalam UST seperti biasa untuk referensi.

Ubah setiap not ke CV dari suku kata pertama, pisahkan tiap fonem dengan spasi. Contohnya "Cat" adalah "K AE T" dalam arpabet, jadi ubah lirik ke `[k ae]`. Begitu juga "Steps" yang konversinya "S T EH P S", ganti lirik dengan `[t eh]`.

Not penting yang kita butuhkan selanjutnya adalah not akhiran. Dimanapun ada rest kamu harus memberi not akhiran sebagai penutup. Praktisnya, jika panjang rest-nya kurang dari 1/4, ganti rest secara keseluruhan. Jika sisanya lebih panjang, 1/4 bagian restnya yang diubah. Untuk "Cat" not akhirannya adalah `[t -]`, dan untuk "Steps", not akhirannya adalah `[s -]`.

Sisanya  adalah memasukkan not transisi. List ini bekerja pada difon, jadi setiap lirik memiliki dua fonem.

Akhiran/Awalan dianggap satu fonem dan dimasukkan saat ada transisi antara lirik asli dan rest. Kita sudah membahas not dengan rest DIBELAKANGNYA, jadi mari kita bahas not dengan rest di depannya. Jika dimulai dengan huruf vokal, kamu bisa menambahkan tanda kurang. Misalnya, "Eye" `[ay]` menjadi `[- ay]`. Jika dimulai dengan cluster konsonan atau konsonan, kamu mungkin ingin mengerjakannya dari belakang mulai dari konsonan inti. Ambil contoh "Strand". Buat not `[s t]` tepat sebelum `[r ae]`, lalu not `[t r]` sebelum `[s t]`. Buat not `[- s] [s t]`. Ini untuk menciptakan transisi penuh dari akhiran, konsonan, ke inti suku kata.

Untuk transisi antar suku kata, gunakan prinsip transisi penuh yang sama antar difon.

"stranded on this island"

`[- s][s t][t r][r ae][ae n][n d][d eh][eh d][d aa][aa n][n dh][dh ih][ih s][s ay][ay l][l eh][eh n][n d][d -]`

Panjang not transisi bergantung pada preutterance not yang mengikutinya. Tapi kamu bebas memanjangkan/memendekkanya.

Panjang not transisi bergantung pada preutterance not yang mengikutinya. Tapi kamu bebas memanjangkan/memendekkanya.

Dari sini, kamu bisa mulai tuning seperti biasa.

---

# Voicebank Usage Tutorial without ARPAsing Assisstant
This tutorial will explain how to use an ARPAsing voicebank in UTAU, without ARPAsing Assistant.

It is in your best interest to have a fully OTO'd voicebank, before making USTs with it, because adjusting the timing of notes will depend on preutterance values.

If you aren't using the plugin, you can bypass all of the problems involved in adjusting the timing and incorrect phonemes. However, you miss out on all the convenience of having base conversions.  
If your computer is able to use ARPAsing Assistant but you choose not to use it, you can open the exe as a standalone program to look up word-to-arpabet conversions. However, if you're completely unable to use it (for example, Mac users) you can use [this website]() to find conversions. The dictionary may not be as robust as the one built into the plugin, but after familiarizing yourself with the phonetic system you should be able to transcribe any missing words yourself. If you're not familiar with Arpabet, you can reference [this article]() or the [phoneme chart]().

Enter the plain english lyrics into the UST as you normally would, for reference.  
Change each note to the main CV of the syllable, separating each phoneme with a space. For example, the word "cat" is "K AE T" in arpabet, so change the lyric to say `[k ae]`. Likewise, "steps" is "S T EH P S", so put `[t eh]`.  
The other essential notes we need are phrase-final notes. Wherever there is a rest after a note, you need to have phoneme to silence. As a rule of thumb, if the rest is less than 1 quarter note long, change the whole rest. If the rest is longer, then only the first quarter note needs to be changed. For "cat" that would be a `[t -]` note, and for "steps" it would be `[s -]`.

The rest of it is entering transitional notes. This list works on diphones, so every lyric note has two phonemes.  
Silence counts as one, and is necessary whenever transitioning between sung lyrics and rests. We already covered notes with rests AFTER them, so let's consider notes with rests before. If it starts with a vowel, you can simply add a hyphen. For example, "eye" `[ay]` becomes `[- ay]`. If it starts with a consonant or consonant cluster, you want to work backwards from the innermost consonant. Take "strand" for example. Make a note just before `[r ae]` that has `[t r]`. Make a note just before `[t r]` that has `[s t]`. Make a note just before `[s t]` that has `[- s]`. This gets you a full transition from silence, through the consonants, to the nucleus of the syllable.  
For transitions between syllables, use this same principle of full transitions from diphone to diphone.

"stranded on this island"
`[- s][s t][t r][r ae][ae n][n d][d eh][eh d][d aa][aa n][n dh][dh ih][ih s][s ay][ay l][l eh][eh n][n d][d -]`

The length of the transitional notes depends on the preutterance of the note that follows it. However, you can use your personal judgement to make them longer or shorter.  
If any particular note sounds strange or off, you can switch to using an alternate recording of the same diphone by adding a numerical suffix, like changing `[f ey]` to `[f ey1]` and so on.

From here, you can tune as normal.
