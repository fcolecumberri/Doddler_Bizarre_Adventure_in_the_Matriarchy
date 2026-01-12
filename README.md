# Daiakuji Translation Project 🇯🇵 → (🇬🇧🇺🇸) & (🇪🇸🇲🇽)

**THIS PROJECT IS NOT FINISHED YET. This is still a work in progress. BUT THE GAME IS PLAYABLE**

## About

This is the translation project for the Alicesoft's Daiakuji game.

This repository provides both translation projects, Dozu Lad' translation and ours (me and the wonderfull people in the `thanks` section).

Dozu Lad' translation is MTL free but still has Japanese text.

In the other hand our translation has been done using multiple machine translation (MTL) systems into Spanish and English. Followed by manually fixing the MTL errors that may appear. There has been a lot of MTL errors already fixed and I know there are still a lot to fix.

Both projects started independently, but now Dozu Lad and I have finally met and decided to join efforts to try to fullfill each others needs.
We hope that my programming experience will fix some known issues that appeared in Dozu Lad project while Dozu Lad's knowledge of the language provides a great oportunity to get rid of MTL.

As always this being a GitHub project, people are welcome to help (Speciall thanks to [GCNess](https://github.com/GCNess) for helping with the project).

## How to play

https://github.com/user-attachments/assets/fbb05d1b-4140-47f9-b4e7-d3e56dfcadf7

Since the text generated here is made with UTF-8, to play this game, you need kichikou's implementation of system3 virtual machine: [xsystem35-sdl2](https://github.com/kichikuou/xsystem35-sdl2)(Tested) or [system35-sdl2](https://github.com/kichikuou/system3-sdl2)(Not tested).

In order to play the game you should acquire a legal copy of the game,
downloads the `.tar.gz` files from [the Releases](https://github.com/fcolecumberri/Doddler_Bizarre_Adventure_in_the_Matriarchy/releases),
extract them and
copy from the game directory the files
`大悪司WA.ALD`,
`大悪司DA.ALD`,
`大悪司BA.ald`,
`大悪司BA.bgi`, and
`大悪司SB.ALD`
(maybe you need some more)
in the same place where you extract the `.tar.gz` files.

If you acquire the game as a Game Disk, you might need to use the upgrade using [AliceSoft support page](https://www.alicesoft.com/support/new_akuji.html) (I have not tested this).

If you don't have a legal copy I suggest you to get it from [DLsite](https://www.dlsite.com/pro/work/=/product_id/VJ003877.html).

## How to contribute

**If you want to contribute, WELCOME!!**

First of all, if you don't know how to use GitHub, check out tutorials, there are plenty.
If you have any doubt, feel free to ask me after checking the tutorials.

### How the files are structured.

The text is structured as a follow:

Each file is a [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) using colon `,` as delimiter and double-quote as quotation `"`.

The 1st field indicate who is talking, assuming my python script could figure it out, otherwise `??`. If the first field is `__system__`, it indicates that rows are not text, but a piece of code.

The 2nd field is the Japanese text, the 3rd is English, the 4th is Spanish.

Text gets automatically wrapped on the recompilation process so there is no need to worry about text length (However if the text is too long it might exceed the 3 lines of the text block, it's not a big issue, since those get automatically wrap into a new text block, but it would be better not to).
in each cell, line breaks are treated as block breaks. For example in `プロローグ.csv` at the begging Akuji says:

```
I had no idea that the war zone I went to with the intention of showing Minka a good time was such an ordeal…
……………
Well… well… it looks like Osaka had a rough time too…
```

That get's rendered as:

```
I had no idea that the war zone I
went to with the intention of
showing Minka a good time was such an ordeal…
```

```
……………


```

```
Well… well… it looks like Osaka had
a rough time too…

```

Every code row had been removed in the process of opening this project here on GitHub so this cannot be used for piracy.
The only exceptions are `{`, `}` which indicates `if` statements, and `~R` which forces line-breaks.
Since those are very needed to format text and understanding conversation.

### What else is needed to be done.

If you wan't to help, start by checking the issues on this project, I'll try to have them updated with the stuff that is missing.

## Thanks

First and foremost, thanks [Alicesoft](https://www.alicesoft.com/) and [Hanny King](https://x.com/hanny_king) for creating this awesome master piece.

[Dozu Lad](https://x.com/Bfarchs) For being as crazy as me thinking this was going to be an easier task and also helping me with this collaboration.

I want to thank AruNaru, [your video](https://www.youtube.com/watch?v=RV37EIVDhpc) was the first domino that made this possible.

[Cecelia](https://www.youtube.com/@CeceliaIsAWeeb) for all the support you have given to me. Each time I have needed help with this project, you knew exactly who I needed to talk to, without you this project would be farther away.

I want to thank
[Kichikou](https://github.com/kichikuou) and [Nunuhara](https://github.com/nunuhara)
for their tools, effort and help provided to me.

Thanks SeizedVirus53 and Michi for all the help translating the images.

Garland, Thanks for editing the images, they look awesome.

[VivversX](https://www.youtube.com/@VivversX) thanks for the cheering, that kind of small things truly motivates me.

## CopyRight

The story, character, music, images (except the fonts on the translated images) and everything I miss to mention is property of Alicesoft.
Everything released here is only to be used as a patch on the legally acquired Alicesoft's software.

The fonts used on the translated images on this non-profit project on the translated images are `Anime Ace` freely usable on non-profit projects.

The provided font file named `FinalFont.ttf` is a meld of [Relaxed Typing Mono Jp](https://github.com/mshioda/relaxed-typing-mono-jp) filling the missing characters with [IBM's plex](https://github.com/IBM/plex). All of them distributed under the `SIL OPEN FONT LICENSE Version 1.1`.

## F.A.Q.

### Why Spanish?

It is my native language.

### Why English?

Spanish is popular, but English is the universal language and I want more people to be able to play this awesome game.

### Why MTL?

At my peak, my Japanese was JPLT N5 (Years ago, and I haven't studied that much since).
Also my English is halfway between B2 and C1. If I translate this, it will surely be worst than MTL.

### There is an error on this piece of text...

If you want to fix it, create a Pull Request, I will gladly merge it and it will be fine on the next release.

If you don't want (or know how to) could you please open an Issue? I'll try to attend it as soon as possible.

### What's going to happen now that there are 2 projects seemingly doing the same?

The idea is to merge both projects into a single final version.

The MTL version will keep since is it is the only one with a Spanish version and
it also provides a version that is fully translated
(people that have no idea of japanese might prefere an English with errors here and there over English with unreadable pieces here and there).

The idea in that front now is to use Dozu Lad's version to clean up MTL garbage both in English and Spanish which will be easier and faster.
Hopefully this will converge in a single translation.
