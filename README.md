
# Markedup_1928_Psalter

A copy of the Psalter (Psalms) from the 1928 Book of Common Prayer [1928_BCP]
with markup to allow optional formatting.

## Goals

* The be able to generate an exact letter-for-letter copy of the _text_ of the Psalms from the 1928_BCP.
  * True to reliable sources for the 1928_BCP
    * http://justus.anglican.org/resources/bcp/1928/Psalms_1928.pdf
    * http://justus.anglican.org/resources/bcp/1928Standard/psalms.pdf (The STANDARD BOOK)
* All additions but be easily ignorable by software

## Why be true to "reliable sources" for the 1928_BCP

For reusaseability.

There are several on-line copies of the 1928

## What do you mean by "Markedup"

## Why the 1928_BCP?

### Asthetic translation with a history

### It is authorized for certain us fr major denomination, including:

#### Episcipal Church of America

The 1928_BCP was the official service and prayer book of the Episcipal Church from 1928 to 1979.
After 1979, it retained it's authorized status:

According to "https://www.episcopalcommonprayer.org/faq.html":

> The 1928 Book of Common Prayer is partially authorized by Resolution 1979-A121 and Resolution 2000-B042.

#### Eastern Orthodox

#### Roman Catholic


# Markup syntax

## Markup showing deatures of the source text

* `<SC>__</SC>` -- Use small caps
* `<BR>`  -- put a blank line after this verse

## Markup showing features of the Saint Dunstan's Psalter

* `<DA>__</DA>`
  * Replace text with an apostrophe.
  * ie `ev<DA>e</DA>` becomes "ev'ry"
* `<DS _2_>_1_</DS>`
  * Substiture _1_ with _2_
* `{d.}`
  * insert a dot character
* `{d-}`
  * insert a dash
* `{df}`
  * insert a flax (breath) marker
  * (shown a dagger character in the Dunstan Psalter)
* `{dx}`
  * Remove the following character
  * Usualy for comas that would confuse plain chant singing
* `{dv}`
* `{d_}`

### Temp

* `+` > `{d.}`
* `[,]` > `{dx},`
* `^` > `{dv}`
* `` > `{d_}`
* `{df}` > `{df}`
* `{d-}` > `{d-}`
* `` > `{}`
* `` > `{}`
* `` > `{}`
* `` > `{}`

## Markup showing history notes

> These show notes found in:
>   * http://justus.anglican.org/resources/bcp/1928/Psalms1.htm
>   * http://justus.anglican.org/resources/bcp/1928/Psalms2.htm
>   * http://justus.anglican.org/resources/bcp/1928/Psalms3.htm
>   * http://justus.anglican.org/resources/bcp/1789/Psalter1789&1892.htm

* `{HN tag}`
  * "tag" refers to an entry under the `verse_history_refs:` section of the YAML

> The `verse_history_refs:` enteries are formatted as follows:
>   * multiple enteries as seperated by ampersands (`&`)
>   * each entry has two parts seperated by a pipe (`|`)
>     * part 1, the referenced text
>     * part 2, notes (greyed out in the source material)

## Markup showing the names that some wish to avoid

> Some with to avoid writing or acidently saying the name or God
>
>  This is even recomended for Catholics.  From http://www.covert.org/Psalter/ :
>>  In accordance with the decree of Pope Benedict dated 29 June 2008, the psalm
>> verses containing the Tetragrammaton (Jehovah) or Digrammaton (Jah) are to be
>> modified when used liturgically by dropping the unspeakable Name (33:12) or
>> by changing it to "the Lord" (68:4, and 83:18).
>
> More details:
>  * https://www.usccb.org/resources/name-god
>  * https://brisbanecatholic.org.au/wp-content/uploads/vatican-directive-on-yhwh.pdf
>  * https://www.bible-researcher.com/dominus.html

* `<TETRAGRAMMATON CATH2008="" DUNSTAN="JEHOVAH"><SC>JEHOVAH</SC></TETRAGRAMMATON>`
  * at 33:12 
* `<TETRAGRAMMATON CATH2008="The Lord" DUNSTAN="JEHOVAH"><SC>JEHOVAH</SC></TETRAGRAMMATON>`
  * at 83:18
* `<DIGRAMMATON CATH2008="The Lord" DUNSTAN="JAH"><SC>JAH</SC></DIGRAMMATON>`
  * at 68:4

> Another option is to use the Hebrew to avoid it being accidently read.
> The printed and e-book "The Psalter of King David: The 1662 Coverdale Psalter
> Arranged for Orthodox Worship"
>> The holy name of God in Psalm 68 is transliterated in the 1662 psalter as
>> JAH, but is here rendered as the Hebrew tetragrammaton יהוה in order to
>> indicate that the sacred name should not be pronounced.
>
> As the editor explains in: https://catholicbibletalk.com/2021/01/the-psalter-of-king-david-part-2-guest-post-by-m-b/ :
>> I made exactly one—and only one—textual change to the 1662 psalter:
>> I restored the Tetragrammaton to Psalm 68, where it was (in my opinion) quite
>> poorly transliterated as “JAH”. I did this because (again, in my opinion)
>> it’s the singular instance where the Coverdale translation fails to read
>> well. JAH is really an ugly, jarring word in English; I’m not sure why
>> Jehovah wasn’t used here instead.



Info:
  * http://justus.anglican.org/resources/bcp/1928/Psalms.htm
  * http://www.ststeve.com/2011/07/31/whys-and-wherefores-of-coverdales-psalms/

Parsable HTML:
  * http://www.covert.org/Psalter/Bk1.html
  * http://www.covert.org/Psalter/Bk2.html
  * http://www.covert.org/Psalter/Bk3.html
  * http://www.covert.org/Psalter/Bk4.html
  * http://www.covert.org/Psalter/Bk5.html


ideas for formatting:
  * https://web.archive.org/web/20180817092926/http://www.stutler.cc/russ/dream_psalter.html

Sources:
  * http://www.covert.org/Psalter/  (Our Primary e-text source)
  * http://justus.anglican.org/resources/bcp/1928/BCP_1928.htm 
      * http://justus.anglican.org/resources/bcp/1928/Psalms_1928.pdf
      * http://justus.anglican.org/resources/bcp/1928/Psalms.htm (Includes history of changes)
      * http://justus.anglican.org/resources/bcp/1928Standard/psalms.pdf (The STANDARD BOOK)
  * https://www.episcopalnet.org/1928bcp/Psalter/Day1.html
  * https://commonprayeronline.com/psalter
  * https://archive.org/details/isbn_9781537520742/page/344/mode/2up (SCAN of 1928 BCP)

Which Psalms to read when:
  * https://www.stpetersaoc.org/Info/1928Lectionary.pdf


Reviews of multiple Psalters:
  * https://russellstutler.com/russ/psalter_reviews.html


== Use by Catholics:

  * https://forum.musicasacra.com/forum/discussion/13037/coverdale-psalms-in-novus-ordo/p1
  * https://www.reddit.com/r/divineoffice/comments/19dq99g/what_are_the_different_approved_liturgical/

  * But:
    * https://www.usccb.org/resources/name-god
    * https://brisbanecatholic.org.au/wp-content/uploads/vatican-directive-on-yhwh.pdf
    * https://www.bible-researcher.com/dominus.html

== https://catholicbibletalk.com/2021/01/the-psalter-of-king-david-part-1-guest-post-by-m-b/


> Since this is Catholic Bible Talk, I’m sure most readers have two questions in mind: What’s the Coverdale psalter? Is this psalter approved for use by Catholics?
>
> To answer the first question, the Coverdale psalter is the official, standard psalter used by the Church of England and most (if not all) of its daughter Anglican churches. (I’m sure it’s seeing much less use nowadays, as there seems to be a vendetta against archaic pronouns.) Myles Coverdale completed one of the earliest English Bible translations in 1535, and his translation of the Psalms in particular became popular enough to be adopted by the Church of England for use in its services. Somehow the Coverdale version managed to remain part of the Book of Common Prayer even after the publication of the Authorized Version (KJV), which has its own magnificent psalter. In my mind—and I know nearly everyone will have their own opinion here—the Coverdale psalter is far and away the greatest English psalter; and it’s one of the greatest influences on the modern English language (alongside the remainder of the BCP, the KJV, and of course the works of Shakespeare).
>
> That all sounds great, but if it isn’t approved for Catholics, then who cares, right? Fear not: for, behold, I bring you good tidings of great joy, which shall be to all people: The Coverdale psalter is now an official, approved Catholic psalter! In September 2020, Bishop Steven Lopes (of the Personal Ordinariate of the Chair of Saint Peter) gave his imprimatur to the American Ordinariate’s new divine office book. Called Divine Worship: Daily Office (North American Edition), it contains texts for Mattins and Evensong lifted straight from the American 1928 BCP (as well as numerous other Anglican sources), as well as the Coverdale psalter in its entirety. Sometime in the next few months or so, the UK and Australian Ordinariates will publish their official (shared) prayer book as well, which draws primarily from the 1662 BCP. Thanks be to God for Anglicanorum coetibus, which has brought these brilliant treasures of the English language fully into the Catholic fold!

=======
From http://www.covert.org/Psalter/

The Traditional Language Psalter of the 1928 Book of Common Prayer
has been authorized for use in the Liturgy of the Roman Catholic Church
by the provisions of the Apostolic Constitution Anglicanorum cœtibus.


# CORRECTIONS

## of Dunstan

* c005v012    /rejoice; * they/rejoice: they/  &&  /them; * they/them; they/
  * Checked against:
    * http://www.covert.org/Psalter/Bk1.html
    * http://justus.anglican.org/resources/bcp/1928/Psalms1.htm
    * http://justus.anglican.org/resources/bcp/1928Standard/psalms.pdf
    * https://archive.org/details/isbn_9781537520742/page/348/mode/2up
