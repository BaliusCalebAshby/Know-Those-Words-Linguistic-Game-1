One syllable words ? How about those same words in a foreign language?
This game helps you do the paradigms

Here's a sample:

KTW games

1 - Identify all related words from list
2 - identify all non-one-syllable words
3 - identify all words you personally don't know
4 - enter synonym /antonym/ homonym/ nearest-sounds-like relationships
5 - make a sentence with the most words
6 - count the Xs in the list
7 - translate into foreign language
8 - get the most scrabble points
9 - multi-tiered menus w/paradigms

ktwdbod=# select * from
(
select DISTINCT(LOWER(UNNEST(string_to_array(word,' ')))) as raw_word
 from stg.wordbase
) t1
LEFT JOIN (select word from wordbase) t2 ON t1.raw_word = t2.word
WHERE LENGTH(raw_word) > 0
AND t2.word IS NULL
ORDER BY 1
;

 raw_word | word 
----------+------
 bark     | 
 best     | 
 clade    | 
 cloy     | 
 crane    | 
 create   | 
 crepe    | 
 dint     | 
 dude     | 
 fluff    | 
 geek     | 
 group    | 
 heap     | 
 hunch    | 
 husk     | 
 just     | 
 knack    | 
 logged   | 
 lunge    | 
 mask     | 
 mine     | 
 niche    | 
 pitch    | 
 quirk    | 
 rift     | 
 rind     | 
 romp     | 
 sap      | 
 scant    | 
 shrewd   | 
 snob     | 
 stiff    | 
 swath    | 
 thy      | 
 tilt     | 
 vague    | 
 warp     | 
 world    | 
(38 rows)

ktwdbod=# 

As native adult speakers of English, you would think we would know all these words, right ?
How many people know clade or dint?
:-)
B
