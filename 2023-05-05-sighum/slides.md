### »Who is the Madonna of Italian-American Literature?« - Extracting and Analyzing Target Entities of Vossian Antonomasia

<!-- ![intro pic](images/greta-garbo-middle-distance-runner_dall-e.jpg)<!-- .element height="200px;" --> 

Michel Schwab ¹ <a href="https://orcid.org/0000-0001-5569-6568"><img height=20 src="https://upload.wikimedia.org/wikipedia/commons/0/06/ORCID_iD.svg"/></a> · Robert Jäschke ¹,³ <a href="https://orcid.org/0000-0003-3271-9653"><img height=20 src="https://upload.wikimedia.org/wikipedia/commons/0/06/ORCID_iD.svg"/></a><!-- .element: style="font-size:0.8em;" --> · Frank Fischer ² <a href="https://orcid.org/0000-0003-2419-6629"><img height=20 src="https://upload.wikimedia.org/wikipedia/commons/0/06/ORCID_iD.svg"/></a><!-- .element: style="font-size:0.8em;" -->

1 · Humboldt-Universität zu Berlin <br />
2 · Freie Universität Berlin<!-- .element: style="font-size:0.6em;" --> <br />
3 · L3S Research Center Hannover<!-- .element: style="font-size:0.6em;" -->

<br />URL of this presentation: <!-- .element: style="font-size:0.6em;" --> **[todo](todo)**  <!-- .element: style="font-size:0.6em;" -->

[SIGHUM2023](https://sighum.wordpress.com/events/latech-clfl-2023/) &nbsp;·&nbsp; Dubrovnik &nbsp;🇭🇷 &nbsp;·&nbsp; Fr, 05. Mai 2023
<!-- .element: style="font-size:0.8em;" -->

---

## Content

<br/>

1. [Definition and Examples](#/1)
2. [Motivation and Difficulty](#/2) 
3. [Task](#/3)
4. [Data](#/4)
5. [Methods](#/5)
6. [Evaluation and Analysis](#/6)

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
- first described around 1600 from Gerardus Vossius
- consists of Target, Source, Modifier (vgl. Bergien 2013)


--

### »the Michael Jordan of football«

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

---

# Task

--

## Vossanto Research

</br>

<div class="timeline">
  <div class="container left">
    <div class="date"></div>
    <i class="icon fa fa-home"></i>
    <div class="content">
      <h2>DHd 2017</h2>
      <p>
        Jäschke et al.
      </p>
    </div>
  </div>
  <div class="container right">
    <div class="date"></div>
    <i class="icon fa fa-gift"></i>
    <div class="content">
      <h2>DSH 2019</h2>
      <p>
       Fischer and Jäschke
      </p>
    </div>
  </div>
  <div class="container left">
    <div class="date"></div>
    <i class="icon fa fa-user"></i>
    <div class="content">
      <h2>EMNLP-IJCNLP 2019</h2>
      <p>
        Schwab et al.
      </p>
    </div>
  </div>
  <div class="container right">
    <div class="date"></div>
    <i class="icon fa fa-running"></i>
    <div class="content">
      <h2>Frontiers in Artificial Intelligence 2022</h2>
      <p>
      Schwab et al.
      </p>
    </div>
  </div>
  <div class="container left">
    <div class="date"></div>
    <i class="icon fa fa-cog"></i>
    <div class="content">
      <h2>ICNLSP 2022</h2>
      <p>
        Schwab et al.
      </p>
    </div>
  </div>
  <div class="container right">
    <div class="date"></div>
    <i class="icon fa fa-certificate"></i>
    <div class="content">
      <h2>DHd 2023</h2>
      <p>
      Schwab and Fischer
      </p>
    </div>
  </div>
  <div class="container left">
    <div class="date"></div>
    <i class="icon fa fa-cog"></i>
    <div class="content">
      <h2>SIGHUM 2023</h2>
      <p>
        Schwab et al.
      </p>
    </div>
  </div>
</div>

--

## Interactive explorable data

</br>

![interaktive Vossanto-Timeline](images/timeline.png)<!-- .element width="70%" -->

https://vossanto.weltliteratur.net/timeline/

--


## Target Extraction and Linking

</br>

- until now: Vossanto detection using sentences as input
- Problem: Target not mentioned/only a reference mentioned
- in this paper: **Extraction and linking of target entity**
- Web-App for Exploration

---

# Data


--


## Vossanto Dataset (Schwab et al. (2019, 2022, 2023))

</br>

<ol>
  <li>
    regular expression: a/an/the [up to 10 words] of/for/among
    <ul style="list-style-type: none;">
      <li>&#8594; candidate sentences </li>
    </ul>
  </li>
  <li>
    Check with Wikidata list consisting of names and aliases having ›instance-of‹ property ›human‹
    <ul style="list-style-type: none;">
      <li>&#8594; Focus on persons </li>
    </ul>
  </li>
  <li>
     Check with manual currated blacklist
    <ul style="list-style-type: none;">
      <li>&#8594; <s>the House of Commons</s> (vgl. <a href="https://www.wikidata.org/wiki/Q3139666">Homer Doliver House</a>)</li>
    </ul>
  </li>
</ol>


<p style="text-align:left;"> <b>Result</b>: 6.095 sentences, <b>3.115</b> include Vossantos </p>


--

## Most frequent targets

</br>

![Target Statistics](images/target_stats.png)<!-- .element width="700px" -->

---

# Methods

--


## Baselines: Coreference Resolution (COREF)


- Model: Longformer \todo(cite)




<br />

1. VA phrase consisting of source and modifier


<p style="font-size: 0.7em; font-style: italic;">It forms the underpinnings for Ms. Barolini's epic saga <span style="color: blue;">Umbertina</span> [. . .]  ''<span style="color: blue;">It</span> is <span style="color: orange;">the Madonna of Italian-American literature</span> in that <span style="color: blue;">it</span> shows the transition from the Italian immigrant to American citizen like no other book of its genre.''</p>
2. Annotated target reference inside the sentence the VA phrase appears 

<p style="font-size: 0.7em; font-style: italic;">It forms the underpinnings for Ms. Barolini's epic saga <span style="color: blue;">Umbertina</span> [. . .]  ''<span style="color: orange;">It</span> is <span style="color: blue;">the Madonna of Italian-American literature</span> in that <span style="color: blue;">it</span> shows the transition from the Italian immigrant to American citizen like no other book of its genre.''</p>


<br />
&rarr; Select first named entity in reference chain

[<span style="color:green">Umbertina</span>, It, the Madonna of Italian-American literature, it]


--

## Question-Answering (QA)

<br>

- Transform VA phrase into QA task:
    - Question: "Who is the Madonna of Italian-American literature?"
    - Context: Article text
- Employ Language Model finetuned on QA (Electra large)
- No need of annotated target reference in sentence
- Independent on the syntax of VA phrases:
    - "the German Madonna" &rarr; Who is the German Madonna?
    - the German [answer to]/[equivalent of]/[version of] Madonna &rarr; Who is the German answer to Madonna?
    - ...
- Preliminary Analysis showed that usually, the target name appears before the VA phrase 
&rarr; cut context after VA phrase appears

--

## Hybrid Approach I
####  Question Answering


<br>

- Pre-Analysis of QA output: courtesy title + last name instead of full name (e.g. Ms. Valdes instead of Zoe Valdes)

<p style="font-size: 0.7em; font-style: italic;">''They are always talking about the coarse <span style="color: green">Zoe Valdes</span>, the crude <span style="color: green">Zoe Valdes</span>,'' she explained. ''In that way, the Cuban state can discredit me here.'' .
 [. . .]
Alejandro Armengol, a critic for El Nuevo Herald, a Miami newspaper, dismissed <span style="color: red"> Ms. Valdes</span> last year as ''the Madonna of Cuban literature, with an equal capacity to transform self-assurance and the grotesque into spectacle, to show vulgarity and eroticism stripped of any mystery.''</p>


--

## Hybrid Approach II

#### Coreference Resolution 

<br>

1. Find reference chain that includes the QA output
2. Choose the "best" named entity in the reference chain:

   &rarr; longest named entitiy that shares word with QA output (except courtesy titles)

[<span style="color:green">Zoe Valdes</span>, <span style="color:green">Zoe Valdes</span>, she, me, <span style="color:red">Ms. Valdes</span>, the Madonna of Cuban literature]




--

## Entity Linking


<br>

GENRE (...)


---

# Evaluation and Analysis




--

## Evaluation

<br>

<table style="text-align: center; margin-left: auto; margin-right: auto;">
  <thead>
    <tr>
    <th colspan="1" </th>
      <th colspan="4" style="text-align:center; border-bottom:2px solid black; border-right:0.6em solid #f4f4e7;">Extraction</th>
      <th colspan="1" style="text-align:center; border-bottom:2px solid black; border-left:0.8em solid #f4f4e7;">Linking</th>
    </tr>
    <tr style="border-bottom:2px solid black">
    <th>model</th>
      <th>prec</th>
      <th>rec</th>
      <th>f1</th>
      <th>em</th>
      <th style="text-align:right;">mp</th>
      </tr>
  </thead>
  <tbody>
    <tr>
      <td>LF<sub>p</sub></td>
      <td style="text-align:right;">.29</td> 
      <td style="text-align:right;">.28</td>
      <td style="text-align:right;">.29</td>
      <td style="text-align:right;">.25</td>
      <td style="text-align:right;">.21</td>
    </tr>
    <tr style="border-bottom:1px solid black">
      <td>LF<sub>t</sub></td>
      <td style="text-align:right;">.58</td>
      <td style="text-align:right;">.54</td>
      <td style="text-align:right;">.56</td>
      <td style="text-align:right;">.47</td>
      <td style="text-align:right;">.46</td>
    </tr>
    <tr>
      <td>ELE<sub>c</sub></td>
      <td style="text-align:right;">.66</td>
      <td style="text-align:right;">.62</td>
      <td style="text-align:right;">.64</td>
      <td style="text-align:right;">.52</td>
      <td style="text-align:right;">.55</td>
    </tr>
    <tr>
      <td>ELE<sub>s</sub></td>
      <td style="text-align:right;">.74</td>
      <td style="text-align:right;">.71</td>
      <td style="text-align:right;">.72</td>
      <td style="text-align:right;">.61</td>
      <td style="text-align:right;">.62</td>
    </tr>
     <tr style="border-bottom:2px solid black">
      <td>ELE<sub>s</sub>+LF</td>
      <td style="text-align:right; font-weight:bold">.78</td>
      <td style="text-align:right; font-weight:bold"">.77</td>
      <td style="text-align:right; font-weight:bold"">.78</td>
      <td style="text-align:right; font-weight:bold"">.71</td>
      <td style="text-align:right; font-weight:bold"">.64</td>
    </tr>
  </tbody>
</table>


--

## Analysis

<br>


--

### Thank you!

<br>

[vossanto.weltliteratur.net](https://vossanto.weltliteratur.net/)

<br>

<!-- <small>Paper: <br />doi:[10.5281/zenodo.7715490](https://doi.org/10.5281/zenodo.7715490)</small> -->
 

 