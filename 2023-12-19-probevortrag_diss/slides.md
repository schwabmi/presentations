## Detection, Extraction and Analysis of Vossian Antonomasia in Large Text Corpora Using Machine Learning


Michel Schwab <a href="https://orcid.org/0000-0001-5569-6568"><img height=20 src="https://upload.wikimedia.org/wikipedia/commons/0/06/ORCID_iD.svg"/></a> 

Humboldt-Universität zu Berlin <br />

<br><br>

Probevortrag Promotion &nbsp;·&nbsp; Berlin &nbsp; 🇩🇪 &nbsp;·&nbsp; Di, 19.12.2023
<!-- .element: style="font-size:0.8em;" -->

---

## Inhalt

<br>


1. [Definition und Task](#/2)
2. [Motivation und Herausforderungen](#/3)
3. [Methoden und Ergebnisse](#/4)
4. [Zusammenfassung und Haupterkenntnisse](#/6)

---


## Definition und Task

--

## Vossianische Antonomasie (Vossanto)

<br />


- eine Trope, eng verwandt mit Metapher und Metonymie
- Ein Spezialfall oder Gegenstück zur klassischen Antonomasie, z.b. "Big Apple" für NYC
- zuerst explizit beschrieben ca. 1600 von Gerardus Vossius
- Zuweisung von bestimmten Eigenschaften an eine Entität durch Nennung einer anderen benannten Entität, die typischerweise für die betreffenden Eigenschaften bekannt ist
- besteht typischerweise aus **Target**, **Source** und **Modifier** (cf. Bergien 2013)


--

## »the Michael Jordan of football«

<br>

![VA Example](images/example.png)
<!-- .element width="450px" -->


<small>
image sources: <a href="https://commons.wikimedia.org/wiki">Wikimedia Commons</a></small>

--


## Beispiel

<br />

![Jim Koch, the Steve Jobs of beer](images/the-steve-jobs-of-beer_theatlantic-com.jpg)<!-- .element height="400px" --> 

<br />

= Jim Koch (Source: [theatlantic.com](https://www.theatlantic.com/magazine/archive/2014/11/the-steve-jobs-of-beer/380790/), 2014)


--

<h2>Task</h2>

<br />

<h3>Erkennung</h3>
<div class="fragment" data-fragment-index="1">Identifikation von Sätzen, die eine VA enthält.</div>

<br />

<h3>Extraktion</h3>
<div class="fragment" data-fragment-index="2">Identifikation der drei Komponenten.</div>

<br />

<h3>Analyse</h3>
<div class="fragment" data-fragment-index="3">Tieferes Verständnis mit Hilfe explorativer Methoden.</div>

<!-- Bilder in rechte Spalte, zum dazugehörigen Task -->

---

## Herausforderungen und Motivation

<br />

--


<h2>Herausforderungen zum Verständnis von VA</h2>

<br />

* Kulturelles und historisches Wissen (the Babe Ruth of golf)
* Zeitliche Veränderungen (the Donald Trump of ...)
* Kontext (Arnold Schwarzenegger of our times)


<!-- <h3> Kulturelles und historisches Wissen</h3>
<div class="fragment" data-fragment-index="1">the Lionel Messi of golf (Europe) ---- the Babe Ruth of golf (America)</div>

<br />

<h3>Zeitliche Veränderungen</h3>
<div class="fragment" data-fragment-index="2"> Donald Trump of the horse show world (1992, Geschäftsmann) ----- Donald Trump of the Tropics (2019, Populist)</div>

<br />

<h3>Kontext</h3>
<div class="fragment" data-fragment-index="3">
Arnold Schwarzenegger of our time (Bodybuilder, Schauspieler, Politiker, American Dream)</div>
-->

--

<h2>Herausforderungen bei der automatischen Identifikation von VA</h2>

<br />


* Semantische Mehrdeutigkeit (the Obama of 2020)
* Syntaktische Vielfalt
* Datenknappheit

<!--
<h3>Semantische Mehrdeutigkeit</h3>
<div class="fragment" data-fragment-index="1">
<ul><li>the ENTITY of PHRASE (the Madonna of [Port Lligat|Japan], the Obama of 2020).</li>
</ul>
</div>

<br />

<h3>Syntaktische Vielfalt</h3>
<div class="fragment" data-fragment-index="2">
<ul>
<li> [the/a/an] SOURCE [of/for/among] MODIFIER </li>
<li> [[the/a/an] MODIFIER/MODIFIER's] [ /answer to/equivalent of/version of] SOURCE</li></ul>

</div>

<br />

<h3>Daten</h3>
<div class="fragment" data-fragment-index="3">
<ul><li>keine annotierten Datensätze </li>
<li> Trainingsdaten werden für ML Modelle benötigt </li>
<li> Bewertung von Modellen schwierig (insb. recall)</li></ul>
</div>
-->		

--


## Motivation

<br />

<h3>Forschungslücke</h3>
<div class="fragment" data-fragment-index="1">
Vergleichsweise wenig erforscht gegenüber anderen rhetorischen Mitteln wie Metapher und Metonymie.</div>

<br>

<h3>Geisteswissenschaften</h3>
<div class="fragment" data-fragment-index="2">
Interdisziplinarität in Geisteswissenschaften: Linguistische, kognitive, kulturelle und historische Elemente.<br>
</div>
<br>

<h3>Natural Language Processing</h3>
<div class="fragment" data-fragment-index="3">

<ul>
<li> Entwicklung neuer Datensätze zur Evaluierung verschiedener NLP Tasks (QA)</li>
<li>Coreference Resolution: Referenz von VA phrase zum Target</li> 
<li>Geografische Analyse: the Paris of the East</li> <!-- geographical parsing -->
<li>Sentimentanalyse: Verständnis von Stimmungen</li> <!--für Sätze, aber auch für genutzte Entitäten -->
<li>Kreative Sprachgenerierung: Texten "aufpeppen"</li>
</ul>
</div>

--


## Ziel der Disseration

<br />

- <strong>Forschungslücke schließen</strong>: Automatisierte Identifikation von VA.<br>
- <strong>Grundlage für weiterführende Forschung</strong>: Ermöglichung umfassenderer Analysen des Phänomens in größeren Maßstäben.
</div>


---

## Übersicht 

![Paper connections](images/paper_all.png)<!-- .element width="50%" -->



---


### "A Buster Keaton of Linguistics": First Automated Approaches for the Extraction of Vossian Antonomasia.

<br />

![Paper connections](images/paper_1.png)<!-- .element width="50%" -->


--

## Methoden

<br>


<section>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 24%; background-color: lightblue; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="1">
<h3>Semi-Auto</h3>
            <p><ol>
<li>NYT Corpus (~60Mio Sätze)</li>
<li>Regex: a/an/the [up to 5 words] for/of/among</li>
	    <li>Wikidata "human" Liste </li>
	    <li>Streichliste</li>
	    </ol></p>
<p><b>Datensatz</b>: Labeln der Daten (6,072; 3,023 VA)</p>
        </div>
</div>
        <div style="width: 24%; background-color: lightgreen; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="2">
<h3>Wikidata</h3>
            <p><ul><li>Ersetzt Schritt 4 durch neues Maß: # WD Sitelinks </li>
	    <li>House (Botaniker) vs. House (Gebäude)</li>

</ul></p>
        </div>        </div>
        <div style="width: 24%; background-color: lightcoral; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="3">
<h3>NER</h3>
            <p>Ersetzt Schritt 3 und 4 durch NER Tagger (spaCy)</p>
</div>        </div>
        <div style="width: 24%; background-color: lightyellow; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="4">
<h3>BLSTM</h3>
            <p><ul><li>Nutzung des gelabelten Datensatzes</li>
	    <li>GloVe + bidirectional LSTM + Linearer Layer</li>
	    <li>binäre Klassifikation</li></ul></p>
        </div>        </div>
    </div>

<div style="display: flex; justify-content: space-around;">
        <div style="width: 24%; background-color: lightblue; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">

</div>
        <div style="width: 24%; background-color: lightgreen; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="5">
F<sub>1</sub>: 0.78
        </div>        </div>
        <div style="width: 24%; background-color: lightcoral; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="5">
F<sub>1</sub>: 0.76
</div>        </div>
        <div style="width: 24%; background-color: lightyellow; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="5">
<b>F<sub>1</sub>: 0.86</b>
        </div>        </div>
    </div>

</section>



---

### "The Rodney Dangerfield of Stylistic Devices": End-to-End Detection and Extraction of Vossian Antonomasia Using Neural Networks.

<br />

![Paper connections](images/paper_2.png)<!-- .element width="50%" -->



--

### Methoden - Erkennung

<br>

<div style="text-align: left; margin-bottom: 0px;">
    <img src="images/blstm-att.png" style="width: 40%; margin-right: 10%;" />
    <img src="images/bert-clf.png" style="width: 40%;" />


</div>
    <div style="display: flex; justify-content: space-around;">
     <div style="width: 40%;: 40%; margin-right: 10%;">
Overview: BLSTM-ATT     </div>
     <div style="width: 40%;: 40%; margin-right: 10%;">
Overview: BERT (Classification) </div>
</div>


--

### Methoden - Extraktion

<br>

<div style="text-align: left; margin-bottom: 0px;">
    <img src="images/blstm-crf.png" style="width: 40%; margin-right: 10%;" />
    <img src="images/bert-seq.png" style="width: 40%;" />


</div>
    <div style="display: flex; justify-content: space-around;">
     <div style="width: 40%;: 40%; margin-right: 10%;">
Overview: BLSTM-CRF     </div>
     <div style="width: 40%;: 40%; margin-right: 10%;">
Overview: BERT (Sequence Tagging)  </div>
</div>



--

## Evaluation

<br>

![Paper connections](images/overview_evalution.png)<!-- .element width="80%" -->


--

<!-- ## Evaluation - aVA

<br>

![Paper connections](images/frontiers_ava.png)<!-- .element width="80%" -->

<!--
## Evaluation - eVA

<br>

![Paper connections](images/frontiers_eva.png)<!-- .element width="80%" -->



## Evaluation - Robustheit

Datensatz: Signal Media Dataset

<br>

<h3>Klassifikation (A): BERT-CLF</h3>
<div class="fragment" data-fragment-index="1">
<ul><li> Normalisierter Vorhersagewert</li></ul>
</div>

<br />


<h3>Sequence Tagging (B): BERT-SEQ</h3>

<div class="fragment" data-fragment-index="2">
<ul><li> Vorhersagemarge: $\delta_w  = |P (t'\|\ w)-P(t'' \|\ w)|$</li>
<li> Vorhersagewert: $\mu_s = \frac{1}{n} \sum_{i=1}^{n}  \delta_{w_i}$</li></ul>
</div>

![Paper connections](images/frontiers_sample_selection.png)<!-- .element width="80%" -->


--

<!--## Results - Robustheit: Ergebnisse

<br>

Datensatz: Signal Media Dataset



![Paper connections](images/frontiers_robustness.png)<!-- .element width="80%" -->




## Evaluation - Generalization

<br>

Datensatz: NYT Corpus

Modell: BERT-SEQ

1. Extraktion neuer Entitätstypen von Sourceentitäten
2. Extraktion neuer syntaktischer Variationen

![Paper connections](images/frontiers_generalization_examples.png)<!-- .element width="70%" -->

<!--![Paper connections](images/frontiers_generalization_results.png)<!-- .element width="50%" -->


---

### "Der Frank Sinatra der Wettervorhersage": Cross-Lingual Vossian Antonomasia Extraction. 

<br />

![Paper connections](images/paper_3.png)<!-- .element width="50%" -->


--

### Daten	

<section>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="1">            <h3>Training</h3>
            <p>
Annotierte Daten aus Schwab et al. 2022
	    </p>

</div>        </div>
       <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="2"><h3>Test: UMBL</h3>
<a href="https://umblaetterer.de/datenzentrum/vossianische-antonomasien.html">manuell gesammelte Liste von Frank Fischer</a>
        </div>        </div>
       <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="3"><h3>Test: ZEIT</h3>
Daten von Jäschke et al. 2017: regelbasierter Ansatz
        </div>        </div>
       <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="4"><h3>Test: negativ</h3>
   <p><ol><li>Syntaktisch ähnliche Phrasen (Wiki)</li>
	    <li>Eigennamen aus Trainingsdaten (taz)</li>
   	    <li>zufällige Sätze (taz)</li>
</ol></p>
        </div>        </div>
	</div>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="1">
6,072 (3,023 VA Sätze)
</div>        </div>
       <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="2">
362 VA Sätze
        </div>        </div>
       <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="3">
224 VA Sätze
        </div>        </div>
       <div style="width: 24%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="4">
3,000 Sätze pro Sample
        </div>        </div>
	</div>
</section>




--

### Methoden und Ergebnisse

<section>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
            <h3>0shot</h3>
            <p><ul>
	    <li>multilinguales Modell </li>
	    <li>XLM-RoBERTa (Conneau et al., 2020)</li>
	    </ul>
	    </p>

</div>
       <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>de2en</h3>
   <p><ul><li>Übersetzen der Testdaten FAIRSEQ (Ott et al., 2019)</li>
	    <li>Tagausrichtung: SimAlign (Jalili Sabet et al., 2020)</li>
	    <li>mBERT (Devlin et al., 2018)</li>
</ul></p>
        </div>
       <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>en2de</h3>
   <p><ul><li>Übersetzen der Trainingsdaten FAIRSEQ</li>
	    <li> Tagausrichtung SimAlign</li>
	    <li>DBMDZ BERT</li>
</ul></p>
        </div>
     	</div>
</section>

&rarr; en2de funktioniert am besten (F<sub>1</sub>: 0.86)

&rarr; Robustness study mit taz Artikeln (F<sub>1</sub>: 0.70)



---

### "Japan's Answer to Mozart": Automatic Detection of Generalized Patterns of Vossian Antonomasia

<br />

![Paper connections](images/paper_4.png)<!-- .element width="50%" -->


--

## Daten

NER für Kandidatengenerierung
<br>


<section>

<div style="display: flex; justify-content: space-around;">
<div style="width: 48%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="1">
<h3>Trainingsdaten</h3>
            <p><ul>
	    <li>Annotierte Daten aus Schwab et al. 2022</li>
	    </ul>
	    </p>

</div></div>
       <div style="width: 48%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="2">
<h3>Testdaten</h3>
   <p><ul><li>Data augmentation</li>
	    <li> the <span style="color:red">SOURCE</span> of <span style="color:blue">MODIFIER</span></li>
	    <li> <span style="color:blue">[the MOD_adj|MOD_noun's]</span> [answer to| version of| equivalent of]? <span style="color:red">SOURCE</span></li>
	    <li>244 VA in Datensatz</li>
</ul></p>
        </div>        </div>
    </div>

<div style="display: flex; justify-content: space-around;">
        <div style="width: 48%; background-color: lightblue; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="3">
<p><b>&rarr; 16,877 Tupel (2,868 positiv)</b></p>
</div>        </div>
        <div style="width: 48%; background-color: lightblue; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="4">
<p><b>&rarr; 8,480 Tupel (2,196 positiv)</b></p>
        </div>        </div>
    </div>
</section>

--

## Methoden

<br>

<section>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>BERT-SEQ</h3>
            <p>
	    Adaption aus Schwab et al. 2022</p>
</div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>BERT-MASK</h3>
   <p><ul><li>Metonymie-Theorie: Kontext ist wichtiger als Wort selbst</li>
   <li>Adaption von Li et al., 2020</li>
</ul></p>
</div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
            <h3>RoBERTa-MIP</h3>
            <p><ul><li>Metapher-Theorie: wörtliche und kontextuelle Bedeutung eines Wortes sind unterschiedlich</li>
	    <li>Adaption von Choi et al. 2022</li>
</ul></p>
        </div>
</div>
<div style="display: flex; justify-content: space-around;">
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
            <h3>RoBERTa-SPV</h3>
	    <p><ul><li>Metapher-Theorie: Wort erscheint in "ungewöhnlichen" Kontext</li>
	    <li>Adaption von Choi et al. 2022</li>
</ul></p>
    </div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>RoBERTa-CLF</h3>
   <p>Einführung spezieller Tokens: [START_SRC], [END_SRC]</p>
        </div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>RoBERTa-PAIR</h3>
   <p>Satzpaare: [Source, Satz]</p>
</div>
</div>
</section>


--

## Evaluation - Trainingsdatensatz

<br>


![Paper connections](images/icnlsp23_results.png)<!-- .element width="80%" -->

--

## Evaluation - Testdatensatz

<br>

![Paper connections](images/icnlsp23_aug.png)<!-- .element width="80%" -->


--

## Evaluation - POS und Syntax

<br>

![Paper connections](images/icnlsp23_pos.png)<!-- .element width="80%" -->




---


### »Who is the Madonna of Italian-American Literature?« - Extracting and Analyzing Target Entities of Vossian Antonomasia

<br />

![Paper connections](images/paper_5.png)<!-- .element width="50%" -->

--

### Methoden und Ergebnisse

Datensatz: annotierter Datensatz aus Schwab et al., 2022.

<section>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="1">
<h3>COREF</h3>
            <p><ul>
	    <li>Coreference Resolution</li>
	    <li>Longformer (Toshniwal et al. (2021))</li>
	    </ul>
	    </p>

</div></div>
       <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="2">
<h3>QA</h3>
   <p><ul><li>Question-Answering</li>
   	    <li>ELECTRA (Clark et al. 2020), SQUAD2.0</li>
	    <li>Umformulierung: Who is the SOURCE of MODIFIER?</li>
</ul></p>
        </div></div>
       <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="3">
<h3>Hybrid</h3>
   <p><ul><li>QA + COREF</li>
</ul></p>
        </div>
     	</div></div>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="4">
<p><ul><li>F<sub>1</sub>: 0.29 (0.56)</li>
<li>EM: 0.25 (0.47)</li></ul></p>
        </div>
</div>
       <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="4">
<p><ul><li>F<sub>1</sub>: 0.64 (0.72)</li>
<li>EM: 0.52 (0.61)</li></ul></p>
        </div>
        </div>
       <div style="width: 33%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="4">
<p><ul><li><b>F<sub>1</sub>: 0.78</b></li>
<li><b>EM: 0.71</b></li></ul></p>
        </div>
        </div>
     	</div>
 <div style="display: flex; justify-content: space-around;">
        <div style="width: 98%; background-color: lightblue; padding: 5px; margin: 5px; text-align: center; border-radius: 10px;">
<div class="fragment" data-fragment-index="5"><h3>Entity Linking</h3></div>
</div>
</div>
 <div style="display: flex; justify-content: space-around;">
        <div style="width: 33%; background-color: lightblue; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="5">
<p>MP: 0.21 (0.46)</p>
     	</div>
</div>
       <div style="width: 33%; background-color: lightblue; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="5">
<p>MP: 0.55 (0.62)</p>
     	</div>
        </div>
       <div style="width: 33%; background-color: lightblue; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<div class="fragment" data-fragment-index="5">
<p><b>MP:0.64</b></p>
        </div>
     	</div>
     	</div>
</section>

--

## Analyse

<br>

[Interactive Visualization](https://vossanto.weltliteratur.net/sighum2023/graph.html)

---

### »Die Greta Garbo der Leichtathletik« - Eine systematische Analyse der Modifier vossianischer Antonomasien mithilfe von Word Embeddings.

<br />

![Paper connections](images/paper_6.png)<!-- .element width="50%" -->

--

### Vorgehen:

<br />

<section>

 <div style="display: flex; justify-content: space-around;">
        <div style="width: 98%; background-color: lightblue; padding: 5px; margin: 5px; text-align: center; border-radius: 10px;">
<div class="fragment" data-fragment-index="1"><h3>Repräsentation: Sentence-BERT</h3>
</div></div></div>
 <div style="display: flex; justify-content: space-around;">
        <div style="width: 98%; background-color: lightblue; padding: 5px; margin: 5px; text-align: center; border-radius: 10px;">
<div class="fragment" data-fragment-index="2"><h3>Clustering: k-means</h3>
</div></div></div>
 <div style="display: flex; justify-content: space-around;">
        <div style="width: 98%; background-color: lightblue; padding: 5px; margin: 5px; text-align: center; border-radius: 10px;">
<div class="fragment" data-fragment-index="3"><h3>lexikalische Themenmodellierung: WordNet Domains</h3>
</div></div></div>
 <div style="display: flex; justify-content: space-around;">
        <div style="width: 98%; background-color: lightblue; padding: 5px; margin: 5px; text-align: center; border-radius: 10px;">
<div class="fragment" data-fragment-index="4"><h3>Dimensionsreduktion: PCA, t-SNE, IVIS, UMAP</h3>
</div></div></div>
<div style="display: flex; justify-content: space-around;">
        <div style="width: 98%; background-color: lightblue; padding: 5px; margin: 5px; text-align: center; border-radius: 10px;">
<div class="fragment" data-fragment-index="5"><h3><a href="https://vossanto.weltliteratur.net/dhd2023/modifier.html">Interaktive Visualisierung</a></h3>
</div></div></div>
</section>


---

## Zusammenfassung und Haupterkenntnisse

<br /> 

### Erkennung
<div class="fragment" data-fragment-index="1">
<ol><li> Regelbasierte Ansätze &rarr; annotierter Datensatz</li>
<li> Robuste Methoden zur Erkennung von VA</li>
<li> Ausweitung auf neue syntaktische Variationen</li></ol>
</div>

<br />

### Extraktion
<div class="fragment" data-fragment-index="2">
<ol><li> Modellierung als Sequence Tagging Task</li>
<li> Robuste Methoden zur Extraktion aller Komponenten</li>
<li> Sprachübergreifende Modelle</li>
<li> Extraktion des Targets im Artikel</li></ol>
</div>

<br />

### Analyse
<div class="fragment" data-fragment-index="3">
<ol><li> Verbessertes Verständnis von VA durch annotierte Daten</li>
<li> Explorative Analyse von Source-Target Verbindungen</li>
<li> Systematische Analyse des Modifiers</li></ol>
</div>