# ARPAsing Reclist Writing Tutorial

ARPAsing is not a single, static reclist, but a method of English UTAU. It's similar to how VCV isn't a single reclist, but a method of Japanese UTAU. The only criteria for a reclist being an arpasing reclist is compatibility with Moresampler's auto-OTOer, and with the ARPAsing Assistant plugin.

You can write your English reclist or reclist addon in any way you like, as long as the phonemes you include directly correspond to Arpabet. Once it's written, you'll need to make an index.csv file in order for Moresampler to know how to OTO it.  
If you're writing a reclist addon, you can simply add to the existing index.csv for that reclist. If you're making a list from scratch, you'll have to make a new index file. You can use any text editor to create one, but you could also use any csv editor you like.

The first column contains all the file names, which is generally exactly the same as the reclist file you would use in OREMO. You need to include the file extension. If using a text editor, separate this column from the next column with a comma. The second column has the arpabet version of the phonemes for that line. Each phoneme must be separated by an underscore.  
Alternatively, you can write your reclist directly in Arpabet to begin with, and separate each phoneme with an underscore. This removes the need to write an index.csv at all.

All arpabet phonemes are accepted by Moresampler's auto OTOer, except these:  
`[em] [en] [eng] [el] [nx] [dx]`

If you've made a reclist addon, you must regenerate the OTO for the whole bank, so that duplicates can be properly numbered.

In order to make recording easier, you can also make an OREMO comment file. This file is named "OREMO-comment.txt" and goes in the destination folder of the voicebank. The first column contains all the file names, corresponding to the reclist. File extension is not necessary, it just needs to match up to the reclist file. Separate the columns with a tab. The next column has the comment, which is where you can write notes, like how the sample is meant to be pronounced.
