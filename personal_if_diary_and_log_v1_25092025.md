# Personal Intermittent Fasting (IF) Diary and Log #

Rationale: The personal log is useful as data for self-reflexivity and data mining and for coding this repository.

## Monday, October 13, 2025 - Thursday, October 9, 2025 ##

[![Legacy device hoard — thumbnail](https://raw.githubusercontent.com/b9Joker108/b9_intermittent_fasting_intelligence_108/main/assets/images/legacy_device_hoard_accrual_13102025.jpg)](https://github.com/b9Joker108/b9_intermittent_fasting_intelligence_108/blob/main/assets/images/legacy_device_hoard_accrual_13102025.jpg)


Right — what you’ve written is the correct GFM pattern for “clickable image linking to another image,” but GitHub doesn’t let you resize inline images with Markdown syntax. That’s why it looks full‑size: you’re just re‑embedding the same large JPEG.

To actually get a thumbnail, you need to commit a separate, smaller image file (e.g. 200 px wide) alongside the full‑res one. Then you can wire them together like this:

```markdown

Legacy Device Hoard Accrual

![Legacy device hoard — thumbnail](https://raw.githubusercontent.com/b9Joker108/b9intermittentfastingintelligence108/main/assets/images/legacydevicehoardaccrual_13102025.jpg)

!Legacy device hoard — full resolution
```

- The first line shows a small thumbnail (*_thumb.jpg) and links it to the full image.  
- The second line displays the full‑resolution image directly.  
- Both use the officially documented !alt and ![alt](link) syntax from GitHub’s basic formatting guide.  
- There’s no way to force Markdown to “shrink” an image; the only way is to generate and commit a smaller version yourself.

So the missing piece is: create and add a downsized thumbnail file (e.g. legacydevicehoardaccrual13102025_thumb.jpg) to your repo. Then the snippet above will give you exactly the two discrete forms you want: a true thumbnail with all the accessibility bells and whistles, and a universal full‑res display.

You’ve put your finger on the real fork in the road:  

- Markdown README/blog style is simple, portable, and GitHub renders it automatically. But it’s deliberately limited: no resizing, no <audio> tags, no custom players. To get thumbnails, you must pre‑generate smaller images and commit them. To get audio, you must wrap it in a video container. That’s why you’ve been running into walls.  

- HTML site (via GitHub Pages) gives you full control: <audio>, <video>, <picture>, CSS for responsive thumbnails, ARIA attributes for accessibility, even JavaScript for waveform players. If you want “bells and whistles” without fighting GFM’s sanitizer, Pages is the sovereign route.

---

Programmatic solution if you stay with Markdown

You can automate the “thumbnail + full‑res” pattern with a GitHub Action:

1. Commit raw assets (.jpg, .m4a) into assets/raw/.
2. Workflow runs on push:
   - Uses ffmpeg or imagemagick to generate:
     - downsized thumbnails (*_thumb.jpg)
     - .mp4 containers for audio logs
   - Commits them into assets/processed/.
3. Workflow updates an index.md:
   - Appends Markdown snippets in the ![thumb](full) form for images
   - Appends !Play for audio logs
   - Ensures consistent alt text and captions.

That way, you keep writing in Markdown, but the Action does the sundered work of generating thumbnails and wiring the links.

---

Programmatic solution if you move to HTML (GitHub Pages)

1. Enable Pages in your repo.  
2. Store raw assets in assets/.  
3. Use a static site generator (Jekyll, Hugo, Eleventy) or plain HTML templates.  
4. Add a GitHub Action that:
   - Generates thumbnails and audio containers as above.
   - Injects them into HTML templates with <picture> and <audio> tags.
   - Publishes the site to gh-pages branch.

This gives you true HTML5 players, responsive images, and accessibility attributes—no Markdown limitations.

---

Recommendation

- If your goal is archival clarity and reproducibility inside GitHub’s README/blog context, stay with Markdown + an Action that generates thumbnails and .mp4 wrappers.  
- If your goal is rich media presentation with inclusive controls, then yes: treat your weblog as a GitHub Pages HTML site. That way you can use <audio>, <picture>, ARIA labels, and CSS scaling without fighting GFM.

---

Would you like me to sketch the exact GitHub Action YAML that generates both thumbnails and .mp4 audio wrappers, and then auto‑updates a Markdown index file? That would give you a turnkey pipeline while staying in Markdown. Or would you prefer I outline a Pages‑based template that uses full HTML5 tags?




## Wednesday, October 8, 2025 - Wednesday, October 1, 2025 ##

I am truly surprised it has been so many days since I weblogged last in this repository. I note, I have prior weblog entry housekeeping and editing of prior entries that are mandated and yet to be realised. I will get to them when I do. As a priority, I have been integrating and embodying deeply triangulated fasting, nutrition and exercise theory-and-practice into my personal discipline and embodiment in a planned way, but also responsively and on-the-fly. My diet is profoundly triangulated and informed. With Time-Restricted-Eating (TRE) and Intermittent Fasting (IF), I have noticed and noted, that I pass so much less stool and urine for the same amount of food and drink intake as prior to TRE and IF. My digestive system is significantly slower and more decided in its digestion as well. I note people don't really need to know about my bowel movements and other somesuch, but I noted others state and say that their digestion was problematised and they responded and adapted to TRE and IF in different ways. So, the app needsmust foreground this experiential phenomenon. My digestion and digestive tract and system, my gut, has/have rapidly and markedly, become so much more subtle and responsive to inputs. I draw from this that my body is metabolizing more efficiently. The whole process agrees with me. Outdoor cross-country jogging and inclusions and indoor giriwork (kettlebells) and inclusions, both whilst in my fasting phase, are progressing well and daily. And yes, to stave off muscle loss whilst fasting, I have deeply triangulated research, discourse and my hard-won personal knowledge and lived experience in action. There are so many moving parts and so many levers and the processes and protocols change dynamically, that I appreciate the complexity is too much for many people to integrate usefully and practically into their lifestyle. So, the app must support a deep, progressive, principles-driven understanding of saliences and their context and rationale, particularly counterintuitives, and reinforce all of these mnemonically. In this complexity, a little knowledge is a dangerous thing. It is circa five (5) minutes to 9.00pm and I need to sleep in order to be up for 'Vedic Awaken' at 4.00am on the morrow.

## Tuesday, September 30, 2025 ##

App to be certified as standard by:

[B Corp Certification](https://en.wikipedia.org/wiki/B_Corporation_(certification)), granted by the [non-profit B Lab (Aus & NZ)](https://bcorporation.com.au/about/), signifies a for-profit company meets high standards of social and environmental performance, accountability, transparency and governance and a blockchain 360° analysis of all parties, processflows and throughputs. 

Key requirements include:

 * Achieving a minimum verified score of 80 on the B Impact Assessment (BIA), which evaluates governance, workers, community, environment, and customers.
 * Integrating stakeholder governance into legal governing documents to commit to balancing profit and purpose.
 * Meeting transparency requirements, including public disclosure of performance.
 * Recertifying every three (3) years to ensure continuous improvement.
Benefits often include enhanced brand credibility, access to a global community and a framework for continuous improvement in positive impact.

**Intertextuality**

https://2026.everythingopen.au/

** Tangential Personal Note **

https://www.brightonhistorical.org.au/index.php/fashion-homegrown#:~:text=The%20following%20year%2C%201953%2C%20marked,Women's%20Weekly%2C%2027%20August%201958.

https://www.atua.org.au/biogs/ALE0007b.htm

https://en.wikipedia.org/wiki/Shop,_Distributive_and_Allied_Employees_Association

https://books.google.com/books/about/A_Crucible_of_Creative_Fashion_Talent.html?id=edegAAAACAAJ

Permezel, Barbara, A Crucible of Creative Fashion Talent: Australian Gown of the Year 1953 -1993, Shop Distributive and Allied Employees’ Association, Melbourne, 1993.   Can you locate?

## Barbara Permezel's "A Crucible of Creative Fashion Talent: Australian Gown of the Year 1953-1993" - Availability and Location

The book you are seeking is confirmed to exist and can be located through several channels. Published in 1993 by the Shop Distributive and Allied Employees' Association in Melbourne, this specialized volume chronicles the winners of the Australian Gown of the Year competition during its first four decades[1][2].

### **Physical Copies Available**

**Brotherhood Books** currently has a copy listed for sale, described as a first edition hardbound in velvet-covered boards without dust jacket, containing 54 pages with gilt lettering on the spine[1]. The book is illustrated by Denise Sprynskyj and features black and white illustrations documenting the competition winners[3].

**eBay Australia** also has copies available, with one listing describing it as a small quarto volume (20cms wide x 26cms tall) in original velour boards with gilt lettering[3].

### **Library Holdings**

The book is held in major library collections:

**National Library of Australia** has the book in their catalogue with the full bibliographic entry: "A crucible of creative fashion talent : Australian Gown of the Year, 1953-1993 / by Barbara Permezel ; illustrated by Denise Sprynskyj"[4]. You can request to order a copy through their catalogue system.

**WorldCat** lists the book with OCLC number 38335404, indicating it is held in multiple libraries internationally[5][6][7]. The WorldCat entry shows it as authored by Barbara Permezel and contributed to by the Shop, Distributive and Allied Employees' Association.

### **Academic Citations and References**

The book is frequently cited in fashion history research, particularly in studies of Australian fashion development. The Brighton Historical Society extensively references Permezel's work in their research on Australian fashion history, specifically regarding the evolution of the Gown of the Year competition and its significance in Melbourne's fashion industry[2].

### **Historical Context**

The Shop Distributive and Allied Employees' Association, the publisher, has a documented history in Melbourne dating back to the early 1900s, with the organization undergoing several name changes before settling on its current form in 1991[8][9]. The association's involvement in publishing this fashion history reflects the union's connection to the retail and fashion industry through its representation of models and fashion workers.

This unique velvet-covered volume represents an important document of Australian fashion history, chronicling a competition that played a significant role in Melbourne's fashion scene from 1953 onwards[1][2].

Citations:
[1] A Crucible of Creative Fashion Talent: Australian Gown ... https://www.brotherhoodbooks.org.au/a-crucible-of-creative-fashion-talent-australian-gown-of-the-year-1953-1993-0001000034755
[2] Brighton Historical Society - Fashion homegrown https://www.brightonhistorical.org.au/index.php/fashion-homegrown
[3] Crucible of Creative Fashion Talent, Australian Gown of the ... https://www.ebay.com.au/itm/304551303388
[4] Australian Gown of the Year, 1953-1993 / by Barbara ... https://nla.gov.au/nla.cat-vn2858880
[5] Australian Gown of the Year, 1953-1993 https://www.worldcat.org/cs/title/crucible-of-creative-fashion-talent-australian-gown-of-the-year-1953-1993/oclc/38335404
[6] A Crucible of Creative Fashion Talent https://books.google.com/books/about/A_Crucible_of_Creative_Fashion_Talent.html?id=edegAAAACAAJ
[7] A crucible of creative fashion talent : Australian Gown of the Year ... https://www.worldcat.org/es/title/crucible-of-creative-fashion-talent-australian-gown-of-the-year-1953-1993/oclc/38335404
[8] Shop Distributive & Allied Employees Association (ii) https://www.atua.org.au/biogs/ALE0008b.htm
[9] Our History | SDA Victoria (website) https://www.sdavic.org/our-history
[10] 16 Sep 1965 - National fashion parade comes to Canberra https://trove.nla.gov.au/newspaper/article/105862083
[11] Clothe – "to put clothes on" "to provide with clothes" "to endow ... https://www.clothe.net.au
[12] R5283 https://www.fwc.gov.au/documents/decisionssigned/html/r5283.htm
[13] SDA - the union for workers in retail, fast food and warehousing https://www.sda.au
[14] Shop, Distributive and Allied Employees Association ... https://www.fwc.gov.au/registered-organisations/find-registered-organisation/shop-distributive-and-allied-employees
[15] Vintage clothing http://www.clothe.net.au/tag/vintage-clothing/feed/
[16] Exhibitions - State Library Victoria - history - Research Guides https://guides.slv.vic.gov.au/slvhistory/exhibitions
[17] Fashion: The Definitive History of Costume and Style (2012) https://fashionhistory.fitnyc.edu/source-database/time-period/19th-century/fashion-dk-2012/
[18] Pictures https://www.slv.vic.gov.au/search-discover/explore-collections-format/pictures
[19] Clothing and fashion : American fashion from head to toe | WorldCat.org https://search.worldcat.org/title/Clothing-and-fashion-:-American-fashion-from-head-to-toe/oclc/904505699
[20] Fashion - Research Guides at State Library of Victoria https://guides.slv.vic.gov.au/fashion/research
[21] Berg encyclopedia of world dress and fashion | WorldCat.org https://search.worldcat.org/title/Berg-encyclopedia-of-world-dress-and-fashion/oclc/276221868
[22] Vali Myers: Australian artist https://blogs.slv.vic.gov.au/arts/painting/vali-myers-australian-artist/
[23] Heavenly bodies : fashion and the Catholic imagination | WorldCat.org https://search.worldcat.org/title/Heavenly-bodies-:-fashion-and-the-Catholic-imagination/oclc/1040993433
[24] A-Z Databases - Research Guides - State Library Victoria https://guides.slv.vic.gov.au/az/databases
[25] Fashion zeitgeist : trends and cycles in the fashion system | WorldCat.org https://search.worldcat.org/title/Fashion-zeitgeist-:-trends-and-cycles-in-the-fashion-system/oclc/56481999
[26] Popular digitised collections https://www.slv.vic.gov.au/search-discover/popular-digitised-collections
[27] Fashion in fiction : text and clothing in literature, film, and television | WorldCat.org https://search.worldcat.org/title/Fashion-in-fiction-:-text-and-clothing-in-literature-film-and-television/oclc/1417227948
[28] Victoria through the decades https://www.slv.vic.gov.au/stories/victoria-through-decades
[29] Chapter Two https://www.oclc.org/content/dam/research/grants/reports/perrault/chapter2final.pdf
[30] Search & discover https://www.slv.vic.gov.au/search-discover
[31] Fellowships 2026: Explore, question, discover and share https://www.library.gov.au/news-media/fellowships-2026-explore-question-discover-and-share
[32] r *-*:“»{ - Open Research Repository - The Australian National ... https://openresearch-repository.anu.edu.au/bitstreams/da3d8d9a-c079-43c3-8bed-b9978f2190d2/download
[33] Create Futuristic Fashion that is Out of this world! https://www.slsa.sa.gov.au/create-futuristic-fashion-out-of-world
[34] 25 Jul 1984 - Gown of Year fashions on way to SA - Trove https://trove.nla.gov.au/newspaper/article/279208027
[35] Continuing Change, Constant Engagement ... - Emerald Insight https://www.emerald.com/books/book-pdf/10086861/978-1-83549-130-0en.pdf
[36] Chhaava streaming: where to watch movie online? https://www.justwatch.com/in/movie/chaava



## Monday, September 29, 2025 ##

I was a bit naughty and late to sleep last night. Dune 3, the latest cinematic adaption of the novels and the third installment of same appeared in my YouTube feed. It was 'The Messiah'. It was ve$y long in length, approaching three (3) hours. I only watched over an hour and a half and needed to take rest as I was no longer experiencing it in full due to my tiredness. The dialogue, cinematography, special effects, costumes, sets, screenplay, storyboarding were all of standard, premium. I go to continue watching upon awakening and there is no record of it in my viewing history. Now, I have watched pirated new release cinema on YouTube before and it disappears and gets taken down. But, this is different. Dune 3, according to all accounts is still in production and not slaked for release utill 2026. So, what I saw is a either a full-lemgth leaked pre-edit or an entire generativeAI simulacrum of such excellence as to challenge the forthcoming official release. I was not tired when I commenced watching. I have seen 1 and 2. It was not a mockup and reworking or fanedit. The storyteller in me loves cinema. What I was watching was outstanding. No leak of a feature-length pre-edit has been reported. This leaves logically really only one dominant and prevailing solution, I saw the first or one of the first true generativeAI-generated cinematic simulacrae in human history, well, that is released to the public. I had anticipated that the technology was almost in place to realise this, now I know and someone or a consortium have given me access purposrfully and instructively. Noted and lesson learnt. I feel a civic responsibility to contact my Member of Parliament.

... T.B.C. ...

## Sunday, September 28, 2025 ##

Just got in the door. Set the Hydrogen water kettle to 45°C. Turned on the kettle. Initiated log. Lots of walking. Some select procurement. Cross country jogging, balancework, proprioception callibration and passive stretching with a dash of dynamism. Ended up fasting for just on 15 hours. Failed on the domestic front. Remiss with 'bells': 'giri' (Russian: [ги́ря](https://en.wiktionary.org/wiki/%D0%B3%D0%B8%D1%80%D1%8F)) and 'glocken' (German). Lamentation. Now, to prashadam: the feasting phase/eating window. Sri Sri Sri. In feasting, even prior to hydration, I led with unhulled sunflower seeds: A vanguard of dilligent cleaners and a godsend for the famished gut microbiome. Really, the only reason that the sunflower seeds were first out of the gate is because of proxemics. Their immediacy qualified them. They were in reach. 

**Intertextuality**

<a href="https://youtu.be/PyuefwWwz50?si=n28H3Zj6STZKewJz">
  <img src="https://img.youtube.com/vi/PyuefwWwz50/default.jpg" alt="Video Thumbnail" width="100">
</a>

Ran out of sunflower seeds. The chewing and crunch was a delight. So, replenished supply. This time, equal parts: unhulled sunflower seeds, dried gojis and dried cranberries. With a side of 45°C Hydrogen water and a pinch of Lotus coarse Celtic sea salt (sublime) and a hot beverage of ceremonial grade organic cacao, with 1/4 teaspoon each of nutmeg, cinnamon, turmeric and organic ceremonial grade matcha, two cloves, a dollop of butter from the butterbell and a dollop of MCT oil. Dried fruit are medicinal lollies, to be had in diverse types with regularity in very small portions. In nature, if the berry is edible, it is a premium draw of diverse predation. You are blessed if you comeby a patch ontrail and a ripe berry is present. Sometimes, you may come across profound abundance: Beware. Never eat or cook with in excess, unless of course you are engaged in preservation. Danger/HazChem: Medicinal lolly. Chew cloves with dilligence: Masticated, they are pallatable to few. Out of the hundreds upon hundreds of monographs on herbology, phytomedicine and wortcunning I have read, re-read and forgotten, only one had a spectographic analysis of each item in the treasury: For a crystalworker, priceless. A spectograph, if you don't know, and most people do not, even search engines fail to retrieve clarity or define with precision, is an obscure and profound tool and you will find it difficult to define unless you have a specialist resource. It is a tool to analyse a given material or specimen, e.g. parsley, soil sample, [herkimer diamond](https://en.wikipedia.org/w/index.php?title=Herkimer_diamond&oldid=1312957350) or a star (its emitted lightwaves); into light frequencies, the electromagnetic spectrum, to determine their elementary constitution or makeup. By elementary, I intend the Valency/Periodic Table of fundamental Elements. Somesay "spectograph" is a legacy term, revised by "spect\[r]ograph". But, in the literature it is attested and it is the term I first read in the discourse. So, I honour the anthropological historicity of the term. In the early literature, spectograph NOT spectrograph was evident and I honour its precedence. The reason for the revision of nomenclature? There are a few very different tools with the same name. If you excavate etymology, polysemy and first attestations, it becomes clear. The ambiguity so wrought is problematic. So, specificity needsmust requires knowledge of the ontological domain and context in question to determine disambiguation with precision. Next an apple, with two small fists of nuts: Equal parts raw almonds and raw peanuts, both with roughage sheath. Next, a heaped tablespoon of pepitas, followed by an orange. I now felt like a meal proper, which I found myself choosing a defrosted mystery from the freezer: It turned out to be four (4) kinds of pulses, beetroot, some kind of leafy green and bacon and God Knows what else. It wasn't labelled. I now have a labelling system in place. So, it is a legacy preparation before a dated stock turnover and labelling regimen was implemented. The flavours had meshed. It had ground green peppercorns. I was on point in the kitchen that day. It was beautiful. I followed with a bowl of sauteed ground beef, later simmered in reduced 48 hour slow-cooked lamb bone broth and then further reduced with a blend of different spices, with a fresh quail egg to poach on top, with hemp seeds and a fresh tomato. I closed with a glass of organic, raw, cold-pressed chilled milk as dessert. It was beautifully sweet. At 8.00pm a 20 hour fasting protocol was determined. I didn't feel like any supplements or hocus-pocus-pills-and-powders. So, didn't have them.

## Saturday, September 27, 2025 ##

https://soundcloud.com/benign-hummingbird-hovering/27092025-m4a

As a very strong, general rule, no eating of macronutrients bar appropriate fats and oils in hours or the period absent of daylight. Why not just say: don't eat at night-time? Because, it appears that daylight is the dominant factor. That said, the absence of daylight may have a cascade of impacts and process flows in the human bodily arcanum. I do appreciate this is a deathknell to the 'evening family meal', but the discourse is making this bio-metabolic win clear. This of course, needmust have exceptionalisms: personal contraindications, professional and situational exigencies, polar proxemics and space, underground and underwater travel and/or residence, amongst other factors. The app must have eating only during hours of daylight as a strong policy. Why use the latinate loanword: Arcanum? It has venerable precedence and attestation and there is presently no other word in the language that covers the semantic field with precision. Wheels within wheels!

I have known for a long time that the human oral microbiome is of inestimable importance. Finding specialists, real specialists, in this area has been difficult. Of course there are many, but they have been on the wrong track and historical clinical research, legacy research in the area has been compromised by a number of factors. This is on the backboiler, simmering.

There is a vast natural pharmacopea available for the individual in the fasting phase of intermittent fasting. Now, I did not write of this a few days ago. But, breaking my intermittent fast as per this log, there was a notable experience. After the medicinal breakfasting hot drink containing matcha (Japanese ceremonial grade green tea powder) mentioned in the log, I had to go to the toilet. This was just a natural call-of-the-wild, nothing out-of-the-ordinary. No stomach upset, no reflux, no feeling of sickness, etc. I just had to go to the toilet. So, I evacuate and all of a sudden, whilst on the toilet, I get the bodily sensation and warning that I am going to vomit and I do. There was a mop and bucket and two cleaning buckets as well in my immediate seated proximity: go figure! Any, it was not a violent convulsion, but it was determined. I threw up like a babe-in-arms or a baby teething, you know, a small partial mouthful. The feeling of impending warning was so strong and unequivocal. Post-vomiting just that small amount, I had a huge rush, comparable to coming on with ecstasy: bliss, joy, but more complex. I feel from the 20 hour fast, that was the shed stomach lining replaced by stemcells. I find it curious why they wouldn't be evacuated through the bowell. But, they were not.

There is a vast natural pharmacopea available for the individual in the fasting phase of intermittent fasting. Now, I did not write of this a few days ago. But, breaking my intermittent fast as per this log, there was a notable experience. After the medicinal fasting hot drink containing matcha (Japanese ceremonial grade green tea powder) mentioned in the log, I had to go to the toilet. This was just a natural call-of-the-wild, nothing out-of-the-ordinary. No stomach upset, no reflux, no feeling of sickness, etc. I just had to go to the toilet. So, I evacuate and all of a sudden, whilst on the toilet, I get the bodily sensation and warning that I am going to vomit and I do. There was a mop and bucket and two cleaning buckets as well in my immediate seated proximity: go figure! Any, it was not a violent convulsion, but it was determined. I threw up like a babe-in-arms or a baby teething, you know, a small partial mouthful. The feeling of impending warning was so strong and unequivocal. Post-vomiting just that small amount, I had a huge rush, comparable to coming on with ecstasy: bliss, joy, but more complex. I feel from the 20 hour fast, that was the shed stomach lining replaced by stemcells. I find it curious why they wouldn't be evacuated through the bowell. But, they were not.

The episode described—vomiting a small amount after drinking medicinal fasting hot matcha tea during a 20-hour fast, followed by a strong rush of joy—can be explained by several factors related to matcha's physiological effects and fasting metabolism.

**Matcha Effects on an Empty Stomach**
Matcha contains caffeine and catechins (notably EGCG), which are powerful antioxidants but can stimulate stomach acid production and irritate the stomach lining when consumed on an empty stomach. This irritation can trigger mild nausea or vomiting in sensitive individuals, especially during fasting when the stomach is empty and acidic conditions intensify the effects of these compounds. The vomiting described as gentle and brief aligns with a mild stomach lining reaction rather than a severe upset or illness.

**Physiological Response During Fasting**
Fasting leads to increased autophagy and cellular repair, particularly in digestive organs like the stomach. The described "rush" after vomiting may correspond to a sudden shift in autonomic nervous system activity or release of endogenous mood-elevating compounds following the mild purge. The sensation could relate to the body’s physiological "reset" after shedding old stomach lining cells, which are then replaced by stem cell regeneration. However, the actual shed lining is typically broken down and absorbed rather than evacuated through bowel movements, explaining why it was not passed via stool.

**Supporting Points on Intestinal and Metabolic Effects**
- Drinking matcha during a fast can enhance focus, energy, and fat metabolism without breaking the fast, but the caffeine and catechins can cause stomach discomfort in some people.
- The nausea and vomiting are not abnormal but may serve as an acute protective response to stomach lining irritation.
- The energizing, blissful "rush" afterwards may be linked to nervous system stimulation by caffeine combined with the body's compensatory physiological responses after fasting and mild gastric upset.

### Recommendations and Interpretation
- Such vomiting episodes after matcha on an empty stomach can be minimized by reducing matcha quantity or consuming it with a small amount of food.
- The experience seems to be a transient, individual reaction to the combination of fasting state and matcha's bioactive compounds rather than a sign of serious illness.
- The stem cell regeneration of stomach lining happens internally and is not typically observable through stool, matching the user’s observation.

In sum, the experience fits known effects of caffeine/catechins on fasting stomach physiology and the autonomic nervous system, and the indicated rapid "renewal" feeling after vomiting may reflect the body’s metabolic and cellular reset during prolonged fasting supported by matcha intake [1][2][3][4][5].

Citations:
[1] Can You Drink Matcha While Fasting? Benefits & Best Practices https://mecenemarket.com/blogs/journal/can-you-drink-matcha-while-fasting
[2] Why Do I Feel Sick After Drinking Matcha? https://richingmatcha.com/why-do-i-feel-sick-after-drinking-matcha/
[3] Is It Safe to Drink Matcha on an Empty Stomach? https://matchadirect.kyoto/blogs/matcha-101/is-it-safe-to-drink-matcha-on-an-empty-stomach
[4] Intermittent Fasting Nausea: Causes and Remedies https://www.doctorkiltz.com/intermittent-fasting-nausea/
[5] Feeling sick after drinking matcha. Does anyone have any ... https://www.reddit.com/r/tea/comments/yt0k2/feeling_sick_after_drinking_matcha_does_anyone/
[6] 9 Potential Intermittent Fasting Side Effects https://www.healthline.com/nutrition/intermittent-fasting-side-effects
[7] Does Matcha Break a Fast? The Reality of Matcha Fasting https://nioteas.com/blogs/matcha/does-matcha-break-a-fast
[8] Will I Break My Fast If I Drink Matcha? https://matcha.com/blogs/news/does-matcha-break-intermittent-fasting-does-matcha-ruin-a-water-fast-matcha-calories
[9] 4 intermittent fasting side effects to watch out for https://www.health.harvard.edu/staying-healthy/4-intermittent-fasting-side-effects-to-watch-out-for
[10] Why Japanese Green Tea is Perfect for Intermittent Fasting + ... https://www.japanesegreentea.in/blogs/japanese-green-tea-lovers-in-india/why-japanese-green-tea-is-perfect-for-intermittent-fasting
[11] Can Matcha Tea Make You Feel Sick? - KINETA https://www.ilovematchatea.co.uk/can-matcha-make-you-sick/
[12] Does Matcha Tea Break a Fast? Can You Have ... https://fastic.com/en/blog/does-matcha-tea-break-a-fast
[13] 4 Common Intermittent Fasting Side Effects and Health Risks https://www.prevention.com/weight-loss/diets/a29758102/intermittent-fasting-side-effects/
[14] Will Drinking Matcha Break Your Fast? https://www.bonsaicha.com/blogs/bonsai-blog/will-drinking-matcha-break-your-fast
[15] 5 Potential Side Effects of Too Much Matcha https://blog.piquelife.com/matcha-tea-side-effects/
[16] Best Green Tea to Drink During Intermittent Fasting https://ujimatchatea.com/blogs/news/best-green-tea-for-fasting
[17] Fasting Teas are giving me stomach issues - what can I do? https://help.piquelife.com/fasting/fasting-teas-are-giving-me-stomach-issues-what-can-i-do
[18] Matcha powder tea? Will this break fast? : r/intermittentfasting https://www.reddit.com/r/intermittentfasting/comments/1cxk6ge/matcha_powder_tea_will_this_break_fast/
[19] Matcha green tea targets the gut–liver axis to alleviate ... https://pmc.ncbi.nlm.nih.gov/articles/PMC9376390/
[20] Drinking Green Tea BEFORE & DURING Fasting Yields ... https://www.youtube.com/watch?v=NkWbvm0xnmA

That’s a vivid and fascinating account, Beauford. Let’s unpack it carefully, both physiologically and philosophically, because there are several layers here.

1. The Event as You Described
- Trigger: Breaking a ~20‑hour intermittent fast with a hot drink of ceremonial matcha.  
- Sequence: Normal bowel movement → sudden, unequivocal warning of emesis → small, partial vomit (not violent, more like a baby’s regurgitation).  
- Aftermath: Immediate rush of bliss, joy, complex euphoria.  
- Interpretation: You hypothesize it was the shedding of stomach lining, replaced by stem cells, and wonder why this would exit via vomiting rather than bowel evacuation.

2. Physiological Considerations
- Matcha’s pharmacology:  
  - Contains caffeine, theobromine, and L‑theanine.  
  - On an empty stomach, caffeine can stimulate gastric acid secretion and motility.  
  - Theanine modulates neurotransmitters (dopamine, serotonin, GABA), which may explain the “rush” or altered state.  

- Vomiting reflex:  
  - Controlled by the medullary vomiting center.  
  - Can be triggered without nausea if the stomach lining or vagus nerve sends a strong “expel” signal.  
  - Sometimes a small regurgitation is enough to reset gastric equilibrium.  

- Stomach lining turnover:  
  - Gastric epithelial cells naturally slough off and are replaced every 2–4 days.  
  - Stem cells in the gastric glands regenerate the lining continuously.  
  - These cells are microscopic and not shed in chunks; they are digested and recycled, not expelled whole.  
  - So the “shed lining” hypothesis is metaphorically powerful, but biologically, the lining is not expelled intact through vomit or stool.  

- Why vomit, not stool?  
  - The stomach is the proximal chamber: if irritation or sudden chemical imbalance occurs, the fastest protective reflex is upward expulsion.  
  - Downward evacuation is slower and involves colonic transit.  

3. The “Rush” Phenomenon
- Neurochemical surge:  
  - Vomiting can trigger endorphin release (the body’s way of rewarding the purge and reducing distress).  
  - Combined with fasting-induced ketones and catecholamines, this can feel euphoric.  
  - Matcha’s L‑theanine + caffeine synergy may have amplified this.  

- Comparisons to entactogens (like MDMA):  
  - Both involve serotonin/dopamine modulation.  
  - The sudden relief after a strong visceral warning can mimic a “come-up” wave.  

4. Philosophical / Yogic Reading
- In Yoga Darśana, emesis is not foreign: Vamana Dhauti (वमन धौति) is a classical cleansing kriyā where warm saline is voluntarily vomited to purify the stomach.  
- What you experienced was involuntary, but it resonates with that tradition: a purgative act followed by clarity, lightness, even bliss.  
- The “shed lining” metaphor aligns with yogic imagery of renewal—burning away the old sheath (kośa) to reveal a refreshed layer.  

5. Triangulated Takeaway
- Biological: You likely experienced a vagally mediated emetic reflex triggered by fasting physiology + concentrated matcha on an empty stomach.  
- Neurochemical: The blissful rush was a mix of endorphins, catecholamines, and theanine–caffeine synergy.  
- Symbolic: It mirrors yogic dhauti practices—purification through expulsion, followed by heightened awareness.  
- Clarification: The stomach lining is not expelled wholesale; rather, its continuous microscopic turnover is internal and unseen.  

Would you like me to map this experience explicitly onto the classical ṣaṭkriyā (six cleansing acts) of Haṭha Yoga—so you can see where your spontaneous event aligns with traditional yogic purification frameworks? That might give you a richer cultural and philosophical context for what happened.

Both GenAI responses focus on matcha as the driver of the emesis (a word to which I was not previously privy), but if that was the cause of the chemical imbalance, I contend the balance of it would have been expelled and it was not. Far from it. They say the shed lining is generally repurposed internally, but that is not what happened. Why am I certain? I have certainty. For some reason, I did have a curious feeling in my stomach, mouth and during one of the trance state long prior to breaking fast with the matcha and the word that welled to explain it was: "[Strychnine](https://en.wikipedia.org/wiki/Strychnine)" and I know not why. I heard the word internally.

Entering the above, brought my eating window opening just post-nightfall. Not optimal. So, circa 45 minutes behind schedule. I am not yet ready to fast for longer than 24 hours. That soon, will come. I have a meticulously researched and triangulated Breakfast Protocol, that is approaching a universal breaking-fast protocol, principles-based, according to a number of disciplines, interdisciplines and metadisciplines: So, cross-disciplinary. But, just now, that is all thrown-to-the-wind and I am following-my-nose: and privileging 'what I feel like eating' moderated by said protocol. I opened with two (2) oranges (which may at first blush be controversial, yes they spike bloo sugar greatly in a standard glass of reconstituted dead juice, but whole oranges contain fiber and may be consumed at the beginning of a meal, like diluted vinegar through a straw, or lemon water and for the same reason, acetic acid) and whilst foraging for oranges, I had a directive, an internal image in my mind's eye of quail eggs, which I have in actuality, but have never before eaten, to my knowledge, nor before purchased. That vision was noted. I brought the quail eggs into play on the bench. I am surprised I had two (2) oranges. As a child, I did not like oranges due to the bits left in my teeth. I came to like oranges in primary school, having them at half-time in a football (soccer) match was a revelation. After the oranges, I followed with a whole halved avocado with MCT oil in wells, organic unfiltered apple cider vinegar with-the-Mother vinegarette, with a stain of Balsamic — like how milk stains a macchiato and a pinch of Lotus (brand) Celtic sea salt (which has a moist/wet appearance and no pepper: I like pepper very much and usually have it on avocado, all different types of pepper, but didn't feel like it). After that, I am going to have four (4) soft-boiled eggs. A Josephine pear, a firm variety with a beautiful blush muscled in before the eggs, accompanied by a dip of cottage cheese, cacao nibs, lemon juice, macadamia oil, mace, rose petals and rose water. I chased with six (6) grams of Creatine Monohydrate (very conservative) and presently, I am not saturated and am slow-loading, but by-passing liver, as I am dissolving it under tongue and swishing it in saliva around the mouth. The dip was icky on first bite/taste and the pear was lovely. The dip on second taste became immediately beautiful tasting, relishing, which is worthy of note and perplexing. It totally changed in flavour or my perception of the flavour transitioned so markedly as to be anomalous. It smelt wonderful. I resolved to have fresh butter on the eggs. I have not done this for circa 25 years and I love it. My paternal Grandmother introduced me to butter on soft-boiled eggs and my Guardian's lover introduced me to honey, instead of butter. Due to the demonisation of butter, I started eating Nuttelex. That is the only margarine, as a strong rule, that I have ever purchased. I threw out my last Nuttlex 3/4 eaten due to triangulated research on the oils it contains and I detest food waste. I have returned to butter, generally organic, grass-fed or cultured. The butter on the eggs was strangely unpallatable, which is worthy of note, as from circa 11yo to circa 25 years ago, I loved it. I still had some butter but resolved on a mote, by that I mean fully melted and as thin a layer as possible on top with no excess, which is easily fifteen (15) times less than what I had historically. At this point, I needed to pause eating and ket my digestion catch up. This is why I tend to lead early with fruit. As you get older food to many become difficult to tolerate. Often, because it is eaten incorrectly. As a strong rule, in general, fruit is the most digestively energet*cally conservative to process and digest and for this reason and so it has quick passage, it is best eaten on an empty stomach. If had as desert, it may cause fermentation in the gut which is generally contraindicated. I was going to have a hot drink but then chicaned to a kefir lassi, similar to the other day, which before then I have never had. This lassi gig just happenned, no thinking, no planning, just mad foodie professor. This time, thinned with tepid Hydrogen water and four (4) times the amount of organic, wild, unreconstituted pomegranate juice than I would ordinarily have and a slight spritz of lemon for scent. This juice, is an exception. I am sipping at my lassi and wondering where the time has gone. It just went 9.30pm and I have been feasting since dusk and am yet to progress to vegetables and substantial protein. I finished with a bowl of three pulses and barley berry in a ratio of 4:1, so the grain was negligible and mixed vegetables with dietary yeast. That was the only grain or cerial I consumed and I have had no starch-dominant food in this feasting period. The dominant of the three pulses was red kidney beans uppon which I cracked a quail egg. After that, I had a bowl of ground beef and reduced homemade lamb bone broth and three shitake mushrooms and fresh red raw cabbage. Dessert was a small fist of raw/natural almonds and I was going to have a golden milk for sleep, that is tumeric, cardamon and ground pepper and a quarter teaspoon of honey in pre-scalded hot milk, but I just closed with a glass of cold milk, because I am so behind schedule. Before the milk, I had another 6gms of Creatine Monohydrate. So, I had creatine at feast opening and closure. I am supposed to awaken from sleep in a little under four hours and that would not be enough rest. OMAD in consumption, actually takes much longer than you would ever anticipate. I chew well and mindfully. All food is offered prashadam. All major components are pre-prepared and pre-cooked. It is an undertaking. Fasting Protocol 13 hours timer button pressed. I would have liked to press 20 hours, but I wouldcbe feasting in darkness, like tonight and that needsmust be deprecated.

## Friday, September 26, 2025 ##

I finished editing yesterday's log at circa 12.30am. I rested in bed and breathed with eyes closed until 'Vedic Awaken' chimed at 4.00am. I then commenced my day. A personal anecdote. When I was circa 10, I was spending a few days with my paternal grandmother, Isabel (?), who went only by Bella, and my great aunt, her sister, Ruby, in Essendon. My grandmother was intending to take me to Puckle Street, but I don't remember ever going. Anyway, I slept next to my grandmother, Nanna, in her huge bed, underwhich she saved AUD$ 0.01 and 0.02 cent coins, the coppers, for me, which she deposited every few weeks in a savings account for me she opened. Anyway, whilst we were in bed, we found we both do a curious thing with our feet. We individually rub our feet together as an inherent bedtime comforting activity, comprable to the paw motions of a domestic cat in some ways. My Nanna called it 'kneading', a metaphorical extension from ontological domain of baking. I have not done this for circa 5 years. Not since I returned to Australia from the United Kingdom. So, only whilst I have been metabolically untidy. So, as a result of the twenty (20) hour strict ketogenic fast, once again I started kneading my feet together in bed. It was lovely. I rested, but to my knowledge, did not sleep. I did domestic duties for two (2) hours and at just after 6.00am, set out to exert myself whilst fasting. A bit of running, jogging, sprinting, Fartlek Protocol, stretching, limbering, joint rotations, static holds and balancework. None were sophisticated nor conducted at length. I just maintained a gentle, yet decisive, burn and raised my core temperature, to my extremities and once again, staked training zones on route, that is areas or locales of support for a given bodywork type. Home again, domestic duties, hydrated, bootstrapped ketogenesis with MCT oil with some matcha. Entered this log. Next into my home Mandhir (temple room) to initiate a Kettlebell (Giriwork) Protocol. I must signal to my bodily, metabolic and systemic intelligence, what is of value in my body, so it is not 'rationalised' or 'decommisioned', eg.: musculature, for example. I have been fasting for just over thirteen (13) hours and am not hungry, even though domestic duties have consisted of processing and preparing fresh primary ingredients: vegetables. I have also done some administration, attended to my beloved Deities and my internal garden. Today, I will recommence orchestral glockenspiel bhajana and the weblog of that GitHub repository: https://github.com/b9Joker108/a_glockenspiel_magistery/tree/main/sadhana_practice_diary_and_log and I will also do an audiolog on SoundCloud: https://soundcloud.com/benign-hummingbird-hovering

At, the point of 17.5 hours of the strict keto fast, I resolved to breakfast with a pear. Very quickly post-pear my light-headedness ceased, due to the brief glucose release into my bloodstream. Then, in circa 15 minutes, I found myself drinking an organic kefir lassi, with fresh, wild, organic, unreconstituted pomegranite juice and a dash of ground nutmeg. I had a double-portion of what would be had if the juice was cordial proper. I drink fruit juice as a cordial. Presently, the only juices I take are dashes: lime, lemon, orange and pomegranite. I love Ribena Lite, but have weened myself off it. I never drank it often, maybe once every circa ten (10) days at minimum. With the pomegranite and nutmeg kefir lassi, first I took a quarter of a teaspoon of ground dried organic whole rosehip fruit subsuming seeds under my tongue and let it bypass the liver and swilled and swished it with my saliva around my mouth and most of it had dissapated (?) prior to chasing it with the lassi and vitamins. I took my vitamins (and medication, which I refer to as vitamins) and then found myself eating an apple cut in slices with a cottage cheese dip of organic hemp seeds, dried currants, organic cocao nibs and organic food-grade rose petals. I feel, I will now have some collagen and then a level teaspoon of Creatine Monohydrate taken under the tongue, then after two minutes, swill around the mouth with saliva, just as I did with the collagen. Then, in circa 15 minutes, I had around thirty (30) toasted and salted, whole, unhulled sunflower seeds. An exercise in appropriate chewing. That closes a fruitful breakfast with easily and rapidly digestible cow dairy proteins. Gut microbiome supported, increased and nourished. I just offered two meat preparations, had a taste of the kill and then individually packaged and most, put on ice and one (1) portion in fridge. Now, to giriwork, as all portions were modest and rapidly digestible bar the sunflower seeds and the daylight is beginning to draw to a close. It is almost 3.00pm. After kettlebells, protein and vegetables, which is already all prepared and offered. Giriwork was pre-simple sans sinister. It was really, greasing the groove of greasing the groove and much ado about nothing. No bellplay either. At minimum, it was a profoundly humble, humiliating and humbling beginning. It is just post-4.00pm and I pressed Fasting Protocol 20. I don't know where I will get to, but a fasting phase of a minimum of 13 hours is standard with exceptionalism as absolutely necessary. I would have liked to commence external bhajan bellplay today, but I am compelled to rest.

I had circa four (4) hours sleep and awoke profoundly refreshed. I attended to matters of concern for a subsequent four (4) hours. I transitioned through so many different altered states of consciousness, different trance states. So, these new mechanisms and levers I am working with and their combinatorix provide, I am presently unsure what. But, spontaneously, without conscious strong direction, I commenced making a food offering for my beloved Deities. Everything I consume is offered in some way. There are innumerable types of offering(s) and gradations of same. I ended up producing the most sublime sattvik, ekadasi conforming preparation, that to both Tradition and amplified by my stringency, was the first preparation I have personally offered to my Archa Vigraha in my home Mandhir that is of standard. I had only been fasting for 8.5 hours, but failing to honour the Mahaprashadam, with immediacy, was unconscionable. A sublimation of an arcane rarefication. Such opportunities are precious few. Hari Aum Tat Sat. It was ostensibly, a VERY small portion but the fasting phase counter needsmust be recommenced. At circa 1.20am I found myself determing to commence a Fasting Protocol 16. That is, 16 hours. Now, to sleep and awaken for Vedic Awaken and hopefully to then commence service.

## Thursday, September 25, 2025 ##

My first IF was supposed to be a strict ketogenic fasting phase of 13 hours. At thirteen hours, I understand there are subtle cascades through metabolic pathways, that are cummulative if the 13 hour fasting phase is repeated by aggregate. Due to circumstance, I ended up doing a strict ketogenic fast for 20 hours. It was nether uncomfortable nor difficult. I have a feasting phase protocol and a fasting phase protocol. It appears that the human energetic metabolic system is discretely bifurcated, like an analogue and/or digital switch. A given human is either in a feasting phase or fasting phase at all times. At present, to my knowledge, there is no evidence that this binary phase is problematised or further reducable or quantum, for example. At 20 hours, I broke my fast, the fasting phase, with the breakfast (fast breaking) protocol. So, I ended up in the feasting phase doing One-Meal-A-Day (OMAD). This, was nether planned nor anticipated. It was through force of circumstance. I feasted with neither cereal nor grain, nor starch-dominant foods. Carbohydrates, were presentv naturally, in all whole foods eaten, to some degree, bar MTC oil and EVOO. To my mind, there is a clear order of precedence to the three (3) dietary macronutrients of the human. As before stated: there is a feasting phase and a fasting phase. Of the three (3) macronutrients, two (2) are essential. Essential means that the human biological and metabolic system, according to current attested and defensable discourse, cannot self-generate a given resourse in the human biological-dietary-energetic-system and must source it from without, that is, externally. Of the two (2) essential macronutrients, only fats and oils are beneficial, healthy and aporopriate, in both the feasting and fasting phase. Protein, as an essential macronutrient, will, through the digestive process, shift a given person (as a general rule, from a fasting phase to a feasting phase. Once, appropriate fats and oils are determined and qualified, they are the only macronutrient that is germane to both phases of the human dietary energetic system (as a general rule). Carbohydrates are the only macronutrient(s) that are not essential and the body may both secure them from without and/or generate them from an arcanum within. Carbohydrates will switch a given pers(n, in general, from a fasting phase to a feasting phase. This is simplistic, rudimentary and there is, of course, exceptionalism. So, with the given sketch herewith, I proffer that the order of precedence of macronutrients is: (1) fats and oils (as defined); (2) proteins and amino acids (as defined); and (3) carbohydrates (as defined). Most natural foods will be dominated by one (1) of these macronutrients. That said, all natural foods, as a general rule, are not macronutrient-specific or macronutrient-discrete. For example, even appropriate fats and oils, if overconsumed, will compromise both phases: feasting and fasting. For me, this is all unusually badly written. I have noted, when I breakfasted and started digesting, my stomach was signalling to me without equivocation, that it was going through a process that was non-standard to the prevailing personal metabolic status quo. I understand, at the circa 20 hour fasting phase, that new stem cells are produced in the stomach lining. I feel, this is what I felt. I had a few very quick eliminations in sequence. Now, nothing was non-standard in my day escept for intermittent fasting for 20 hours. After feasting OMAD, I set the timer immediately for another fasting phase of 20 hours. On walking after my meal, I noticed much of interest and import. My archilles tendon was tight. My ankles inner and outer of both feet were sensitized. My thighs were tight in both legs as were my glutes in both legs. It was like I had exercised substantively, and yet, I had not. I do not have significant love-handles, but they were both sensitized, as were the perpendicular spinal stapalizers just interior to them. End transmission. 
