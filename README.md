# uyghur-topology
Topological approach to selecting a shape from the set of morphs of a Uyghur letter

# Shape Classes

## Short Introduction

There are 32 letters in Uyghur Arabic Alphabet that is used as the official written system. Among these 32 letters, there are 26 consonants and 8 vowels. 

> 32 Letters = 26 Consonants + 8 Vowels

Not sure what consonants and vowels are? Don't bother the definition for now. Here are some examples in English:

```
Consonants:  , b, c, d, , f, g, ...
Vowels    : a,  ,  ,  ,e,  ,  , ..., i, ..., o, ..., u, ...
```

In Uyghur language, however, here are the alphabet:

```
Consonants: ب، پ، ت، ج، چ، خ، د، ر، ز، ژ، س، ش، غ، ف، ق، ك، گ، ڭ، ل، م، ن، ھ، ۋ، ي
Vowels    : ئا، ئە، ئې، ئى، ئو، ئۇ، ئۆ، ئۈ
```

## Shapes

Each letter has several shapes, namely, 2, 4 or 8 shapes for each letter. For example: `ئا` (A) has 4 shapes, `ئې` (É) has 8 shapes; `د` (D) has 2 shapes and `ب` has 4 shapes. 

So how do you know decide which shape to use for a particular letter in a particular word? It is easy. *Use the one that makes sense!* Here is what I mean by that.


## Classification

Let's first consider the four shapes below. 

```
│, ┴, └, ┘
```

If you are given a set of four shapes as below, and the only rule is *always do *not* have open ends *horizontally* (well, that is how we write letter, right? Not vertical.) Then we could assemble them into something like this below:

Right: (notice that no open ends on left, right or middle)

```
└┘
└┴┘
└┘└┴┘
└┘│└┴┘
└┴┘││
```



Wrong: (notice the open ends on left, right or middle)

```
┘└
┴┴┘
└│┘
```

When teaching these, I would stand in front of the class, and use my arms to get the shapes above: extend my arms to be `┴`, only extend right arm to be `└`, and stand still with arms on both sides (as soldiers) to be `│`. Well, you get the point, and amused.


## Letters and Categories

We have base shapes `{│, ┴, └, ┘}`. Now let's do the classification. Here are the rules:

> All *consonants* have either 2:{│, ┘} or 4:{│, ┴, └, ┘} shapes;  
> All *vowels* have either 4:{│, ┘} or 8:{│, ┴, └, ┘} shapes;  (you are right, there are only 2 and 4 stuff in the set; look below);  
> Each shape of *vowels* (not consonants) have two forms: with &#1569; (e.g.  ┘&#1569; ) or without &#1569; (e.g.  ┘)  

We will come to `&#1569;` later. Let's first contentrate of the first two rules above.


### Consonants Classification

All consonants of shape class `2:{│, └}` are: `د، ر، ز، ژ، ۋ، ھ`. 

All other consonants are of shape class `4:{│, ┴, └, ┘}`. 

Here is the Uyghur Arabic Script Alphabet along with the Latin Script:

[here][ULY]


### Vowel Classification

All vowels of shape class `4:{│, ┴, └, ┘}` are: `ئې، ئى`.  (é, i)

All other vowels are of shape class `2:{│, └}`. 



### Topology

Letter are connected in a way that reduces open ends. An easier way of saying this is: 

>> Always hold hands whenever possible. (Be friendly!)

### Consonants and vowels

Most words native to Uyghur language keeps the consonants and vowels in it balanced. A counter example would be a word like `strict` where we only have one vowel `i` in the word, while 5 consonants `strct` are in the word. In Uyghur language, we mostly have words such as `dada` (father), `ana` (mom), `bala` (child) etc. 

Here is also a simple rule for the structure of the words. But first, we need to talk about `Syllable`.


### Syllables

I will keep it simple and this is not a formal definition. 

A syllable is a smallest possible meaningful *phonetic* component of a word. For example, `mo·ther` has two syllables: `mo` and `ther`. More examples are: `hap·py`, `fa·ther`. In Uyghur language, it is the same. Using the words we used above: `da·da`, `a·na`, `ba·la`. 

Now the rules. We use `A` for represent vowels, and `B` to represent consonants.

> The syllables in *most* words *native* to Uyghur language are: syllables={`A`, `AB`, `BA`, `BAB`} (notice the absence of structures such as `BB`, `BBA`, `ABB` etc.)  
> When a **syllable** *begins* with a **vowel**, then the vowel adds a **&#1569;** to its shape.

In short, if a syllable is of form `A` or `AB`, then the `A` has &#1569;.

## Examples

### `dada` => `││││`

Let's first give examples to the first rule above. Consider the words `da·da`. We can see that this word has two syllabes: `da` and `da`. `d` is a consonant, therefore `B`, and `a` is a vowel, therefore `A`. Thus this word has two syllables of shape `BA` among the four shapes above. Since both `BA` does *NOT* begin with a vowel (it begins with `d`), therefore we can forget about &#1569;. We can *write* the word even *without* knowing the letters themselves! Let's try. `d` is a consonant shape set in `2:{│, └}`, `a` is *not* in the vowels shape set `4:{│, ┴, └, ┘}` (we only have two for these but `a` is not any of the two!). Note that, Uyghur Arabic script is written **from right to left**. Lets' write it:

1. Choose a shape from `2:{│, └}` for the first letter `d`. Since we are writing from right to left, and *cannot* have open ends horizontally, we *cannot* choose `└` from the two `2:{│, └}`. Let's choose `│`.
2. Choose a shape from `2:{│, └}` for the first letter `a`. The first letter on its right does not *offer a hand* to it, so it cannot *hold hands* using shape `└`. Choose `│` again.
4. Consider the next `d`. Same logic, and we choose `│` for the previous (second) letter `a` does not *offer a hand*. 
5. Consider the last letter `a`. Follow the same logic. And we choose `│` for the previous (third) letter `d` also *does not offer a hand*. 
6. It seems they are not so friendly!
7. We have our word `dada` at last: `││││`. (four standing side by side, without holding hands).

### `bala` => `└┘└┘`

Now consider `ba·la`. `ba` is of syllables structure `BA`, `la` is of syllables structure `BA` as well. So no &#1569;. `b` is from `4:{│, ┴, └, ┘}`, and `a` is form `2:{│, └}`.

1. `b` is the first letter of shape `4:{│, ┴, └, ┘}`. Since `b` is the *first* letter on the right, we can choose either from `│, ┘`. Let's move on.
2. `a` is the letter next to `b` of shape `2:{│, └}`. *Let's be friendly!* We choose `└` for `a` so that it offers a hand to the previous `b`.
3. `b` can now *hold hands* with `a` using shape `┘`.
4. This leaves us with shape `└┘` for the first two letter `ba`.
5. We can find that `la` are also in the same situnation: `l` is also of the shape `4:{│, ┴, └, ┘}` as `b` was! So `la` can *also be friends*: `la` => `└┘`
6. In the end, we have `bala` => `└┘└┘`.
 
### Some more!

Let's consider some more words. `bulut` (cloud), `su` (water), `kala` (cow), `siz` (you), `asman` (sky).

`bulut` (cloud):  (work this out yourself before looking at the answer below!)

The letter and their shape classes are:

- `b` <- `4:{│, ┴, └, ┘}`
- `u` <- `2:{│, └}`
- `l` <- `4:{│, ┴, └, ┘}`
- `u` <- `2:{│, └}`
- `t` <- `4:{│, ┴, └, ┘}`

Let's put them together and make sure they get along well (become friends). Here is the selection. Note that the syllables are of form `BA·BAB`, so no syllable that begins with a vowel. We can forget about &#1569;. 

- `b` <- `┘`
- `u` <- `└`
- `l` <- `┘`
- `u` <- `└`
- `t` <- `└`

We get: `│└┘└┘`


----

`su` (water):  (work this out yourself before looking at the answer below!)

The letter and their shape classes are:

- `s` <- `4:{│, ┴, └, ┘}`
- `s` <- `2:{│, └}`
 
This is simple. It is one syllable and of form `BA`. Does not begin with a vowel. So we get `└┘`.

----

`kala` (cow):  (work this out yourself before looking at the answer below!)

Look up the rule table for the letter and their shape classes. Which class does `k`, `a`, `l` belong? (We can choose from classes `4:{│, ┴, └, ┘}`, `2:{│, └}`).

`kala` has a syllabus form of `BA·BA`. We can safely forget &#1569;. We get: `└┘└┘`.

-----

`siz` (you):  (work this out yourself before looking at the answer below!)

Look up the rule table for the letter and their shape classes. Which class does `s`, `i`, `z` belong? (We can choose from classes `4:{│, ┴, └, ┘}`, `2:{│, └}`).

We find that they all belong to `4:{│, ┴, └, ┘}`. Imagine three friends who are willing to do anyting for each other. You are going to take a picture of them, so they stand in a line, *holding hands*. So the most happy case for them is: `└┴┘`. 

And syllabus form is `BAB` threfore no &#1569;.

-----

`asman` (sky): (work this out yourself before looking at the answer below!)

The letter and their shape classes are:

- `a` <- `2:{│, └}`
- `s` <- `4:{│, ┴, └, ┘}`
- `m` <- `4:{│, ┴, └, ┘}`
- `a` <- `2:{│, └}`
- `n` <- `4:{│, ┴, └, ┘}`

In order to a) *connect* those letters and b) be friendly, we have to choose the following set:

- `a` <- `│`
- `s` <- `┘`
- `m` <- `┴`
- `a` <- `└`
- `n` <- `│`


We get: `│└┴┘│`.

Notice that the syllables of `as·man` as has a form of `AB·BAB`. The first syllable `AB` begins with a vowel `a` (as `A` in our representation). Therefore we add &#1569;. In the end, we get:

We get: `│└┴┘│`&#1569;.


-----

Isn't it amazing that there is only one possible way to connect them!? Well, that is the by the laws of topology. But we can forget about them. A simple rules is: if people choose how friendly they are going to be to their neighbors (friendly to the left `┘`, to the right `└`, or better, to both neighbors `┴`, or worse, to none of the neibours `│`, then *you can always satisfy them in a neighborhood (not in a building, but a contryside where you have houses side by side!)




## Last Word

This set of rules are a result of my continuing effort in trying to teach our language and its script to students, freinds who speak Uyghur but trying to learn how to write, and also to friends who do *not* speak the language itself, but tryint to learn. This topology based approach is very universal so that students can learn how to write **before** they are familiar with the full alphabet and all the different shapes of each and every letters. You can even play with this set of rules in your own language!

I hope this routine could be taught in schools where kids can **play** in their classes taking roles as the four base shapes. This way of learning is much fun, and can give very clear idea fo the script for the students from the beginnin.

These are my original ideas. Please cite this website http://hyiltiz.com/uyghur-topology if you used this work either commertially or non-commercially. 

[ULY]: https://upload.wikimedia.org/wikipedia/commons/0/0c/UEY_ULY_Elipbesi_Kichik.jpg  "Uyghur UEY ULY"
