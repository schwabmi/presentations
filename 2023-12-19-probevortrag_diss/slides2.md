
<section></section>

--

## Methoden

<br>



---

## Data

<br>


<section>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 48%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
            <h3>Trainingsdaten</h3>
            <p><ul>
	    <li>Annotierte Daten aus Schwab et al. 2022</li>
	    </ul>
	    </p>
</div>
       <div style="width: 48%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>Testdaten</h3>
   <p><ul><li>Data augmentation: Erzeugung neuer syntaktischer Variationen, die ihre Semantik beibhalten</li>
	    <li> the <span style="color:red">SOURCE</span> of <span style="color:blue">MODIFIER</span></li>
	    <li> &rarr; <span style="color:blue">[the MOD_adj|MOD_noun's]</span> [answer to| version of| equivalent of]? <span style="color:red">SOURCE</span></li>
    	    <li>Funktioniert nur mit geographischen Orten (WP Listen)</li>
	    <li>244 VA in Datensatz</li>
</ul></p>
        </div>
    </div>
<div style="display: flex; justify-content: space-around;">
        <div style="width: 48%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<p><b>&rarr; 16,877 Tupel (2,868 positiv)</b></p>
</div>
        <div style="width: 48%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
	   <p><b>&rarr; 8,480 Tupel (2,196 positiv)</b></p>
        </div>
    </div>
</section>




--


## Methods

<br>

<section>
    <div style="display: flex; justify-content: space-around;">
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
            <h3>BERT-SEQ</h3>
            <p><ul>
	    <li>Adaption aus Schwab et al. 2022</li>
	    <li>Fokus: Nur source tagging</li>
	    </ul></p>
</div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>BERT-MASK</h3>
   <p><ul><li>Metonymie-Theorie: Kontext ist wichtiger als Wort selbst</li>
	    <li>Adaption von auf source</li>
	    <li>RoBERTa</li>
    	    <li></li>
</ul></p>
</div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
            <h3>RoBERTa-MIP</h3>
            <p><ul><li>Metapher-Theorie: wörtliche und kontextuelle Bedeutung eines Wortes sind unterschiedlich</li>
	    <li>Adaption von Choi et al. 2022  auf source</li>
	    <li>RoBERTa</li>
    	    <li></li>
</ul></p>
        </div>
</div>
<div style="display: flex; justify-content: space-around;">
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
            <h3>RoBERTa-SPV</h3>
	    <p><ul><li>Metapher-Theorie: Wort erscheint in "ungewöhnlichen" Kontext</li>
	    <li>Adaption von Choi et al. 2022  auf source</li>
	    <li>RoBERTa</li>
    	    <li></li>
</ul></p>
    </div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>RoBERTa-CLF</h3>
   <p><ul>
	    <li>Einführung spezieller Tokens: [START_SRC], [END_SRC]</li>
	    <li>RoBERTa</li>
    	    <li></li>
</ul></p>
        </div>
        <div style="width: 32%; background-color: lightgrey; padding: 5px; margin: 5px; text-align: left; border-radius: 10px;">
<h3>RoBERTa-PAIR</h3>
   <p><ul><li>Sentence-Pair classification</li>
	    <li>1. Satz: source</li>
	    <li>2. Satz: vollständiger Satz</li>
    	    <li>RoBERTa</li>
</ul></p>
</div>
</div>
</section>


--



### »Die Greta Garbo der Leichtathletik« - Eine systematische Analyse der Modifier vossianischer Antonomasien mithilfe von Word Embeddings. 

<br />

![Paper connections](images/paper_4.png)<!-- .element width="80%" -->


--


### »Who is the Madonna of Italian-American Literature?« - Extracting and Analyzing Target Entities of Vossian Antonomasia

<br />

![Paper connections](images/paper_5.png)<!-- .element width="80%" -->


--

### »Who is the Madonna of Italian-American Literature?« - Extracting and Analyzing Target Entities of Vossian Antonomasia

<br />

- Dataset creation:
   - Annotating target entity in corresponding article
- Methods:
    - Coreference Resolution (reference chain)
    - Question-Answering (transforming VA into Question)
    - Hybrid model (Coref + QA)

- [interactive visualization](https://vossanto.weltliteratur.net/sighum2023/graph.html)


--

### »Die Greta Garbo der Leichtathletik« - Eine systematische Analyse der Modifier vossianischer Antonomasien mithilfe von Word Embeddings.

<br />

- Methods:
   1. Sentence-BERT (efficient Computing of semantic similarity)
   2. Clustering (k-means)
   3. Topic assignment for clusters (WordNet Domains)
   4. [interactive Visualization (Reduction algorithms (PCA, t-SNE, etc.))](https://vossanto.weltliteratur.net/dhd2023/modifier.html)


---

## Findings
 <br /> 

- create annotated VA dataset
- first fully automated approaches to detect VA
- binary classification and sequence tagging
- robustness studies against unseen data
- cross-lingual VA detection
- target detection
- systematic analysis of the modifier
- data augmentation to create a diverse dataset
- methods for unseen syntactic varations
