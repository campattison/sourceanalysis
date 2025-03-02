# 📚 Source Analysis System

<div align="center">
  
  ![Banner](pictures/Bodlein_Library_MS._Arab.d.84_roll332_frame1.jpg)
  
  <h2>Computational Approaches to Philosophical Text Analysis</h2>
  
  <p><em>Bridging ancient wisdom and modern AI</em></p>
  
  <p>
    <a href="#overview">Overview</a> •
    <a href="#pipeline">Pipeline</a> •
    <a href="#inputs">Inputs</a> •
    <a href="#prompts">Prompts</a> •
    <a href="#results">Results</a> •
    <a href="#significance">Significance</a>
  </p>
  
  <br>
  
  <p><em>Arabic manuscript from Bodleian Library (MS. Arab.d.84)</em></p>
</div>

---

<a id="overview"></a>
## 🔍 Overview

<div align="center">
  <table>
    <tr>
      <td align="center" width="33%"><h3>🔍 Discover</h3>Hidden textual connections</td>
      <td align="center" width="33%"><h3>🔄 Compare</h3>Cross-linguistic influences</td>
      <td align="center" width="33%"><h3>📊 Analyze</h3>Evidence-based relationships</td>
    </tr>
  </table>
</div>

<br>

The Source Analysis System is a sophisticated computational pipeline designed to analyze philosophical texts, identify thematic connections, and trace potential influences between ancient works. This system combines natural language processing, machine learning, and classical scholarship to provide evidence-based insights into textual relationships that might otherwise remain hidden.

---

<a id="problem"></a>
## ⚠️ Problem Statement

<table>
  <tr>
    <td width="70%">
      <h3>Challenges in Traditional Analysis</h3>
      <ul>
        <li><strong>Labor-Intensive Process:</strong> Tracing the transmission of ideas across philosophical traditions requires extensive manual effort</li>
        <li><strong>Human Limitations:</strong> Individual scholars can only process a finite amount of text</li>
        <li><strong>Subjective Biases:</strong> Manual analysis is influenced by individual scholar perspectives</li>
        <li><strong>Cross-Linguistic Barriers:</strong> Comparing texts across languages adds significant complexity</li>
      </ul>
      <h3>Our Solution</h3>
      <p>Leverage AI to augment scholarly analysis while maintaining rigorous academic standards</p>
    </td>
    <td width="30%" align="center">
      <img src="pictures/Immanuel_Bekker_-_Imagines_philologorum.jpg" alt="Immanuel Bekker" width="300"/>
      <p><em>Immanuel Bekker (1785-1871)<br>Classical philologist whose work exemplifies traditional source analysis</em></p>
    </td>
  </tr>
</table>

---

<a id="pipeline"></a>
## ⚙️ Three-Stage Pipeline

Our system employs a sophisticated three-stage pipeline that progressively refines the analysis:

<div align="center">
  <table>
    <tr>
      <th width="20%">Stage</th>
      <th width="40%">Focus</th>
      <th width="40%">Output</th>
    </tr>
    <tr>
      <td align="center"><h3>1️⃣</h3><strong>Thematizer</strong></td>
      <td>Individual text analysis</td>
      <td>Thematic profiles</td>
    </tr>
    <tr>
      <td align="center"><h3>2️⃣</h3><strong>Source Analyzer</strong></td>
      <td>Pairwise comparison</td>
      <td>Relationship evidence</td>
    </tr>
    <tr>
      <td align="center"><h3>3️⃣</h3><strong>Deep Analyzer</strong></td>
      <td>In-depth analysis</td>
      <td>Detailed influence assessment</td>
    </tr>
  </table>
</div>

<br>

### <img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/brain.svg" width="20" height="20"> Thematizer

**Purpose:** Initial broad analysis of texts to identify themes, structure, and key concepts

**Process:**
- 📥 Ingests raw text files from input and database directories
- 🧠 Performs deep thematic analysis using Claude AI
- 🔑 Extracts metadata, themes, abstracts, and structural breaks
- 📋 Generates comprehensive thematic profiles for each text

**Output:**
- JSON data with detailed thematic analysis
- Human-readable summary reports
- Foundation for subsequent analysis stages

### <img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/magnifying-glass.svg" width="20" height="20"> Source Analyzer

**Purpose:** Compare texts to identify potential relationships and influences

**Process:**
- 🔄 Takes thematizer results as input
- 🔍 Performs pairwise comparisons between input texts and database texts
- 🔗 Identifies verbal parallels, conceptual parallels, methodological similarities
- 📊 Calculates confidence scores based on multiple factors

**Output:**
- Detailed comparison reports with evidence of relationships
- Confidence scores indicating likelihood of influence
- Recommendations for further research

### <img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/microscope.svg" width="20" height="20"> Deep Analyzer

**Purpose:** Perform in-depth analysis of high-confidence matches

**Process:**
- 🎯 Focuses only on text pairs with high confidence scores (≥0.7)
- 🔬 Analyzes three key dimensions:
  - Transmission patterns (direct textual dependencies, conceptual dependencies)
  - Philosophical development (argument structure, conceptual frameworks)
  - Linguistic transformation (technical terminology, argumentative language)
- 📝 Provides concrete evidence for each observation

**Output:**
- Comprehensive analysis of textual relationships
- Evidence-based assessment of influence patterns
- Detailed reports suitable for scholarly use

---

<a id="inputs"></a>
## 📄 Input Texts

Our system works with philosophical texts in multiple languages and from various traditions. Here are examples of the raw input texts we analyze:

### Ancient Greek Example (Aristotle's Poetics)

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
περὶ ποιητικῆς αὐτῆς τε καὶ τῶν εἰδῶν αὐτῆς, ἥν τινα δύναμιν ἕκαστον ἔχει, 
καὶ πῶς δεῖ συνίστασθαι τοὺς μύθους εἰ μέλλει καλῶς ἕξειν ἡ ποίησις, ἔτι δὲ 
ἐκ πόσων καὶ ποίων ἐστὶ μορίων, ὁμοίως δὲ καὶ περὶ τῶν ἄλλων ὅσα τῆς αὐτῆς 
ἐστι μεθόδου, λέγωμεν ἀρξάμενοι κατὰ φύσιν πρῶτον ἀπὸ τῶν πρώτων.
        </pre>
      </td>
    </tr>
    <tr>
      <td align="center"><em>Original Greek text from Bekker's edition (1831)</em></td>
    </tr>
  </table>
</div>

### Classical Arabic Example (Al-Farabi)

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
وأما الشعر فإنه كلام مخيل مؤلف من أقوال لها إيقاعات متساوية، وهذه الأقوال 
متساوية الأجزاء عند العرب متفقة الأواخر، وعند اليونانيين متساوية في الأزمنة 
متفقة الأوزان، وكل قول منها عند العرب يسمى بيتا، وعند اليونانيين يسمى الواحد 
منها فاصلة، وعند كثير من الأمم يسمى الواحد منها سطرا.
        </pre>
      </td>
    </tr>
    <tr>
      <td align="center"><em>Classical Arabic text from Al-Farabi's "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ"</em></td>
    </tr>
  </table>
</div>

### Text Preparation Process

1. **Digitization**: Texts are digitized from critical editions or existing digital repositories
2. **Cleaning**: Removal of editorial apparatus, normalization of characters
3. **Segmentation**: Division into logical units for analysis
4. **Metadata Tagging**: Addition of bibliographic information and structural markers

<div align="center">
  <img src="pictures/Bekker_1831_page184.jpg" alt="Bekker Edition of Aristotle" width="500"/>
  <p><em>Page from Bekker's edition of Aristotle's works (1831), showing the type of texts analyzed by our system</em></p>
</div>

---

<a id="prompts"></a>
## 🤖 AI Prompts

Our system uses carefully engineered prompts to guide the AI analysis. Here are examples of the prompts used at each stage:

### Thematizer Prompt Example

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
You are a philosophical text analyzer with expertise in ancient and medieval philosophy.
Your task is to analyze the following text and identify its key themes, concepts, and structure.

TEXT:
[Input text is inserted here]

Please provide:
1. A concise summary (3-5 sentences)
2. Main philosophical themes (list 5-7)
3. Key concepts and their definitions as used in this text
4. Logical structure breakdown (major sections and their functions)
5. Philosophical tradition(s) this text appears to belong to
6. Potential influences from earlier philosophical works (if detectable)

Format your analysis as structured JSON with the following keys:
"summary", "themes", "key_concepts", "structure", "tradition", "potential_influences"
        </pre>
      </td>
    </tr>
  </table>
</div>

### Source Analyzer Prompt Example

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
You are a comparative philosophical analyst with expertise in identifying textual relationships.
Your task is to compare two philosophical texts and assess potential influence or relationship.

TEXT A (Potential Source):
[Source text thematic profile is inserted here]

TEXT B (Text Under Analysis):
[Target text thematic profile is inserted here]

Please analyze:
1. Verbal parallels (similar phrasing, terminology, examples)
2. Conceptual parallels (similar ideas, arguments, frameworks)
3. Methodological similarities (approach, structure, reasoning patterns)
4. Assess the likelihood of direct influence (scale 0.0-1.0)
5. Provide specific evidence for your assessment

Format your analysis as structured JSON with the following keys:
"verbal_parallels", "conceptual_parallels", "methodological_similarities", 
"influence_score", "evidence", "confidence_explanation"
        </pre>
      </td>
    </tr>
  </table>
</div>

### Deep Analyzer Prompt Example

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
You are a specialist in philosophical transmission analysis with expertise in cross-cultural 
philosophical influence. Your task is to perform an in-depth analysis of the relationship 
between two texts that have been identified as having a high probability of influence.

TEXT A (Potential Source):
[Source text is inserted here]

TEXT B (Text Under Analysis):
[Target text is inserted here]

PREVIOUS ANALYSIS:
[Source analyzer results are inserted here]

Please provide a detailed analysis of:
1. Transmission patterns:
   - Evidence of direct textual dependencies
   - Evidence of conceptual dependencies
   - Possible transmission pathways

2. Philosophical development:
   - How concepts from Text A are developed or transformed in Text B
   - Innovations or adaptations in Text B
   - Cultural or contextual factors affecting the transformation

3. Linguistic transformation:
   - Technical terminology correspondences
   - Translation or adaptation patterns
   - Argumentative language similarities

Provide specific textual evidence for each observation.
        </pre>
      </td>
    </tr>
  </table>
</div>

---

<a id="results"></a>
## 📊 Results & Case Studies

### Al-Farabi and Aristotle: Poetics Transmission

Our system has been tested on analyzing the relationship between Al-Farabi's "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ" and Aristotle's "Poetics":

<div align="center">
  <table>
    <tr>
      <th width="40%">Comparison</th>
      <th width="20%">Confidence Score</th>
      <th width="40%">Key Findings</th>
    </tr>
    <tr>
      <td align="center">Al-Farabi → Poetics</td>
      <td align="center"><strong>0.85</strong></td>
      <td>Strong thematic and conceptual parallels</td>
    </tr>
    <tr>
      <td align="center">Al-Farabi → Analytica Posteriora</td>
      <td align="center"><strong>0.40</strong></td>
      <td>Moderate methodological similarities</td>
    </tr>
  </table>
</div>

### Thematizer Output Example

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
{
  "summary": "Al-Farabi's text presents a systematic analysis of poetics, 
  defining poetry as imaginative discourse with rhythmic patterns. It 
  compares Arabic and Greek poetic traditions, highlighting differences 
  in metrical systems while identifying universal elements of poetic 
  composition. The text establishes a philosophical framework for 
  understanding poetry as a form of logical discourse with specific 
  effects on the soul.",
  
  "themes": [
    "Definition and nature of poetry",
    "Comparative poetics (Arabic vs. Greek traditions)",
    "Metrical systems and rhythmic patterns",
    "Imaginative discourse and its effects",
    "Poetry as logical argumentation",
    "Classification of poetic forms",
    "Relationship between poetry and truth"
  ],
  
  "key_concepts": {
    "takhyīl (imagination)": "The quality of discourse that evokes images 
    in the mind of the listener, central to poetic effect",
    "wazn (meter)": "The rhythmic pattern that organizes poetic discourse 
    into measurable units",
    "qawl (statement)": "The basic unit of poetic composition, equivalent 
    to a verse or line",
    "īqāʿāt (rhythms)": "Regular patterns of sound that create the musical 
    quality of poetry",
    "qiyās shiʿrī (poetic syllogism)": "A form of logical argument that 
    operates through imaginative rather than demonstrative means"
  },
  
  "structure": [
    {"section": "Definition of Poetry", "function": "Establishes the essential 
    nature of poetic discourse"},
    {"section": "Comparative Analysis", "function": "Contrasts Arabic and Greek 
    poetic traditions"},
    {"section": "Metrical Theory", "function": "Explains the technical aspects 
    of poetic composition"},
    {"section": "Psychological Effects", "function": "Analyzes how poetry 
    affects the soul through imagination"},
    {"section": "Classification System", "function": "Categorizes types of 
    poetry by form and function"}
  ],
  
  "tradition": "Islamic Peripatetic philosophy with strong Aristotelian influence",
  
  "potential_influences": [
    {"source": "Aristotle's Poetics", "confidence": "High", 
     "evidence": "Conceptual framework, terminology, and analytical approach"},
    {"source": "Aristotle's Organon", "confidence": "Medium", 
     "evidence": "Logical framework and syllogistic approach"},
    {"source": "Arabic poetic tradition", "confidence": "High", 
     "evidence": "Technical terminology and metrical analysis"}
  ]
}
        </pre>
      </td>
    </tr>
  </table>
</div>

### Source Analyzer Output Example

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
{
  "verbal_parallels": [
    {
      "concept": "Mimesis/Takhyīl",
      "text_a": "ἡ γὰρ τῆς τραγῳδίας μίμησις μιμεῖται τοὺς πράττοντας",
      "text_b": "والتخييل هو أن تتمثل للسامع من لفظ الشاعر المخيل أو معانيه",
      "analysis": "Both texts use terms for imaginative representation as the 
      foundation of poetic effect, with Aristotle using 'mimesis' and Al-Farabi 
      using 'takhyīl'"
    },
    {
      "concept": "Poetic Forms Classification",
      "text_a": "ἐποποιία δὴ καὶ ἡ τῆς τραγῳδίας ποίησις ἔτι δὲ κωμῳδία",
      "text_b": "وأصناف الشعر عند اليونانيين المديح والهجاء والمراثي والتشبيب",
      "analysis": "Both texts systematically classify poetic forms, though with 
      culturally specific categories"
    }
  ],
  
  "conceptual_parallels": [
    {
      "concept": "Poetry as Logical Discourse",
      "text_a": "Aristotle presents poetry as having a logical structure with 
      its own form of reasoning",
      "text_b": "Al-Farabi explicitly develops the concept of 'poetic syllogism' 
      (qiyās shiʿrī) as a form of logical argument",
      "analysis": "Al-Farabi extends Aristotle's logical approach to poetry, 
      integrating it more explicitly with syllogistic reasoning"
    },
    {
      "concept": "Catharsis/Psychological Effect",
      "text_a": "δι' ἐλέου καὶ φόβου περαίνουσα τὴν τῶν τοιούτων παθημάτων κάθαρσιν",
      "text_b": "وقد يستعمل المخيل لإثارة انفعالات في النفس تؤدي إلى تطهيرها",
      "analysis": "Both texts address the psychological effects of poetry on the 
      audience, with Al-Farabi adopting Aristotle's concept of catharsis"
    }
  ],
  
  "methodological_similarities": [
    {
      "approach": "Analytical Framework",
      "similarity": "Both texts approach poetry as a subject for philosophical 
      analysis rather than purely aesthetic appreciation",
      "significance": "Indicates shared intellectual methodology characteristic 
      of Peripatetic tradition"
    },
    {
      "approach": "Comparative Analysis",
      "similarity": "Al-Farabi adopts Aristotle's comparative approach but extends 
      it to include Arabic poetic traditions",
      "significance": "Shows adaptation of Aristotelian methodology to new cultural context"
    }
  ],
  
  "influence_score": 0.85,
  
  "evidence": [
    "Terminological correspondences between key concepts",
    "Structural similarities in analytical approach",
    "Adaptation of Aristotelian concepts to Arabic poetic tradition",
    "Integration with broader Peripatetic philosophical framework",
    "Historical evidence of transmission through Syriac translations"
  ],
  
  "confidence_explanation": "The high confidence score (0.85) is based on multiple 
  lines of evidence including conceptual, methodological, and historical factors. 
  The adaptations and extensions in Al-Farabi's text are consistent with creative 
  engagement with a source text rather than coincidental similarity."
}
        </pre>
      </td>
    </tr>
  </table>
</div>

### Deep Analyzer Insights

Our deep analysis revealed specific transmission patterns between Aristotle's Poetics and Al-Farabi's work:

1. **Transmission Pathway**: 
   - Evidence suggests Al-Farabi accessed Aristotle's Poetics through Syriac translations
   - Key concepts were transmitted with terminological adaptations (mimesis → takhyīl)

2. **Conceptual Transformation**:
   - Al-Farabi integrated Aristotelian poetics with Arabic literary tradition
   - Extended Aristotle's logical framework to develop the concept of "poetic syllogism"
   - Adapted catharsis theory to Islamic philosophical psychology

3. **Cultural Adaptation**:
   - Modified classification system to accommodate Arabic poetic forms
   - Integrated analysis of metrical systems not present in Greek tradition
   - Recontextualized Aristotelian concepts within Islamic philosophical discourse

<div align="center">
  <table>
    <tr>
      <td align="center" width="45%">
        <h4>Aristotle's Original Concept</h4>
        <p>Mimesis (μίμησις) as imitation of actions</p>
      </td>
      <td align="center" width="10%">→</td>
      <td align="center" width="45%">
        <h4>Al-Farabi's Adaptation</h4>
        <p>Takhyīl (تخييل) as imaginative representation in the soul</p>
      </td>
    </tr>
  </table>
</div>

---

<a id="significance"></a>
## 🌟 Significance for Humanities

<table>
  <tr>
    <td align="center" width="33%">
      <h4>📚 Enhanced Research</h4>
      <ul>
        <li>Process large text volumes</li>
        <li>Identify hidden connections</li>
        <li>Cross-linguistic analysis</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h4>🔄 Methodological Innovation</h4>
      <ul>
        <li>Combine traditional and computational methods</li>
        <li>Quantitative + qualitative insights</li>
        <li>Reproducible processes</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h4>🌐 New Directions</h4>
      <ul>
        <li>Map influence networks</li>
        <li>Test transmission hypotheses</li>
        <li>Macro-level tradition analysis</li>
      </ul>
    </td>
  </tr>
</table>

---

<a id="limitations"></a>
## ⚠️ Limitations and Challenges

<table>
  <tr>
    <td align="center" width="33%">
      <h3>⚠️ AI Limitations</h3>
      <ul>
        <li>Occasional hallucinations</li>
        <li>Variable performance by language/period</li>
        <li>Requires expert validation</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h3>📊 Data Challenges</h3>
      <ul>
        <li>Input text quality dependency</li>
        <li>Limited digitized ancient texts</li>
        <li>Textual variants and translations</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h3>🔍 Methodological Considerations</h3>
      <ul>
        <li>Efficiency vs. depth balance</li>
        <li>AI-assisted scholarship transparency</li>
        <li>Integration with existing practices</li>
      </ul>
    </td>
  </tr>
</table>

---

<a id="future"></a>
## 🚀 Future Directions

<table>
  <tr>
    <td align="center" width="33%">
      <h3>🔧 Technical Enhancements</h3>
      <ul>
        <li>Specialized language models</li>
        <li>Influence network visualization</li>
        <li>Enhanced cross-linguistic capabilities</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h3>📚 Scholarly Applications</h3>
      <ul>
        <li>Additional philosophical traditions</li>
        <li>Concept evolution analysis</li>
        <li>Collaborative AI-assisted platforms</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h3>🌉 Interdisciplinary Opportunities</h3>
      <ul>
        <li>Computational linguistics + classics</li>
        <li>Shared humanities computing methods</li>
        <li>Computational philosophy standards</li>
      </ul>
    </td>
  </tr>
</table>

---

<a id="conclusion"></a>
## 🏆 Conclusion

The Source Analysis System represents a significant step forward in computational approaches to philosophical text analysis. By combining the strengths of AI with traditional scholarly methods, it offers new possibilities for understanding the complex relationships between texts across time, language, and tradition.

This project demonstrates the potential of thoughtful AI integration in humanities research—not replacing human scholars, but augmenting their capabilities and opening new avenues for discovery.

---

<div align="center">
  <h2>Thank You</h2>
  <p>For more information about this project, please contact:</p>
  <div style="padding: 20px; margin-top: 10px;">
    <p><strong>[Your Name]</strong><br>
    [Your Institution]<br>
    [Your Email]</p>
  </div>
  
  <p style="margin-top: 30px; font-size: 0.8em; color: #666;">
    © 2023 Source Analysis System Project • All Rights Reserved
  </p>
</div> 
