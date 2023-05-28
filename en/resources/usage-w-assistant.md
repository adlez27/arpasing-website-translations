## Voicebank Usage Tutorial with ARPAsing Assistant

This tutorial will explain how to use an ARPAsing voicebank in UTAU, using ARPAsing Assistant.  
It is in your best interest to have a fully OTO'd voicebank, before making USTs with it, because adjusting the timing of notes will depend on preutterance values.

If you don't yet have the ARPAsing Assistant plugin, you can download it from [here]().  Unzip the toolkit, and move the "arpasing-assistant" folder to the "plugins" folder where UTAU is installed.  
Put plain english words into the UST, select the notes, and run the ARPAsing Assistant plugin to convert them. Alternatively, you can enter plain arpabet phonemes into the note, separated by spaces. If you put `/u` at the end of a word, the note will be divided evenly for each diphone, instead of each diphone being different lengths.
The notes you select for conversion MUST have another note after them. The best way to ensure this is by putting a rest at the end of the UST.

To do multi-syllable words via **word input**, you will have to delete all notes but the first syllable, and extend the first note to cover the length of all the notes combined. Put the entire word in the note, and convert as normal. From there you will have to put the notes back at the correct pitch and fix the timing.
However, doing multi-syllable words via **phoneme input** is a lot simpler, as you can simply break the phonemes across multiple existing notes before conversion.

**FOR MULTIPITCH AND EXTRA SAMPLES:** If the voicebank is properly configured, it should work without issue, but there are common situations that cause incompatibility with ARPAsing Assistant. The main voicebank folder must contain one pitch without suffixes, and all other pitches must be in subfolders. Any non-standard extra samples must also be in subfolders. ARPAsing Assistant only reads the oto.ini file in the top level of the voicebank, and that file must only contain standard ARPAsing OTO entries.

When converting words to diphone notes, ARPAsing Assistant will select the best copy of a particular diphone based on context. For example, if you input the word "stand", it will choose a `[t ae]` note from a "stae" sample rather than from a "tae" sample. The context of word-like recordings creates natural pronunciation. This is the purpose of numeric suffixes, to distinguish one from another. Don't delete the numbers.

While it is recommended to use a completely untuned UST, you can adjust the volume level of notes and flags prior to conversion, and they will be retained. Pitchbends and vibrato get messed up and aligned to the wrong notes, so it's recommended to remove them entirely first.

Listen to the UST as it is right now to get an idea of how it sounds, and what sections you need to fix. Chances are that some notes will be off time, and there will be pronunciations that you are unhappy with.
Find the words or syllables where the pronunciation isn't what you want it to be. If you're not familiar with Arpabet, you can reference [this article]() or the [phoneme chart]() when editing.

Let's fix the timing. The most glaring problem is with multi-syllable words. Because they had to be combined into a single note prior to conversion, the timing is no longer the same as intended. Hold down ctrl and drag the ends of the notes to change the lengths without pushing the notes around. Align them so that the core CVs of each syllable start at the intended position. Fix the pitches while you're at it, by selecting all the notes of one syllable and moving it up/down.  
Look for phrases that start with consonants. (They would be the first syllable after what used to be a rest.) The `[- C]` note is often very short, so hold ctrl and drag the left side to make it longer that way. Adjust the length so that it starts where the envelope of the next note starts.

From there you can go through note by note fixing the timing of all the small notes, by changing them to the length of the preutterance envelope of the next note. This is why you want your bank to already be fully OTO'd. You probably want to set your Quantize to 64th notes.  
As you go along you may also be modifying pronunciation. For example, "don't want" will become `[d ow][ow n][n t][t w][w aa]` etc. but this is far too many notes for a short space, where in practicality this phrase often sounds like "don want" when singing. So, remove the `[n t]` and change the `[t w]` to `[n w]`.

From here, you can tune as normal.
