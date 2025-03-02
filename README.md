# 📚 Source Analysis System

<div align="center">
  
  ![Banner](pictures/Bodlein_Library_MS._Arab.d.84_roll332_frame1.jpg)
  
  <h2>Computational Approaches to Philosophical Text Analysis</h2>
  
  <p><em>Bridging ancient wisdom and modern AI</em></p>
  
  <p>
    <a href="#overview">Overview</a> •
    <a href="#pipeline">Pipeline</a> •
    <a href="#case-study">Case Study</a> •
    <a href="#significance">Significance</a> •
    <a href="#future">Future</a>
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

<div align="center">
  <img src="pictures/Bekker_1831_page184.jpg" alt="Bekker Edition of Aristotle" width="500"/>
  <p><em>Page from Bekker's edition of Aristotle's works (1831), showing the type of texts analyzed by our system</em></p>
</div>

---

<a id="technical"></a>
## 💻 Technical Implementation

<table>
  <tr>
    <td align="center" width="33%">
      <h3>💻 Languages</h3>
      <ul>
        <li>Python for core processing</li>
        <li>OpenAI and Anthropic APIs</li>
        <li>JSON for data storage</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h3>🏗️ Architecture</h3>
      <ul>
        <li>Modular design</li>
        <li>Robust error handling</li>
        <li>Comprehensive logging</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h3>🤖 AI Integration</h3>
      <ul>
        <li>Strategic prompt engineering</li>
        <li>Model selection by task</li>
        <li>Output validation</li>
      </ul>
    </td>
  </tr>
</table>

---

<a id="case-study"></a>
## 📖 Case Study: Al-Farabi and Aristotle

Our system has been tested on analyzing the relationship between Al-Farabi's "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ" and Aristotle's works:

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

### 📊 Initial Findings
- Strong thematic connections to Aristotle's "Poetics" (0.85 confidence)
- Moderate connections to "Analytica Posteriora"
- Shared concepts of mimesis and poetic categorization

### 💡 Key Insights
- Identified specific verbal parallels between Arabic and Greek texts
- Traced conceptual adaptations across linguistic boundaries
- Provided evidence-based assessment of transmission pathways

---

<a id="significance"></a>
## 🌟 Significance

### 📚 For Humanities

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

### ⚙️ For Engineering

<table>
  <tr>
    <td align="center" width="33%">
      <h4>🧠 Novel AI Applications</h4>
      <ul>
        <li>Specialized LLM use</li>
        <li>Domain-specific prompting</li>
        <li>Multi-stage refinement</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h4>🔄 Technical Challenges</h4>
      <ul>
        <li>Cross-linguistic comparison</li>
        <li>Specialized vocabulary</li>
        <li>Precision-recall balance</li>
      </ul>
    </td>
    <td align="center" width="33%">
      <h4>🧩 Extensible Framework</h4>
      <ul>
        <li>Modular design</li>
        <li>Continuous improvement</li>
        <li>Integration-friendly outputs</li>
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
