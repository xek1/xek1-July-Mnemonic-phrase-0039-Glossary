# xek1-July-Mnemonic-phrase-0039-Glossary

# Wordlists

* [英语English](bip-0039/english.txt)
* [日语Japanese](bip-0039/japanese.txt)
* [韩语Korean](bip-0039/korean.txt)
* [西班牙语Spanish](bip-0039/spanish.txt)
* [中文Chinese 简体(Simplified)](bip-0039/chinese_simplified.txt)
* [中文Chinese 繁体(Traditional)](bip-0039/chinese_traditional.txt)
* [法语French](bip-0039/french.txt)
* [意大利语Italian](bip-0039/italian.txt)
* [捷克语Czech](bip-0039/czech.txt)
* [葡萄牙语Portuguese](bip-0039/portuguese.txt)
* [词汇表排序组成Vocabulary sorting composition](bip-0039/%E8%AF%8D%E6%B1%87%E8%A1%A8%E6%8E%92%E5%BA%8F.xlsx)





以上是十种语言随便生成一种助记词在钱包上试着其他地方只要是39词汇的都是通用的

比如你英文里面助记词生成

【英文】leisure ridge poet banner donor ginger ivory retire clinic mystery pulse derive

【中文简体】幅 隐 蓝 又 望 挥 耐 珍 才 摇 牙 京

【中文繁体】幅 隱 藍 又 望 揮 耐 珍 才 搖 牙 京

【日语】そっかん　ねまわし　とくしゅう　うえき　けおとす　しうち　せつめい　ねさげ　かたち　ちあん　なにわ　くさき

助记词分种拿到认意一种都可以计算出来其他的语言助记词只需要在词汇表里面找到对应排序即可根据自己爱好选择自己的助记词

【1022】leisure幅
【1485】ridge 隐
【1388】poet 蓝
【147】banner 又
【523】donor 望
【785】ginger 挥
【952】ivory 耐
【1472】retire 珍
【346】clinic 才
【1172】mystery 摇
【1389】pulse 牙
【476】derive 京
助记词是12个单词，英文的中文的只需在中文的词汇表找到对应排序的即可


## Wordlists (Special Considerations)

### Japanese

1. **Developers implementing phrase generation or checksum verification must separate words using ideographic spaces / accommodate users inputting ideographic spaces.**
(UTF-8 bytes: **0xE38080**; C/C+/Java: **"\u3000"**; Python: **u"\u3000"**)
However, code that only accepts Japanese phrases but does not generate or verify them should be fine as is.
This is because when generating the seed, normalization as per the spec will
automatically change the ideographic spaces into normal ASCII spaces, so as long as your code never shows the user an ASCII space
separated phrase or tries to split the phrase input by the user, dealing with ASCII or Ideographic space is the same.

2. Word-wrapping doesn't work well, so making sure that words only word-wrap at one of the
ideographic spaces may be a necessary step. As a long word split in two could be mistaken easily
for two smaller words (This would be a problem with any of the 3 character sets in Japanese)

### Spanish

1. Words can be uniquely determined by typing the first 4 characters (sometimes less).

2. Special Spanish characters like 'ñ', 'ü', 'á', etc... are considered equal to 'n', 'u', 'a', etc... in terms of identifying a word. Therefore, there is no need to use a Spanish keyboard to introduce the passphrase, an application with the Spanish wordlist will be able to identify the words after the first 4 chars have been typed even if the chars with accents have been replaced with the equivalent without accents.

3. There are no words in common between the Spanish wordlist and any other language wordlist, therefore it is possible to detect the language with just one word.

### Chinese

1. Chinese text typically does not use any spaces as word separators. For the sake of
uniformity, we propose to use normal ASCII spaces (0x20) to separate words as per standard.

### French

Credits: @Kirvx @NicolasDorier @ecdsa @EricLarch
([The pull request](https://github.com/bitcoin/bips/issues/152))

1.  High priority on simple and common French words.
2.  Only words with 5-8 letters.
3.  A word is fully recognizable by typing the first 4 letters (special French characters "é-è" are considered equal to "e", for example "museau" and "musée" can not be together).
4.  Only infinitive verbs, adjectives and nouns.
5.  No pronouns, no adverbs, no prepositions, no conjunctions, no interjections (unless a noun/adjective is also popular than its interjection like "mince;chouette").
6.  No numeral adjectives.
7.  No words in the plural (except invariable words like "univers", or same spelling than singular like "heureux").
8.  No female adjectives (except words with same spelling for male and female adjectives like "magique").
9.  No words with several senses AND different spelling in speaking like "verre-vert", unless a word has a meaning much more popular than another like "perle" and "pairle".
10. No very similar words with only 1 letter of difference.
11. No essentially reflexive verbs (unless a verb is also a noun like "souvenir").
12. No words with "ô;â;ç;ê;œ;æ;î;ï;û;ù;à;ë;ÿ".
13. No words ending by "é;ée;è;et;ai;ait".
14. No demonyms.
15. No words in conflict with the spelling corrections of 1990 (http://goo.gl/Y8DU4z).
16. No embarrassing words (in a very, very large scope) or belonging to a particular religion.
17. No identical words with the Spanish wordlist (as Y75QMO wants).

### Italian

Credits: @paoloaga @Polve

Words chosen using the following rules:

1. Simple and common Italian words.
2. Length between 4 and 8 characters.
3. First 4 letters must be unique between all words.
4. No accents or special characters.
5. No complex verb forms.
6. No plural words.
7. No words that remind negative/sad/bad things.
8. If both female/male words are available, choose male version.
9. No words with double vowels (like: lineetta).
10. No words already used in other language mnemonic sets.
11. If 3 of the first 4 letters are already used in the same sequence in another mnemonic word, there must be at least other 3 different letters.
12. If 3 of the first 4 letters are already used in the same sequence in another mnemonic word, there must not be the same sequence of 3 or more letters.

Rules 11 and 12 prevent the selection words that are not different enough. This makes each word more recognizable among others and less error prone. For example: the wordlist contains "atono", then "atomo" is rejected, but "atomico" is good.

All the words have been manually selected and automatically checked against the rules.

### Czech

Credits: @zizelevak (Jan Lansky zizelevak@gmail.com)

Words chosen using the following rules:

1.  Words are 4-8 letters long.
2.  Words can be uniquely determined by typing the first 4 letters.
3.  Only words containing all letters without diacritical marks. (It was the hardest task, because one third of all Czech letters has diacritical marks.)
4.  Only nouns, verbs and adverbs, no other word types. All words are in basic form.
5.  No personal names or geographical names.
6.  No very similar words with 1 letter of difference.
7.  Words are sorted according to English alphabet (Czech sorting has difference in "ch").
8.  No words already used in other language mnemonic sets (english, italian, french, spanish). Letters with diacritical marks from these sets are counted as analogous letters without diacritical marks.

### Portuguese

Credits: @alegotardo @bitmover-studio @brenorb @kuthullu @ninjastic @sabotag3x @Trimegistus

1. Words can be uniquely determined by typing the first 4 characters.
2. No accents or special characters.
3. No complex verb forms.
4. No plural words, unless there's no singular form.
5. No words with double spelling.
6. No words with the exact sound as another word with different spelling.
7. No offensive words.
8. No words already used in other language mnemonic sets.
9. The words which have not the same spelling in Brazil and in Portugal are excluded.
10. No words that remind one of negative/sad/bad things.
11. No very similar words with only 1 letter of difference.
