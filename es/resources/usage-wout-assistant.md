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
