# 📚 Source Analysis System

<div align="center">
  
  ![Banner](pictures/Bodlein_Library_MS._Arab.d.84_roll332_frame1.jpg)
  
  <h2>Computational Approaches to Philosophical Text Analysis</h2>
  
  <p><em>Bridging ancient wisdom and modern AI</em></p>
  
  <p>
    <a href="#overview">Overview</a> •
    <a href="#problem">Problem Statement</a> •
    <a href="#pipeline">Pipeline</a> •
    <a href="#stage1">Thematizer</a> •
    <a href="#stage2">Source Analyzer</a> •
    <a href="#stage3">Deep Analyzer</a> •
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

The following sections demonstrate each stage of the pipeline with concrete examples of inputs, processes, and outputs for each stage, starting with the Thematizer.

---

<a id="stage1"></a>
## 🧠 Stage 1: Thematizer

<div align="center">
  <img src="pictures/Bekker_1831_page184.jpg" alt="Bekker Edition of Aristotle" width="500"/>
  <p><em>Page from Bekker's edition of Aristotle's works (1831), showing the type of texts analyzed by our system</em></p>
</div>

### Purpose

The Thematizer performs initial broad analysis of individual texts to identify themes, structure, and key concepts. It serves as the foundation for all subsequent analysis by creating comprehensive thematic profiles for each text.

### Input Example: Classical Arabic Text (Al-Farabi)

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

### Process

The Thematizer follows these steps:

1. **Text Preparation**
   - Ingests raw text files from input and database directories
   - Validates file structure and creates organized directory for outputs
   - Splits large texts into manageable chunks (approximately 20,000 characters)

2. **AI Analysis**
   - Processes each text chunk using Claude 3.5 Sonnet
   - Applies specialized prompt engineering for philosophical text analysis
   - Identifies author, title, text type, themes, and structural elements
   - Generates scholarly abstracts for each text chunk

3. **Result Compilation**
   - Merges analyses from multiple chunks with intelligent deduplication
   - Combines abstracts and consolidates themes
   - Identifies natural breaks and section divisions
   - Generates comprehensive thematic profiles

### AI Prompt Used

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
You are a Classical scholar specializing in ancient Greek and Arabic philosophy. 
You are analyzing an academic philosophical text that could be:
1. An ancient Greek philosophical work (like Aristotle's originals)
2. An Arabic philosophical text (like Al-Farabi's originals)
3. A commentary or interpretation of philosophical works
4. Part of the established philosophical canon

Please analyze the following chunk and extract:

1. Author identification
2. Title identification
3. Text type classification
4. Themes and concepts
5. Abstract focusing on main philosophical arguments
6. Structural elements

You MUST respond in valid JSON format with these exact fields:
{
    "author": "Author's name or 'Unknown' if not found in this chunk",
    "title": "Title of the work or 'Unknown' if not found in this chunk",
    "text_type": "original text|commentary|treatise|unknown",
    "themes": ["theme1", "theme2", ...],
    "abstract": "A scholarly abstract of this chunk of text.",
    "natural_breaks": ["Break 1", "Break 2", ...] or [] if none found
}
        </pre>
      </td>
    </tr>
  </table>
</div>

### Output Example

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

### Key Features

- **Multilingual Analysis**: Processes texts in Ancient Greek, Classical Arabic, and other languages
- **Intelligent Chunking**: Handles texts of any length by splitting into manageable chunks while preserving context
- **Structured Output**: Generates standardized JSON data for consistent downstream processing
- **Error Handling**: Implements robust retry logic and error recovery mechanisms
- **Comprehensive Logging**: Maintains detailed logs for transparency and debugging

---

<a id="stage2"></a>
## 🔍 Stage 2: Source Analyzer

### Purpose

The Source Analyzer compares texts to identify potential relationships and influences between them. It takes the thematic profiles generated by the Thematizer and performs pairwise comparisons to detect verbal parallels, conceptual similarities, and methodological connections.

### Input Example

The Source Analyzer takes two thematic profiles as input:

1. **Text A (Potential Source)**: Thematic profile of Aristotle's "Poetics"
```json
{
  "author": "Aristotle",
  "title": "Poetics",
  "text_type": "original text",
  "themes": [
    "Mimesis (imitation) as the foundation of poetry",
    "Classification of poetic forms (tragedy, comedy, epic)",
    "Structure and elements of tragedy",
    "Catharsis as emotional purification",
    "Unity of plot and action",
    "Character development in drama",
    "Relationship between poetry and truth"
  ],
  "abstract": "Aristotle's Poetics establishes a systematic theory of poetry and drama, focusing primarily on tragedy. The text defines poetry as mimesis (imitation) and analyzes how different poetic forms imitate reality through various means. Aristotle examines the structure of tragedy, identifying its six essential components: plot, character, thought, diction, melody, and spectacle. He emphasizes the primacy of plot and the importance of unity, completeness, and magnitude in dramatic composition. The work also discusses the psychological effects of tragedy, introducing the concept of catharsis as emotional purification through pity and fear."
}
```

2. **Text B (Text Under Analysis)**: Thematic profile of Al-Farabi's "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ"
```json
{
  "author": "Al-Farabi",
  "title": "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ",
  "text_type": "treatise",
  "themes": [
    "Definition and nature of poetry",
    "Comparative poetics (Arabic vs. Greek traditions)",
    "Metrical systems and rhythmic patterns",
    "Imaginative discourse and its effects",
    "Poetry as logical argumentation",
    "Classification of poetic forms",
    "Relationship between poetry and truth"
  ],
  "abstract": "Al-Farabi's text presents a systematic analysis of poetics, defining poetry as imaginative discourse with rhythmic patterns. It compares Arabic and Greek poetic traditions, highlighting differences in metrical systems while identifying universal elements of poetic composition. The text establishes a philosophical framework for understanding poetry as a form of logical discourse with specific effects on the soul."
}
```

### Process Workflow

The Source Analyzer follows a systematic workflow to compare texts and assess potential influence:

<div align="center">
  <table>
    <tr>
      <th>Step</th>
      <th>Action</th>
      <th>Purpose</th>
    </tr>
    <tr>
      <td>1</td>
      <td>Load thematic profiles</td>
      <td>Retrieve structured data from Thematizer outputs</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Identify shared themes</td>
      <td>Detect overlapping philosophical concepts</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Extract key passages</td>
      <td>Locate specific textual evidence for comparison</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Analyze verbal parallels</td>
      <td>Compare terminology, phrasing, and examples</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Analyze conceptual parallels</td>
      <td>Compare ideas, arguments, and frameworks</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Analyze methodological similarities</td>
      <td>Compare approaches, structures, and reasoning patterns</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Calculate confidence score</td>
      <td>Quantify likelihood of influence (0.0-1.0)</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Generate evidence summary</td>
      <td>Provide detailed justification for assessment</td>
    </tr>
  </table>
</div>

### Technical Implementation

The Source Analyzer is implemented as a Python module that:

1. **Loads and Validates Data**
   - Reads JSON outputs from the Thematizer
   - Validates data structure and required fields
   - Prepares text pairs for comparison

2. **Performs AI-Powered Analysis**
   - Constructs specialized prompts for Claude 3.5 Sonnet
   - Sends paired texts for comparative analysis
   - Processes and validates AI responses

3. **Generates Structured Results**
   - Creates standardized JSON output
   - Calculates confidence scores based on multiple factors
   - Organizes evidence by category (verbal, conceptual, methodological)

### AI Prompt Used

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
You are a comparative philosophical analyst with expertise in identifying textual relationships 
between ancient Greek and Arabic philosophical works. Your task is to compare two philosophical 
texts and assess potential influence or relationship.

TEXT A (Potential Source):
{
  "author": "{{text_a.author}}",
  "title": "{{text_a.title}}",
  "text_type": "{{text_a.text_type}}",
  "themes": {{text_a.themes|json}},
  "abstract": "{{text_a.abstract}}"
}

TEXT B (Text Under Analysis):
{
  "author": "{{text_b.author}}",
  "title": "{{text_b.title}}",
  "text_type": "{{text_b.text_type}}",
  "themes": {{text_b.themes|json}},
  "abstract": "{{text_b.abstract}}"
}

Please analyze these texts for evidence of influence or relationship, focusing on:

1. Verbal parallels:
   - Similar terminology or phrasing
   - Shared examples or illustrations
   - Comparable definitions of key concepts

2. Conceptual parallels:
   - Similar philosophical ideas or arguments
   - Comparable theoretical frameworks
   - Shared philosophical problems or questions

3. Methodological similarities:
   - Similar analytical approaches
   - Comparable organizational structures
   - Shared reasoning patterns or logical methods

4. Influence assessment:
   - Evaluate the likelihood of direct influence (scale 0.0-1.0)
   - Consider historical context and transmission pathways
   - Assess alternative explanations for similarities

Provide specific evidence for each category and explain your confidence score.
Format your analysis as structured JSON with these exact fields:
"verbal_parallels", "conceptual_parallels", "methodological_similarities", 
"influence_score", "evidence", "confidence_explanation"
        </pre>
      </td>
    </tr>
  </table>
</div>

### Output Example: Detailed Comparison Analysis

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
{
  "verbal_parallels": [
    {
      "concept": "Mimesis/Takhyīl",
      "text_a": "Aristotle defines poetry fundamentally as mimesis (μίμησις), 
                the imitation or representation of reality through artistic means",
      "text_b": "Al-Farabi establishes takhyīl (تخييل) as the central concept, 
                defining it as imaginative representation that creates images 
                in the mind of the listener",
      "analysis": "Both texts center their poetic theories on representational 
                  concepts, with Aristotle's mimesis and Al-Farabi's takhyīl 
                  serving analogous functions despite subtle differences in scope"
    },
    {
      "concept": "Poetic Forms Classification",
      "text_a": "Aristotle systematically categorizes poetry into tragedy, comedy, 
                and epic poetry, defining each by its means, objects, and manner 
                of imitation",
      "text_b": "Al-Farabi presents a classification system that acknowledges Greek 
                categories while incorporating Arabic forms like madīḥ (praise), 
                hijāʾ (satire), and rithāʾ (elegy)",
      "analysis": "Both authors employ taxonomic approaches to poetic forms, 
                  though Al-Farabi adapts the classification to accommodate 
                  Arabic literary traditions"
    },
    {
      "concept": "Technical Terminology",
      "text_a": "Aristotle employs specialized vocabulary including μῦθος (plot), 
                λέξις (diction), and κάθαρσις (catharsis)",
      "text_b": "Al-Farabi uses corresponding technical terms including ḥikāya 
                (narrative), lafẓ (verbal expression), and taṭhīr (purification)",
      "analysis": "The technical vocabulary shows clear correspondences that 
                  suggest deliberate translation or adaptation of Aristotelian 
                  terminology into Arabic philosophical language"
    }
  ],
  
  "conceptual_parallels": [
    {
      "concept": "Poetry as Logical Discourse",
      "text_a": "Aristotle integrates poetry into his broader philosophical system, 
                treating it as a form of knowledge with its own logical structure",
      "text_b": "Al-Farabi explicitly develops the concept of 'poetic syllogism' 
                (qiyās shiʿrī), positioning poetry within his logical framework 
                derived from Aristotle's Organon",
      "analysis": "Al-Farabi extends Aristotle's approach by more explicitly 
                  connecting poetics to formal logic, developing what was implicit 
                  in Aristotle into a systematic theory of poetic reasoning"
    },
    {
      "concept": "Psychological Effect of Poetry",
      "text_a": "Aristotle's theory of catharsis describes how tragedy produces 
                emotional purification through the arousal and resolution of 
                pity and fear",
      "text_b": "Al-Farabi analyzes how poetic discourse affects the soul through 
                imagination, creating emotional responses that can lead to 
                ethical improvement",
      "analysis": "Both philosophers are concerned with poetry's psychological 
                  impact, though Al-Farabi adapts the concept to fit within 
                  Islamic philosophical psychology"
    },
    {
      "concept": "Unity and Structure",
      "text_a": "Aristotle emphasizes the importance of unity, completeness, and 
                magnitude in tragic plots, arguing that a well-constructed plot 
                should have a beginning, middle, and end",
      "text_b": "Al-Farabi discusses structural principles for poetic composition, 
                emphasizing coherence and proportionality in relation to the 
                intended effect",
      "analysis": "Both texts present normative theories of poetic structure, 
                  though Al-Farabi's approach is more explicitly connected to 
                  the logical structure of arguments"
    }
  ],
  
  "methodological_similarities": [
    {
      "approach": "Analytical Framework",
      "similarity": "Both texts approach poetry as a subject for philosophical 
                    analysis rather than purely aesthetic appreciation, 
                    integrating poetics into broader philosophical systems",
      "significance": "Indicates shared intellectual methodology characteristic 
                      of Peripatetic tradition, suggesting Al-Farabi's conscious 
                      positioning within this philosophical lineage"
    },
    {
      "approach": "Comparative Analysis",
      "similarity": "Al-Farabi adopts Aristotle's comparative approach but extends 
                    it to include Arabic poetic traditions, explicitly comparing 
                    Greek and Arabic metrical systems and poetic forms",
      "significance": "Shows adaptation of Aristotelian methodology to new cultural 
                      context while maintaining the fundamental analytical approach"
    },
    {
      "approach": "Definition and Division",
      "similarity": "Both authors begin with general definitions of poetry and 
                    proceed by division into types and analysis of components, 
                    following the classical method of definition by genus and 
                    specific difference",
      "significance": "Demonstrates Al-Farabi's adoption of Aristotelian logical 
                      methods in structuring his treatise"
    }
  ],
  
  "influence_score": 0.85,
  
  "evidence": [
    "Terminological correspondences between key concepts (mimesis/takhyīl, 
     catharsis/taṭhīr)",
    "Structural similarities in analytical approach and organization",
    "Adaptation of Aristotelian concepts to Arabic poetic tradition",
    "Integration with broader Peripatetic philosophical framework",
    "Historical evidence of transmission through Syriac translations",
    "Al-Farabi's explicit references to 'the author of the book on poetry'",
    "Consistent pattern of creative adaptation rather than mere imitation"
  ],
  
  "confidence_explanation": "The high confidence score (0.85) is based on multiple 
  lines of evidence including terminological, conceptual, methodological, and 
  historical factors. The pattern of similarities shows systematic engagement 
  with Aristotle's text, while the adaptations and extensions demonstrate 
  Al-Farabi's creative interpretation rather than coincidental similarity. 
  Historical evidence confirms that Al-Farabi had access to Aristotle's Poetics 
  through the translation tradition, and his other works show similar patterns 
  of engagement with Aristotelian texts. The score is not higher (e.g., 0.95) 
  because some similarities could be attributed to shared philosophical tradition 
  rather than direct textual influence, and because Al-Farabi introduces 
  significant innovations not found in Aristotle."
}
        </pre>
      </td>
    </tr>
  </table>
</div>

### Confidence Score Calculation

The Source Analyzer calculates confidence scores based on a weighted combination of factors:

<div align="center">
  <table>
    <tr>
      <th>Factor</th>
      <th>Weight</th>
      <th>Description</th>
    </tr>
    <tr>
      <td>Verbal Parallels</td>
      <td>30%</td>
      <td>Similarity in terminology, phrasing, and examples</td>
    </tr>
    <tr>
      <td>Conceptual Parallels</td>
      <td>35%</td>
      <td>Similarity in ideas, arguments, and frameworks</td>
    </tr>
    <tr>
      <td>Methodological Similarities</td>
      <td>20%</td>
      <td>Similarity in approach, structure, and reasoning</td>
    </tr>
    <tr>
      <td>Historical Context</td>
      <td>15%</td>
      <td>Known transmission pathways and historical evidence</td>
    </tr>
  </table>
</div>

### Results Visualization

The Source Analyzer generates visualizations to help scholars understand the relationships between texts:

<div align="center">
  <table>
    <tr>
      <th colspan="3">Influence Confidence Matrix</th>
    </tr>
    <tr>
      <th>Source Text</th>
      <th>Target Text</th>
      <th>Confidence Score</th>
    </tr>
    <tr>
      <td>Aristotle: Poetics</td>
      <td>Al-Farabi: Risālah fī qawānīn ṣināʿat al-šuʿarāʾ</td>
      <td><strong>0.85</strong></td>
    </tr>
    <tr>
      <td>Aristotle: Analytica Posteriora</td>
      <td>Al-Farabi: Risālah fī qawānīn ṣināʿat al-šuʿarāʾ</td>
      <td><strong>0.40</strong></td>
    </tr>
    <tr>
      <td>Plato: Republic (Books II-III)</td>
      <td>Al-Farabi: Risālah fī qawānīn ṣināʿat al-šuʿarāʾ</td>
      <td><strong>0.25</strong></td>
    </tr>
    <tr>
      <td>Arabic Poetic Tradition</td>
      <td>Al-Farabi: Risālah fī qawānīn ṣināʿat al-šuʿarāʾ</td>
      <td><strong>0.70</strong></td>
    </tr>
  </table>
</div>

### Key Features

- **Cross-Linguistic Analysis**: Compares texts across different languages and traditions
- **Evidence-Based Assessment**: Provides specific textual evidence for each claim
- **Confidence Scoring**: Quantifies the likelihood of influence on a standardized scale
- **Multi-Dimensional Analysis**: Examines verbal, conceptual, and methodological parallels
- **Historical Contextualization**: Considers known transmission pathways and historical factors

---

<a id="stage3"></a>
## 🔬 Stage 3: Deep Analyzer

<div align="center">
  <img src="pictures/comparison_analysis.jpg" alt="Deep Analysis Visualization" width="500"/>
  <p><em>Visualization of conceptual transformations between philosophical traditions</em></p>
</div>

### Purpose

The Deep Analyzer performs in-depth analysis of high-confidence matches identified by the Source Analyzer. It focuses on text pairs with high confidence scores (≥0.7) and provides detailed evidence-based assessment of influence patterns, transmission pathways, and conceptual transformations.

### Input Example

The Deep Analyzer takes three inputs:

1. **Text A (Potential Source)**: Full text of Aristotle's "Poetics"
```
περὶ ποιητικῆς αὐτῆς τε καὶ τῶν εἰδῶν αὐτῆς, ἥν τινα δύναμιν ἕκαστον ἔχει, καὶ πῶς 
δεῖ συνίστασθαι τοὺς μύθους εἰ μέλλει καλῶς ἕξειν ἡ ποίησις, ἔτι δὲ ἐκ πόσων καὶ 
ποίων ἐστὶ μορίων, ὁμοίως δὲ καὶ περὶ τῶν ἄλλων ὅσα τῆς αὐτῆς ἐστι μεθόδου, λέγωμεν 
ἀρξάμενοι κατὰ φύσιν πρῶτον ἀπὸ τῶν πρώτων.

ἐποποιία δὴ καὶ ἡ τῆς τραγῳδίας ποίησις ἔτι δὲ κωμῳδία καὶ ἡ διθυραμβοποιητικὴ καὶ 
τῆς αὐλητικῆς ἡ πλείστη καὶ κιθαριστικῆς πᾶσαι τυγχάνουσιν οὖσαι μιμήσεις τὸ σύνολον...
```

2. **Text B (Text Under Analysis)**: Full text of Al-Farabi's "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ"
```
وأما الشعر فإنه كلام مخيل مؤلف من أقوال لها إيقاعات متساوية، وهذه الأقوال 
متساوية الأجزاء عند العرب متفقة الأواخر، وعند اليونانيين متساوية في الأزمنة 
متفقة الأوزان، وكل قول منها عند العرب يسمى بيتا، وعند اليونانيين يسمى الواحد 
منها فاصلة، وعند كثير من الأمم يسمى الواحد منها سطرا...
```

3. **Previous Analysis**: Source Analyzer results for this text pair
```json
{
  "verbal_parallels": [
    {
      "concept": "Mimesis/Takhyīl",
      "text_a": "Aristotle defines poetry fundamentally as mimesis (μίμησις)...",
      "text_b": "Al-Farabi establishes takhyīl (تخييل) as the central concept...",
      "analysis": "Both texts center their poetic theories on representational concepts..."
    },
    // Additional verbal parallels...
  ],
  "conceptual_parallels": [
    // Conceptual parallels from Source Analyzer...
  ],
  "methodological_similarities": [
    // Methodological similarities from Source Analyzer...
  ],
  "influence_score": 0.85,
  "evidence": [
    // Evidence points from Source Analyzer...
  ],
  "confidence_explanation": "The high confidence score (0.85) is based on multiple lines of evidence..."
}
```

### Process Workflow

The Deep Analyzer follows a systematic workflow to provide comprehensive analysis:

<div align="center">
  <table>
    <tr>
      <th>Phase</th>
      <th>Actions</th>
      <th>Outputs</th>
    </tr>
    <tr>
      <td>1. Preparation</td>
      <td>
        • Load full texts and previous analysis<br>
        • Identify key passages for detailed comparison<br>
        • Extract relevant historical context
      </td>
      <td>Aligned passage pairs for analysis</td>
    </tr>
    <tr>
      <td>2. Transmission Analysis</td>
      <td>
        • Analyze textual dependencies<br>
        • Map conceptual relationships<br>
        • Reconstruct transmission pathways
      </td>
      <td>Transmission pathway diagram</td>
    </tr>
    <tr>
      <td>3. Conceptual Analysis</td>
      <td>
        • Compare philosophical frameworks<br>
        • Identify conceptual transformations<br>
        • Analyze cultural adaptations
      </td>
      <td>Concept transformation matrix</td>
    </tr>
    <tr>
      <td>4. Linguistic Analysis</td>
      <td>
        • Map terminology correspondences<br>
        • Analyze translation patterns<br>
        • Compare argumentative structures
      </td>
      <td>Terminology correspondence table</td>
    </tr>
    <tr>
      <td>5. Synthesis</td>
      <td>
        • Integrate findings from all analyses<br>
        • Generate comprehensive report<br>
        • Provide scholarly citations
      </td>
      <td>Comprehensive analysis report</td>
    </tr>
  </table>
</div>

### Technical Implementation

The Deep Analyzer is implemented as a Python module that:

1. **Processes Full Texts**
   - Handles original language texts (Ancient Greek, Classical Arabic, etc.)
   - Aligns passages based on thematic and conceptual similarities
   - Extracts key passages for detailed comparison

2. **Applies Specialized AI Analysis**
   - Uses Claude 3.5 Sonnet with specialized prompts for deep philosophical analysis
   - Implements multi-step reasoning for complex influence assessment
   - Applies historical and cultural context to interpretation

3. **Generates Comprehensive Reports**
   - Creates detailed analysis reports with specific textual evidence
   - Produces visualizations of conceptual transformations
   - Provides scholarly citations and references

### AI Prompt Used

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
You are a specialist in philosophical transmission analysis with expertise in cross-cultural 
philosophical influence between Ancient Greek and Classical Arabic traditions. Your task is 
to perform an in-depth analysis of the relationship between two texts that have been identified 
as having a high probability of influence.

TEXT A (Potential Source):
{{text_a_full}}

TEXT B (Text Under Analysis):
{{text_b_full}}

PREVIOUS ANALYSIS:
{{source_analyzer_results}}

HISTORICAL CONTEXT:
{{historical_context}}

Please provide a detailed analysis of:

1. Transmission patterns:
   - Identify specific passages showing direct textual dependencies
   - Map conceptual dependencies between the texts
   - Reconstruct possible transmission pathways considering historical factors
   - Assess the role of intermediate translations or commentaries

2. Philosophical development:
   - Analyze how specific concepts from Text A are developed or transformed in Text B
   - Identify innovations or adaptations in Text B not present in Text A
   - Explain cultural or contextual factors affecting the transformation
   - Assess the philosophical significance of these transformations

3. Linguistic transformation:
   - Create a detailed mapping of technical terminology correspondences
   - Analyze translation or adaptation patterns across languages
   - Compare argumentative structures and rhetorical strategies
   - Identify language-specific features affecting conceptual expression

For each observation, provide:
   - Specific textual evidence with original language quotations
   - Scholarly context including relevant secondary literature
   - Confidence assessment for each claim
   - Alternative interpretations where appropriate

Format your analysis as a comprehensive scholarly report with clearly defined sections.
        </pre>
      </td>
    </tr>
  </table>
</div>

### Output Example: Comprehensive Analysis Report

<div align="center">
  <table>
    <tr>
      <td>
        <pre>
# Deep Analysis Report: Al-Farabi's Poetics and Aristotle's Poetics

## Executive Summary

This analysis confirms a high probability (0.85) of direct influence from Aristotle's 
Poetics on Al-Farabi's "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ." The influence manifests 
through systematic terminological correspondences, conceptual adaptations, and methodological 
similarities. Al-Farabi's work represents a creative adaptation rather than mere translation, 
integrating Aristotelian poetics into Islamic philosophical discourse while accommodating 
Arabic literary traditions.

## 1. Transmission Patterns

### 1.1 Direct Textual Dependencies

Seven passages show strong evidence of direct textual dependency:

| Aristotle's Poetics | Al-Farabi's Risālah | Analysis |
|---------------------|---------------------|----------|
| "ἐποποιία δὴ καὶ ἡ τῆς τραγῳδίας ποίησις ἔτι δὲ κωμῳδία καὶ ἡ διθυραμβοποιητικὴ καὶ τῆς αὐλητικῆς ἡ πλείστη καὶ κιθαριστικῆς πᾶσαι τυγχάνουσιν οὖσαι μιμήσεις τὸ σύνολον" (1447a13-15) | "فأما الشعر اليوناني فإنه ينقسم إلى المديح والهجاء والتراجيديا والكوميديا والديثرمبية وغير ذلك، وكلها تشترك في كونها محاكاة" | Al-Farabi follows Aristotle's classification system while adapting it to include Arabic forms. The structural parallel is unmistakable, though Al-Farabi adds "madīḥ" (praise) and "hijāʾ" (satire) to accommodate Arabic tradition. |
| "ἐπεὶ δὲ μιμοῦνται οἱ μιμούμενοι πράττοντας, ἀνάγκη δὲ τούτους ἢ σπουδαίους ἢ φαύλους εἶναι" (1448a1-2) | "والمحاكاة إما أن تكون لأفعال الفضلاء أو لأفعال الأشرار" | Direct correspondence in the ethical classification of mimetic subjects as either virtuous or base. The parallel extends to the logical structure of the division. |

Five additional passages show similar dependencies (confidence: high).

### 1.2 Conceptual Dependencies

The analysis identifies three primary conceptual dependencies:

1. **Mimesis Framework**: Al-Farabi adopts Aristotle's foundational concept of mimesis but transforms it into "takhyīl" (imaginative representation), expanding its scope to include psychological effects.

2. **Logical Structure**: Al-Farabi integrates poetics into the logical framework derived from Aristotle's Organon, developing the concept of "poetic syllogism" (qiyās shiʿrī).

3. **Cathartic Function**: Al-Farabi adapts Aristotle's theory of catharsis to align with Islamic philosophical psychology, emphasizing ethical improvement through imaginative experience.

### 1.3 Transmission Pathway

Historical evidence supports the following transmission pathway:

1. Aristotle's Poetics (4th century BCE, Greek)
2. Syriac translation by Abu Bishr Matta ibn Yunus (9th century CE)
3. Arabic commentaries in Baghdad Peripatetic circle
4. Al-Farabi's direct access to these translations and commentaries

Evidence includes:
- Al-Farabi's references to "the author of the book on poetry" (صاحب كتاب الشعر)
- Terminological consistency with established translation conventions
- Historical documentation of Al-Farabi's association with Abu Bishr Matta
- References to intermediate commentaries by Themistius and Alexander of Aphrodisias

## 2. Philosophical Development

### 2.1 Conceptual Transformations

| Aristotelian Concept | Al-Farabi's Transformation | Significance |
|----------------------|----------------------------|--------------|
| Mimesis (μίμησις) as imitation of actions | Takhyīl (تخييل) as imaginative representation in the soul | Shifts focus from objective representation to psychological effect |
| Catharsis (κάθαρσις) as emotional purification | Taṭhīr (تطهير) integrated with ethical improvement | Aligns with Islamic ethical philosophy |
| Poetry as separate from logic | "Poetic syllogism" (قياس شعري) as part of logical system | Integrates poetics into comprehensive logical framework |

### 2.2 Innovations in Al-Farabi

1. **Comparative Poetics**: Al-Farabi systematically compares Greek and Arabic poetic traditions, analyzing differences in metrical systems and poetic forms.

2. **Psychological Theory**: Develops a sophisticated theory of how poetic discourse affects the soul through imagination, extending beyond Aristotle's more limited discussion.

3. **Integration with Islamic Philosophy**: Situates poetics within the broader Islamic philosophical system, connecting it to theories of knowledge, ethics, and politics.

### 2.3 Cultural Adaptation Factors

The transformation of Aristotelian concepts in Al-Farabi's work is shaped by:

1. **Islamic Intellectual Context**: Adaptation to monotheistic theological framework
2. **Arabic Literary Tradition**: Accommodation of established Arabic poetic forms and criticism
3. **Translation Movement Context**: Part of broader project to integrate Greek philosophy into Islamic thought
4. **Political Context**: Alignment with Al-Farabi's political philosophy and concept of the virtuous city

## 3. Linguistic Transformation

### 3.1 Terminology Correspondences

| Greek Term | Arabic Equivalent | Semantic Shift |
|------------|-------------------|----------------|
| μίμησις (mimesis) | تخييل (takhyīl) | From "imitation" to "causing imagination" |
| κάθαρσις (catharsis) | تطهير (taṭhīr) | Similar meaning but with ethical dimension |
| μῦθος (mythos) | حكاية (ḥikāya) | From "plot" to "narrative" |
| λέξις (lexis) | لفظ (lafẓ) | From "diction" to "verbal expression" |
| διάνοια (dianoia) | فكر (fikr) | From "thought" to "intellectual content" |
| μέλος (melos) | لحن (laḥn) | From "melody" to "musical mode" |
| ὄψις (opsis) | منظر (manẓar) | From "spectacle" to "visual aspect" |

### 3.2 Translation Patterns

Analysis reveals three primary translation strategies:

1. **Conceptual Adaptation**: 65% of terms show conceptual rather than literal translation
2. **Terminological Innovation**: 25% of terms represent new technical vocabulary
3. **Direct Calque**: 10% of terms show direct word-for-word translation

### 3.3 Argumentative Structure

Al-Farabi preserves Aristotle's analytical approach while adapting to Arabic rhetorical conventions:

1. Maintains definition-division-analysis structure
2. Incorporates Islamic scholarly citation practices
3. Adapts Greek syllogistic reasoning to Arabic logical forms
4. Integrates comparative elements not present in Aristotle

## 4. Scholarly Significance

This analysis confirms that Al-Farabi's engagement with Aristotle's Poetics represents:

1. A crucial link in the transmission of Greek poetic theory to the Islamic world
2. A creative adaptation rather than mere translation or commentary
3. An integration of poetics into a comprehensive philosophical system
4. A foundation for subsequent developments in Arabic literary theory

The evidence strongly supports the classification of Al-Farabi's work as a creative adaptation of Aristotle's Poetics, transformed through the lens of Islamic philosophy and Arabic literary tradition.

## 5. References

1. Black, D. (1990). Logic and Aristotle's Rhetoric and Poetics in Medieval Arabic Philosophy. Brill.
2. Butterworth, C. (1987). "Al-Farabi's Introductory Sections on Logic." Arabic Sciences and Philosophy, 7(1), 93-124.
3. Dahiyat, I. (1974). Avicenna's Commentary on the Poetics of Aristotle. Brill.
4. Kemal, S. (1991). The Poetics of Alfarabi and Avicenna. Brill.
5. Walzer, R. (1985). Al-Farabi on the Perfect State. Oxford University Press.
        </pre>
      </td>
    </tr>
  </table>
</div>

### Key Features and Visualizations

#### Concept Transformation Map

<div align="center">
  <table>
    <tr>
      <th colspan="3">Conceptual Transformation from Aristotle to Al-Farabi</th>
    </tr>
    <tr>
      <th width="30%">Greek Concept</th>
      <th width="40%">Transformation Process</th>
      <th width="30%">Arabic Adaptation</th>
    </tr>
    <tr>
      <td>μίμησις<br>(mimesis)</td>
      <td>→ Translation + Psychological extension + Integration with logic</td>
      <td>تخييل<br>(takhyīl)</td>
    </tr>
    <tr>
      <td>κάθαρσις<br>(catharsis)</td>
      <td>→ Translation + Ethical reframing + Integration with soul theory</td>
      <td>تطهير<br>(taṭhīr)</td>
    </tr>
    <tr>
      <td>τραγῳδία<br>(tragedy)</td>
      <td>→ Translation + Cultural adaptation + Genre modification</td>
      <td>تراجيديا<br>(trājīdiyā)</td>
    </tr>
    <tr>
      <td>μέτρον<br>(meter)</td>
      <td>→ Translation + Technical adaptation to Arabic prosody</td>
      <td>وزن<br>(wazn)</td>
    </tr>
  </table>
</div>

#### Transmission Pathway Visualization

<div align="center">
  <table>
    <tr>
      <td align="center">
        <strong>Aristotle's Poetics</strong><br>
        (Greek, 4th century BCE)
      </td>
    </tr>
    <tr>
      <td align="center">↓<br><em>Translation</em></td>
    </tr>
    <tr>
      <td align="center">
        <strong>Syriac Translation</strong><br>
        (Abu Bishr Matta, 9th century CE)
      </td>
    </tr>
    <tr>
      <td align="center">↓<br><em>Translation + Commentary</em></td>
    </tr>
    <tr>
      <td align="center">
        <strong>Baghdad Peripatetic Circle</strong><br>
        (9th-10th centuries CE)
      </td>
    </tr>
    <tr>
      <td align="center">↓<br><em>Philosophical Adaptation</em></td>
    </tr>
    <tr>
      <td align="center">
        <strong>Al-Farabi's Poetics</strong><br>
        (Arabic, 10th century CE)
      </td>
    </tr>
  </table>
</div>

### Scholarly Applications

The Deep Analyzer provides scholars with:

1. **Evidence-Based Assessment**: Detailed textual evidence for influence claims
2. **Conceptual Mapping**: Visualization of how concepts transform across traditions
3. **Transmission Reconstruction**: Evidence-based reconstruction of transmission pathways
4. **Cultural Contextualization**: Analysis of how cultural factors shape philosophical adaptation
5. **Interdisciplinary Integration**: Combines philological, philosophical, and historical approaches

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
