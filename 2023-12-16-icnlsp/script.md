
## »Japan's Answer to Mozart«



### Automatic Detection of Generalized Patterns of Vossian Antonomasia



<br />


[Michel Schwab](https://hu.berlin/schwab/)¹, [Robert Jäschke](https://hu.berlin/RJ/)¹² and	[Frank Fischer](https://lehkost.github.io/)³
<br/>

¹ Humboldt-Universität zu Berlin,<br/>
² L3S Forschungszentrum Hannover,
³ Freie Universität Berlin<br/>
<br/> 

<!--<ul>
<li class="web">[vossanto.weltliteratur.net](https://vossanto.weltliteratur.net/)
<li class="doc">Schwab, M., Jäschke, R., Fischer, F., Strötgen, J.: ['A Buster Keaton of Linguistics': First Automated Approaches for the Extraction of Vossian Antonomasia](https://doi.org/10.18653/v1/D19-1647). Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing. pp. 6239–6244. Association for Computational Linguistics, 2019.
</ul>-->

<b> ICNLSP 2023</b>

<!-- keep me, otherwise this gets interpreted as an ordered list -->
<p style="font-size:.45em"> 16. December 2023 </p>

<p style="font-size:.25em">
<a rel="license"
href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative
Commons Lizenzvertrag" style="border-width:0" src="images/cc.png"/></a> <br/>
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.<br /><br />
Data and Code are available at our <a href="https://vossanto.weltliteratur.net/">Website</a>.
</p> 
<!-- .element: style="font-size:0.45em; margin-bottom: 0px; margin-top: 3em;" -->


<!-- ![Logos](images/logos.png) -->


---


## Content

<br />

1. [Defintion and Examples](#/1)
2. [Motivation and Difficulty](#/2)
3. [Data](#/3)
4. [Methods](#/4)
5. [Evaluation](#/5)


---


# Defintion and Examples

--

## Definition

<br />

<!--[portrait of Gerhard Johannes Vossius; source: Wikimedia Commons](images/vossius.jpg)
 .element width="100px" --> 

- a trope, closely related to metaphor and metonymy
- special case of general antonomasia
- attributing a particular property to an entity by naming another named entity, that is typically well-known for the respective property




![VA Example](images/example.png)
<!-- .element width="450px" -->


<small>
image sources: <a href="https://commons.wikimedia.org/wiki">Wikimedia Commons</a></small>


--


## Examples

<br />

![Jim Koch, the Steve Jobs of beer](images/the-steve-jobs-of-beer_theatlantic-com.jpg)<!-- .element height="400px" --> 

<br />

= Jim Koch (Quelle: [theatlantic.com](https://www.theatlantic.com/magazine/archive/2014/11/the-steve-jobs-of-beer/380790/), 2014)


--

## Examples

<br />

![Tatsuo Horiuchi](images/michelangelo-of-excel.png)<!-- .element width="400px" -->

<br />

= Tatsuo Horiuchi (Quelle: [theschedio.com](https://theschedio.com/painting-on-excel/), 2020)
 

--

## Examples

<br />

![Truffles](images/mozart-of-mushrooms.png)<!-- .element width="400px" -->

<br />

= Truffles (Quelle: [capeinsights.com](https://www.capeinsights.com/the-mozart-of-mushrooms/), 2021)


--

## Examples

<br />

![Modern Meteorology](images/dangerfield-of-sciences.png)<!-- .element width="400px" -->

<br />

= Modern Meteorology (Quelle: [delawareonline.com](https://eu.delawareonline.com/story/opinion/columnists/1/01/01/the-roger-dangerfield-of-sciences/3663375/))

---

# Difficulty and Motivation 

--


##  Difficulty - Understanding

 
<br />

&rarr; requires deep cultural background kowledge

<table>
    <thead>
        <tr>
            <th>VA Phrase </th>
            <th>Explanation</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>the <span class="vasource">Dolly Parton</span> of <span
   class="vamodifier">cakes</span> </td>
            <td>a little bit tacky, but you love her</td>
        </tr>
        <tr>
            <td>the <span class="vasource">Donald Trump</span> of <span
   class="vamodifier">the horse show world</span> </td>
            <td>buying and selling horses like so many pieces of real estate, pocketing a profit and never shedding a tear as she watches her property being trucked away</td>
        </tr>
    </tbody>
</table>


--

## Difficulty - semantic ambiguity

<br />

<table>
    <thead>
        <tr>
            <th>VA phrase </th>
            <th>literal phrase </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>the <span class="vasource">Beethoven</span> of <span
   class="vamodifier">traffic cops</span> </td>
            <td>the Beethoven of the 5th Symphony </td>
        </tr>
        <tr>
            <td>the <span class="vasource">Nobel</span> of <span
   class="vamodifier">maths</span> </td>
            <td>the Nobel of physics</td>
        </tr>
        <tr>
            <td>the <span
   <span class="vasource">Barack Obama</span> of <span class="vamodifier">2020</span> </td>
            <td>the Barack Obama of 2020 </td>
        </tr>
    </tbody>
</table>

--

## Difficulty - syntactic variations

<br />

<table>
    <thead>
  <tr>
    <th class="tg-0lax">the Mozart of Japan</th>
  </tr>
</thead>
<tbody>
  <tr>
  <tr>
    <td class="tg-0lax">the Japanese Mozart</td>
  </tr>
  <tr>
    <td class="tg-0lax">the Japanese answer to Mozart</td>
  </tr>
  <tr>
    <td class="tg-0lax">the Japanese version of Mozart</td>
  </tr>
  <tr>
    <td class="tg-0lax">the Japanese equivalent of Mozart</td>
  </tr>
  <tr>
    <td class="tg-0lax">Japan's Mozart</td>
  </tr>
  <tr>
    <td class="tg-0lax">Japan's answer to Mozart</td>
  </tr>
  <tr>
    <td class="tg-0lax">Japan's version of Mozart</td>
  </tr>
  <tr>
    <td class="tg-0lax">Japan's equivalent of Mozart</td>
  </tr>
</tbody>
</table>
</tbody>
</table>



--

## Goal and Approach

<br />

<section>
    <style>
        .custom-left-align {
            text-align: left;
        }
    </style>
    <p class="custom-left-align"><b>Goal</b>: Detection of syntactic variations of VA phrases</p>
    <ul>
        <li>Focus on source</li>
        <li>All named entities are source candidates</li>
        <li>Binary classification of candidates</li>
    </ul>
</section>


---


# Data 

<br />

--

## Data - Candidate Generation

<br />


1. Given: annotated dataset (Schwab et al. 2022)
  &rarr; 6,096 sentences (3,115 include VA phrases)
  
2. NER tagger ([FLAIR](https://github.com/flairNLP/flair) (Akbik et al. 2019)) for source candidates extraction
3. Tuples: (candidate, sentence, label)



--

## Data - Training Data

<br />

- 2,980 negative and 2,868 positive sentences from the annotated dataset

**&rarr; 16,877 Tuples (2,868 positive)**




--
## Data - Test Data

<br />

- lack of syntactic variations in dataset: (a|an|the) SOURCE (of|for|among) MODIFIER
- Idea: Data augmentation:
  - CP: (“answer to”,“version of”, “equivalent of”)
  - Modifier noun: MODIFIER’s (CP)? SOURCE 
  - Modifier adjective: (a|an|the) MODIFIER (CP)? SOURCE
- only works with a small subset: modifier as geographical places
- use adjectival and demonymic forms of place names from Wikipedia.
- 244 VA phrases (countries, cities, regions, continents)

**&rarr; 1,952 augmented sentences**

**&rarr; 8,480 tuples (2,196 positives)**






---

# Methods 


<br />

--

## Methods - Baseline
 
<br />

- Schwab et al. 2022
- fine-tuned BERT for sequence tagging
- Adaptation: source tagging only

--

## Methods - BERT-MASK 
 
<br />

- Li et al. 2020
  - metonymy resolution
  - masked word classification (context is important)
  - BERT based
- Adaptation: masking source words with a single token


--

## Methods - Linguistic Metaphor Theories 1

- MIP (Metaphor Identification Procedure)
  - word is metaphorical if literal meaning deviates from its contextual meaning
- Choi et al. 2021 
  -  RoBERTa
  - compute embedding for isolated and contextualized candidate
  - binary classification of the  concatenated embeddings
- Adaptation to source

--

## Methods - Linguistic Metaphor Theories 2

- SPV (Selectional Preference Violation)
  - word is metaphorical if it appears in unusual context
- Choi et al. 2021 
  -  RoBERTa
  - compute embedding for contextualized candidate and the aggregated embedding of the whole sentence
  - binary classification of the  concatenated embeddings
- Adaptation to source

--

## Methods - RoBERTa-CLF

<br />

- Highlighting source candidates by special tokens
  - [START_SRC], [END_SRC]
- fine-tune RoBERTa

--

## Methods - RoBERTa-PAIR

<br />

- Modeling as sentence-pair classification:
  - Pair: [candidate, sentence]
- fine-tune RoBERTa



---

# Evaluation

--

## Results - Training Data

<br />

</table> <table class="eval">
  <caption style="caption-side:bottom">Performance of the models using 5-fold cross
validation on the training dataset.</caption>
<thead>
  <tr style="border-bottom:2px solid black">
    <th>Model</th>
    <th>Precision</th>
    <th align='right'>Recall </th>
    <th align='right'>F<sub>1</sub></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">BERT_SEQ</td>
    <td class="tg-0lax">.88</td>
    <td class="tg-0lax"><b>.97</b></td>
    <td class="tg-0lax"><b>.92</b></td>
  </tr>
  <tr>
    <td class="tg-0lax">BERT_MASK</td>
    <td class="tg-0lax">.83</td>
    <td class="tg-0lax">.88</td>
    <td class="tg-0lax">.85</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_MIP</td>
    <td class="tg-0lax">.88</td>
    <td class="tg-0lax">.89</td>
    <td class="tg-0lax">.88</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_SPV</td>
    <td class="tg-0lax"><b>.93</b></td>
    <td class="tg-0lax">.85</td>
    <td class="tg-0lax">.89</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_CLF</td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.87</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_PAIR</td>
    <td class="tg-0lax">.76</td>
    <td class="tg-0lax">.94</td>
    <td class="tg-0lax">.84</td>
      <tr style="border-bottom:2px solid black">
  </tr>
  </tbody>
</table>

</div>


--

## Results - Test data

<br />


<style>
  .tg-0lax:nth-child(4), .tg-0lax:nth-child(7) {
    border-right: 1px solid #000; /* This adds a solid black border */
  }
</style>
</table> <table class="eval">
  <caption style="caption-side:bottom">Performance of the models on the test data which include the original and augmented data.</caption>
<thead>
  <tr>
   <tr style="border-bottom:2px solid black">
    <th class="tg-0lax"></th>
    <th class="tg-0lax" colspan="3">total</th>
    <th class="tg-0lax" colspan="3">original</th>
    <th class="tg-0lax" colspan="3">augmented</th>
  </tr>
</thead>
<tbody>
  <tr>
   <tr style="border-bottom:2px solid black">
    <td class="tg-0lax">model</td>
    <td class="tg-0lax">precision</td>
    <td class="tg-0lax">recall</td>
    <td class="tg-0lax">F<sub>1</sub></td>
    <td class="tg-0lax">precision</td>
    <td class="tg-0lax">recall</td>
    <td class="tg-0lax">F<sub>1</sub></td>
    <td class="tg-0lax">precision</td>
    <td class="tg-0lax">recall</td>
    <td class="tg-0lax">F<sub>1</sub></td>
  </tr>
  <tr>
    <td class="tg-0lax">BERT_SEQ</td>
    <td class="tg-0lax">.73</td>
    <td class="tg-0lax">.17</td>
    <td class="tg-0lax">.27</td>
    <td class="tg-0lax"><b>.99</b></td>
    <td class="tg-0lax"><b>1.00</b></td>
    <td class="tg-0lax"><b>.99</b></td>
    <td class="tg-0lax">.42</td>
    <td class="tg-0lax">.07</td>
    <td class="tg-0lax">.12</td>
  </tr>
  <tr>
    <td class="tg-0lax">BERT_MASK</td>
    <td class="tg-0lax">.69</td>
    <td class="tg-0lax">.15</td>
    <td class="tg-0lax">.25</td>
    <td class="tg-0lax">.92</td>
    <td class="tg-0lax">.81</td>
    <td class="tg-0lax">.86</td>
    <td class="tg-0lax">.52</td>
    <td class="tg-0lax">.07</td>
    <td class="tg-0lax">.13</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_MIP</td>
    <td class="tg-0lax">.92</td>
    <td class="tg-0lax">.62</td>
    <td class="tg-0lax">.74</td>
    <td class="tg-0lax">.97</td>
    <td class="tg-0lax">.92</td>
    <td class="tg-0lax">.95</td>
    <td class="tg-0lax">.91</td>
    <td class="tg-0lax">.58</td>
    <td class="tg-0lax">.71</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_SPV</td>
    <td class="tg-0lax"><b>.97</b></td>
    <td class="tg-0lax">.42</td>
    <td class="tg-0lax">.58</td>
    <td class="tg-0lax"><b>.99</b></td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.93</td>
    <td class="tg-0lax"><b>.97</b></td>
    <td class="tg-0lax">.36</td>
    <td class="tg-0lax">.53</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_CLF</td>
    <td class="tg-0lax">.73</td>
    <td class="tg-0lax">.29</td>
    <td class="tg-0lax">.41</td>
    <td class="tg-0lax">.95</td>
    <td class="tg-0lax">.82</td>
    <td class="tg-0lax">.88</td>
    <td class="tg-0lax">.66</td>
    <td class="tg-0lax">.22</td>
    <td class="tg-0lax">.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">RoBERTa_PAIR</td>
    <td class="tg-0lax">.89</td>
    <td class="tg-0lax"><b>.83</b></td>
    <td class="tg-0lax"><b>.86</b></td>
    <td class="tg-0lax">.91</td>
    <td class="tg-0lax">.97</td>
    <td class="tg-0lax">.94</td>
    <td class="tg-0lax">.89</td>
    <td class="tg-0lax"><b>.81</b></td>
    <td class="tg-0lax"><b>.85</b></td>
     <tr style="border-bottom:2px solid black">
  </tr>
</tbody>
</table>


--

## Results - Results by pattern and POS

<style>
  .tg-0lax:nth-child(4), .tg-0lax:nth-child(7) {
    border-right: 1px solid #000; /* This adds a solid black border */
  }
</style>
</table> <table class="eval">
  <caption style="caption-side:bottom">Performance of RoBERTa_PAIR on the augmented data, split up by pattern and POS type.</caption>
<thead>
  <tr>
   <tr style="border-bottom:2px solid black">
    <th class="tg-0lax"></th>
    <th class="tg-0lax" colspan="3">total</th>
    <th class="tg-0lax" colspan="3">noun</th>
    <th class="tg-0lax" colspan="3">adjective</th>
  </tr>
</thead>
<tbody>
  <tr>
   <tr style="border-bottom:2px solid black">
    <td class="tg-0lax">syntax</td>
    <td class="tg-0lax">precision</td>
    <td class="tg-0lax">recall</td>
    <td class="tg-0lax">F<sub>1</sub></td>
    <td class="tg-0lax">precision</td>
    <td class="tg-0lax">recall</td>
    <td class="tg-0lax">F<sub>1</sub></td>
    <td class="tg-0lax">precision</td>
    <td class="tg-0lax">recall</td>
    <td class="tg-0lax">F<sub>1</sub></td>
  </tr>
  <tr>
    <td class="tg-0lax">—</td>
    <td class="tg-0lax"><b>.91</b></td>
    <td class="tg-0lax"><b>.93</b></td>
    <td class="tg-0lax"><b>.92</b></td>
    <td class="tg-0lax"><b>.90</b></td>
    <td class="tg-0lax"><b>.93</b></td>
    <td class="tg-0lax"><b>.92</b></td>
    <td class="tg-0lax"><b>.91</b></td>
    <td class="tg-0lax"><b>.93</b></td>
    <td class="tg-0lax"><b>.92</b></td>
  </tr>
  <tr>
    <td class="tg-0lax">answer to</td>
    <td class="tg-0lax">.85</td>
    <td class="tg-0lax">.62</td>
    <td class="tg-0lax">.72</td>
    <td class="tg-0lax">.88</td>
    <td class="tg-0lax">.72</td>
    <td class="tg-0lax">.79</td>
    <td class="tg-0lax">.82</td>
    <td class="tg-0lax">.51</td>
    <td class="tg-0lax">.63</td>
  </tr>
  <tr>
    <td class="tg-0lax">version of</td>
    <td class="tg-0lax">.89</td>
    <td class="tg-0lax">.83</td>
    <td class="tg-0lax">.86</td>
    <td class="tg-0lax"><b>.90</b></td>
    <td class="tg-0lax">.90</td>
    <td class="tg-0lax">.90</td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.77</td>
    <td class="tg-0lax">.81</td>
  </tr>
  <tr>
    <td class="tg-0lax">equivalent of</td>
    <td class="tg-0lax">.89</td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.88</td>
    <td class="tg-0lax"><b>.90</b></td>
    <td class="tg-0lax">.91</td>
    <td class="tg-0lax">.91</td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.82</td>
    <td class="tg-0lax">.85</td>
     <tr style="border-bottom:2px solid black">
  </tr>
  <tr>
    <td class="tg-0lax">total</td>
    <td class="tg-0lax">.89</td>
    <td class="tg-0lax">.81</td>
    <td class="tg-0lax">.85</td>
    <td class="tg-0lax">.90</td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.88</td>
    <td class="tg-0lax">.87</td>
    <td class="tg-0lax">.76</td>
    <td class="tg-0lax">.81</td>
     <tr style="border-bottom:2px solid black">
  </tr>
</tbody>
</table>

<br />

---

# Bibliography 

<br />

<span style="font-size: .9rem">

- Alan Akbik, Tanja Bergmann, Duncan Blythe, Kashif Rasul, Stefan
Schweter, and Roland Vollgraf. 2019.  FLAIR: An easy-to-use framework
for state-of-the-art NLP. In Proceedings of the 2019 Conference of the
North American Chapter of the Association for Computational
Linguistics (Demonstrations), pages 54–59, Minneapolis,
Minnesota. Association for Computational Linguistics.

- Minjin Choi, Sunkyung Lee, Eunseong Choi, Heesoo Park, Junhyuk Lee,
Dongwon Lee, and Jongwuk Lee. 2021. MelBERT: Metaphor detection via
contextualized late interaction using metaphorical identification
theories. In Proceedings of the 2021 Conference of the North American
Chapter of the Association for Computational Linguistics: Human
Language Technologies, pages 1763–1773, Online. Association for
Computational Linguistics.

- Haonan Li, Maria Vasardani, Martin Tomko, and Timothy
Baldwin. 2020. Target word masking for location metonymy
resolution. In Proceedings of the 28th International Conference on
Computational Linguistics, pages 3696–3707, Barcelona, Spain (Online).
International Committee on Computational Linguistics.

- Michel Schwab, Robert Jäschke, and Frank Fischer.2022. ”The Rodney
Dangerfield of Stylistic Devices”: End-to-end detection and extraction
of Vossian Antonomasia using neural networks. Frontiers in
Artificial Intelligence.  </span>

<!-- THIS IS AN EXAMPLE TO SPLIT SLIDE INTO TWO COLUMNS
--
## 
<div id="left">
### Machine Translation and Alignment
</div>
<div id="right">
### Zero-Shot
</div> -->


</script>