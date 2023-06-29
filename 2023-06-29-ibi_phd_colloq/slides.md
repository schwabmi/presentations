### Automatic Detection, Extraction and Analysis of the stylistic device Vossian Antonomasia


Michel Schwab <a href="https://orcid.org/0000-0001-5569-6568"><img height=20 src="https://upload.wikimedia.org/wikipedia/commons/0/06/ORCID_iD.svg"/></a> 

Humboldt-Universität zu Berlin <br />

<br />URL of this presentation: <!-- .element: style="font-size:0.6em;" --> **[bit.ly/3UvC1JX](https://bit.ly/3UvC1JX)**  

[IBI PHD Colloquium] &nbsp;·&nbsp; Berlin &nbsp; 🇩🇪 &nbsp;·&nbsp; Fri, 30 June 2023
<!-- .element: style="font-size:0.8em;" -->

---

## Content

<br>

1. [Definition and Examples](#/2)
2. [Summary](#/3)
3. [Chapters](#/4)
3. [Findings](#/5)


---

# Definition and Examples

--

## Vossian Antonomasia (Vossanto)

<br />

<!--[portrait of Gerhard Johannes Vossius; source: Wikimedia Commons](images/vossius.jpg)
 .element width="100px" --> 

- a trope, closely related to metaphor and metonymy
- special case of general antonomasia
- attributing a particular property to an entity by naming another named entity, that is typically well-known for the respective property
- first described around 1600 by Gerardus Vossius
- consists of Target, Source, Modifier (cf. Bergien 2013)


--

## »the Michael Jordan of football«

<br>

![VA Example](images/example.png)
<!-- .element width="450px" -->


<small>
image sources: <a href="https://commons.wikimedia.org/wiki">Wikimedia Commons</a></small>

--


## Examples

<br />

![Jim Koch, the Steve Jobs of beer](images/the-steve-jobs-of-beer_theatlantic-com.jpg)<!-- .element height="400px" --> 

<br />

= Jim Koch (Source: [theatlantic.com](https://www.theatlantic.com/magazine/archive/2014/11/the-steve-jobs-of-beer/380790/), 2014)

---

## Summary

--

### PhD Progress

<br />

![PhD Timeline](images/timeline.png)<!-- .element width="80%" -->



---

## Chapters

--

### "A Buster Keaton of Linguistics": First Automated Approaches for the Extraction of Vossian Antonomasia.

<br />

![Paper connections](images/paper_1.png)<!-- .element width="80%" -->


--

### "A Buster Keaton of Linguistics": First Automated Approaches for the Extraction of Vossian Antonomasia.

<br />

1. Semi-automated approach to create a labeled Dataset
    - Labeled Dataset: 3,000 pos. Instances, 3000 neg. Instances
2. First Automated Approach using a "popularity measure"
    - Introduce "popularity measure"

3. Second Automated Approach using Neural Networks
    - Bidirectional Long-Short Term Memory (binary classifier)


--

### "The Rodney Dangerfield of Stylistic Devices": End-to-End Detection and Extraction of Vossian Antonomasia Using Neural Networks.

<br />

![Paper connections](images/paper_2.png)<!-- .element width="80%" -->



--

### "The Rodney Dangerfield of Stylistic Devices": End-to-End Detection and Extraction of Vossian Antonomasia Using Neural Networks.

<br />

1. Binary classification
   - BLSTM combined with Attention Layer
   - fine-tuned BERT

2. Sequence Tagging
   - BLSTM-CRF
   - fine-tuned BERT

3. Robustness Studies


--

### "Der Frank Sinatra der Wettervorhersage": Cross-Lingual Vossian Antonomasia Extraction. 

<br />

![Paper connections](images/paper_3.png)<!-- .element width="80%" -->


--

### "Der Frank Sinatra der Wettervorhersage": Cross-Lingual Vossian Antonomasia Extraction. 

<br />

1. Zero-Shot Cross Lingual Transfer
    - fine-tune Multilingual Language Model (XLM-RoBERTa)

2. Machine Translation and Alignment of Training Data
    - fine-tune mBERT

3. Machine Translation and Alignment of Test Data
    - fine-tune "german BERT"

--

### »Die Greta Garbo der Leichtathletik« - Eine systematische Analyse der Modifier vossianischer Antonomasien mithilfe von Word Embeddings. 

<br />

![Paper connections](images/paper_4.png)<!-- .element width="80%" -->


--

### »Die Greta Garbo der Leichtathletik« - Eine systematische Analyse der Modifier vossianischer Antonomasien mithilfe von Word Embeddings.

<br />




--

### »Who is the Madonna of Italian-American Literature?« - Extracting and Analyzing Target Entities of Vossian Antonomasia

<br />

![Paper connections](images/paper_5.png)<!-- .element width="80%" -->


--

### »Who is the Madonna of Italian-American Literature?« - Extracting and Analyzing Target Entities of Vossian Antonomasia

<br />

1. Coreference Resolution

2. Question-Answering

3. Hybrid Model



--

### EMNLP 2023

<br />

![Paper connections](images/paper_6.png)<!-- .element width="80%" -->


--

### EMNLP 2023

<br />

1. Data Augmentation
    - the Michael Jordan of Germany vs. the German Michael Jordan

2. Focus on Source and model problem for different scenarios



---

## Findings

--

## 

- create annotated VA dataset
- first fully automated approaches to detect VA
- binary classification and sequence tagging
- robustness studies against unseen data
- cross-lingual VA detection
- target detection
- systematic analysis of the modifier
- data augmentation to create a diverse dataset
- methods for unseen syntactic varations
