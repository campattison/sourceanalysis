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

<div class="grid-container" style="display: grid; grid-template-columns: 2fr 1fr; gap: 20px; align-items: center;">
  <div>
    <h3>Challenges in Traditional Analysis</h3>
    <ul>
      <li><strong>Labor-Intensive Process:</strong> Tracing the transmission of ideas across philosophical traditions requires extensive manual effort</li>
      <li><strong>Human Limitations:</strong> Individual scholars can only process a finite amount of text</li>
      <li><strong>Subjective Biases:</strong> Manual analysis is influenced by individual scholar perspectives</li>
      <li><strong>Cross-Linguistic Barriers:</strong> Comparing texts across languages adds significant complexity</li>
    </ul>
    <h3>Our Solution</h3>
    <p>Leverage AI to augment scholarly analysis while maintaining rigorous academic standards</p>
  </div>
  <div align="center">
    <img src="pictures/Immanuel_Bekker_-_Imagines_philologorum.jpg" alt="Immanuel Bekker" width="300"/>
    <p><em>Immanuel Bekker (1785-1871)<br>Classical philologist whose work exemplifies traditional source analysis</em></p>
  </div>
</div>

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

<div class="stage-container" style="display: flex; align-items: center; margin-bottom: 20px;">
  <div class="stage-content" style="flex: 3;">
    <p><strong>Purpose:</strong> Initial broad analysis of texts to identify themes, structure, and key concepts</p>
    
    <p><strong>Process:</strong></p>
    <ul>
      <li>📥 Ingests raw text files from input and database directories</li>
      <li>🧠 Performs deep thematic analysis using Claude AI</li>
      <li>🔑 Extracts metadata, themes, abstracts, and structural breaks</li>
      <li>📋 Generates comprehensive thematic profiles for each text</li>
    </ul>
    
    <p><strong>Output:</strong></p>
    <ul>
      <li>JSON data with detailed thematic analysis</li>
      <li>Human-readable summary reports</li>
      <li>Foundation for subsequent analysis stages</li>
    </ul>
  </div>
</div>

### <img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/magnifying-glass.svg" width="20" height="20"> Source Analyzer

<div class="stage-container" style="display: flex; align-items: center; margin-bottom: 20px;">
  <div class="stage-content" style="flex: 3;">
    <p><strong>Purpose:</strong> Compare texts to identify potential relationships and influences</p>
    
    <p><strong>Process:</strong></p>
    <ul>
      <li>🔄 Takes thematizer results as input</li>
      <li>🔍 Performs pairwise comparisons between input texts and database texts</li>
      <li>🔗 Identifies verbal parallels, conceptual parallels, methodological similarities</li>
      <li>📊 Calculates confidence scores based on multiple factors</li>
    </ul>
    
    <p><strong>Output:</strong></p>
    <ul>
      <li>Detailed comparison reports with evidence of relationships</li>
      <li>Confidence scores indicating likelihood of influence</li>
      <li>Recommendations for further research</li>
    </ul>
  </div>
</div>

### <img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/microscope.svg" width="20" height="20"> Deep Analyzer

<div class="stage-container" style="display: flex; align-items: center; margin-bottom: 20px;">
  <div class="stage-content" style="flex: 3;">
    <p><strong>Purpose:</strong> Perform in-depth analysis of high-confidence matches</p>
    
    <p><strong>Process:</strong></p>
    <ul>
      <li>🎯 Focuses only on text pairs with high confidence scores (≥0.7)</li>
      <li>🔬 Analyzes three key dimensions:
        <ul>
          <li>Transmission patterns (direct textual dependencies, conceptual dependencies)</li>
          <li>Philosophical development (argument structure, conceptual frameworks)</li>
          <li>Linguistic transformation (technical terminology, argumentative language)</li>
        </ul>
      </li>
      <li>📝 Provides concrete evidence for each observation</li>
    </ul>
    
    <p><strong>Output:</strong></p>
    <ul>
      <li>Comprehensive analysis of textual relationships</li>
      <li>Evidence-based assessment of influence patterns</li>
      <li>Detailed reports suitable for scholarly use</li>
    </ul>
  </div>
</div>

<div align="center">
  <img src="pictures/Bekker_1831_page184.jpg" alt="Bekker Edition of Aristotle" width="500"/>
  <p><em>Page from Bekker's edition of Aristotle's works (1831), showing the type of texts analyzed by our system</em></p>
</div>

---

<a id="technical"></a>
## 💻 Technical Implementation

<div align="center">
  <div class="tech-grid" style="display: flex; justify-content: space-between; margin: 30px 0;">
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>💻 Languages</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Python for core processing</li>
        <li>OpenAI and Anthropic APIs</li>
        <li>JSON for data storage</li>
      </ul>
    </div>
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>🏗️ Architecture</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Modular design</li>
        <li>Robust error handling</li>
        <li>Comprehensive logging</li>
      </ul>
    </div>
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>🤖 AI Integration</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Strategic prompt engineering</li>
        <li>Model selection by task</li>
        <li>Output validation</li>
      </ul>
    </div>
  </div>
</div>

---

<a id="case-study"></a>
## 📖 Case Study: Al-Farabi and Aristotle

<div class="case-study" style="margin: 20px 0;">
  <p>Our system has been tested on analyzing the relationship between Al-Farabi's "Risālah fī qawānīn ṣināʿat al-šuʿarāʾ" and Aristotle's works:</p>

  <div align="center">
    <table>
      <tr>
        <th width="40%">Comparison</th>
        <th width="20%">Confidence Score</th>
        <th width="40%">Key Findings</th>
      </tr>
      <tr>
        <td align="center">Al-Farabi → Poetics</td>
        <td align="center"><span style="color: #2ecc71; font-weight: bold;">0.85</span></td>
        <td>Strong thematic and conceptual parallels</td>
      </tr>
      <tr>
        <td align="center">Al-Farabi → Analytica Posteriora</td>
        <td align="center"><span style="color: #f39c12; font-weight: bold;">0.40</span></td>
        <td>Moderate methodological similarities</td>
      </tr>
    </table>
  </div>

  <div class="findings" style="margin-top: 20px;">
    <h3>📊 Initial Findings</h3>
    <ul>
      <li>Strong thematic connections to Aristotle's "Poetics" (0.85 confidence)</li>
      <li>Moderate connections to "Analytica Posteriora"</li>
      <li>Shared concepts of mimesis and poetic categorization</li>
    </ul>

    <h3>💡 Key Insights</h3>
    <ul>
      <li>Identified specific verbal parallels between Arabic and Greek texts</li>
      <li>Traced conceptual adaptations across linguistic boundaries</li>
      <li>Provided evidence-based assessment of transmission pathways</li>
    </ul>
  </div>
</div>

---

<a id="significance"></a>
## 🌟 Significance

<div class="significance-container">
  <div class="humanities" style="margin-bottom: 30px;">
    <h3>📚 For Humanities</h3>
    
    <div align="center">
      <div class="significance-grid" style="display: flex; justify-content: space-between; margin: 20px 0;">
        <div style="flex: 1; text-align: center; padding: 15px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa;">
          <h4>📚 Enhanced Research</h4>
          <ul style="text-align: left; list-style-position: inside;">
            <li>Process large text volumes</li>
            <li>Identify hidden connections</li>
            <li>Cross-linguistic analysis</li>
          </ul>
        </div>
        <div style="flex: 1; text-align: center; padding: 15px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa;">
          <h4>🔄 Methodological Innovation</h4>
          <ul style="text-align: left; list-style-position: inside;">
            <li>Combine traditional and computational methods</li>
            <li>Quantitative + qualitative insights</li>
            <li>Reproducible processes</li>
          </ul>
        </div>
        <div style="flex: 1; text-align: center; padding: 15px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa;">
          <h4>🌐 New Directions</h4>
          <ul style="text-align: left; list-style-position: inside;">
            <li>Map influence networks</li>
            <li>Test transmission hypotheses</li>
            <li>Macro-level tradition analysis</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  
  <div class="engineering" style="margin-bottom: 30px;">
    <h3>⚙️ For Engineering</h3>
    
    <div align="center">
      <div class="significance-grid" style="display: flex; justify-content: space-between; margin: 20px 0;">
        <div style="flex: 1; text-align: center; padding: 15px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa;">
          <h4>🧠 Novel AI Applications</h4>
          <ul style="text-align: left; list-style-position: inside;">
            <li>Specialized LLM use</li>
            <li>Domain-specific prompting</li>
            <li>Multi-stage refinement</li>
          </ul>
        </div>
        <div style="flex: 1; text-align: center; padding: 15px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa;">
          <h4>🔄 Technical Challenges</h4>
          <ul style="text-align: left; list-style-position: inside;">
            <li>Cross-linguistic comparison</li>
            <li>Specialized vocabulary</li>
            <li>Precision-recall balance</li>
          </ul>
        </div>
        <div style="flex: 1; text-align: center; padding: 15px; margin: 0 10px; border-radius: 8px; background-color: #f8f9fa;">
          <h4>🧩 Extensible Framework</h4>
          <ul style="text-align: left; list-style-position: inside;">
            <li>Modular design</li>
            <li>Continuous improvement</li>
            <li>Integration-friendly outputs</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

---

<a id="limitations"></a>
## ⚠️ Limitations and Challenges

<div align="center">
  <div class="limitations-grid" style="display: flex; justify-content: space-between; margin: 20px 0;">
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #fff3f3; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>⚠️ AI Limitations</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Occasional hallucinations</li>
        <li>Variable performance by language/period</li>
        <li>Requires expert validation</li>
      </ul>
    </div>
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f0f8ff; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>📊 Data Challenges</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Input text quality dependency</li>
        <li>Limited digitized ancient texts</li>
        <li>Textual variants and translations</li>
      </ul>
    </div>
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f0fff0; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>🔍 Methodological Considerations</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Efficiency vs. depth balance</li>
        <li>AI-assisted scholarship transparency</li>
        <li>Integration with existing practices</li>
      </ul>
    </div>
  </div>
</div>

---

<a id="future"></a>
## 🚀 Future Directions

<div align="center">
  <div class="future-grid" style="display: flex; justify-content: space-between; margin: 20px 0;">
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f5f5f5; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>🔧 Technical Enhancements</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Specialized language models</li>
        <li>Influence network visualization</li>
        <li>Enhanced cross-linguistic capabilities</li>
      </ul>
    </div>
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f5f5f5; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>📚 Scholarly Applications</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Additional philosophical traditions</li>
        <li>Concept evolution analysis</li>
        <li>Collaborative AI-assisted platforms</li>
      </ul>
    </div>
    <div style="flex: 1; text-align: center; padding: 20px; margin: 0 10px; border-radius: 8px; background-color: #f5f5f5; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <h3>🌉 Interdisciplinary Opportunities</h3>
      <ul style="text-align: left; list-style-position: inside;">
        <li>Computational linguistics + classics</li>
        <li>Shared humanities computing methods</li>
        <li>Computational philosophy standards</li>
      </ul>
    </div>
  </div>
</div>

---

<a id="conclusion"></a>
## 🏆 Conclusion

<div class="conclusion" style="background-color: #f9f9f9; padding: 20px; border-radius: 8px; margin: 20px 0;">
  <p>The Source Analysis System represents a significant step forward in computational approaches to philosophical text analysis. By combining the strengths of AI with traditional scholarly methods, it offers new possibilities for understanding the complex relationships between texts across time, language, and tradition.</p>

  <p>This project demonstrates the potential of thoughtful AI integration in humanities research—not replacing human scholars, but augmenting their capabilities and opening new avenues for discovery.</p>
</div>

---

<div align="center">
  <h2>Thank You</h2>
  <p>For more information about this project, please contact:</p>
  <div style="display: inline-block; padding: 20px; border-radius: 8px; background-color: #f5f5f5; margin-top: 10px;">
    <p><strong>[Your Name]</strong><br>
    [Your Institution]<br>
    [Your Email]</p>
  </div>
  
  <p style="margin-top: 30px; font-size: 0.8em; color: #666;">
    © 2023 Source Analysis System Project • All Rights Reserved
  </p>
</div> 
