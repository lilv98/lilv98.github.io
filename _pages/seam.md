---
permalink: /seam/
title: "SEAM: Semantically Equivalent Across Modalities"
excerpt: "A rigorous benchmark for evaluating vision-language models across semantically equivalent textual and visual representations"
author_profile: true
classes: wide
---

<style>
.hero-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 60px 20px;
  text-align: center;
  margin: -20px -20px 40px -20px;
  border-radius: 0 0 20px 20px;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
}

.hero-subtitle {
  font-size: 1.4rem;
  margin-bottom: 1rem;
  opacity: 0.9;
}

.hero-description {
  font-size: 1.1rem;
  margin-bottom: 2rem;
  opacity: 0.8;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

.hero-buttons {
  display: flex;
  gap: 15px;
  justify-content: center;
  flex-wrap: wrap;
}

.btn-hero {
  padding: 12px 24px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  display: inline-block;
}

.btn-hero.primary {
  background: rgba(255,255,255,0.2);
  border: 2px solid white;
  color: white;
}

.btn-hero.primary:hover {
  background: white;
  color: #667eea;
  transform: translateY(-2px);
}

.btn-hero.secondary {
  background: transparent;
  border: 2px solid rgba(255,255,255,0.5);
  color: white;
}

.btn-hero.secondary:hover {
  background: rgba(255,255,255,0.1);
  border-color: white;
  transform: translateY(-2px);
}

.news-section {
  background: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
  margin-bottom: 30px;
  border-left: 4px solid #667eea;
}

.news-title {
  font-size: 1.3rem;
  font-weight: 600;
  color: #333;
  margin-bottom: 15px;
}

.news-item {
  margin-bottom: 10px;
  padding: 8px 0;
}

.news-date {
  font-weight: 600;
  color: #667eea;
}

.section-title {
  font-size: 2.2rem;
  font-weight: 600;
  margin: 40px 0 20px 0;
  color: #333;
  border-bottom: 3px solid #667eea;
  padding-bottom: 10px;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.stat-card {
  background: white;
  padding: 25px;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  border-top: 4px solid #667eea;
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  color: #667eea;
  display: block;
}

.stat-label {
  font-size: 1rem;
  color: #666;
  margin-top: 5px;
}

.domain-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.domain-card {
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.domain-card:hover {
  transform: translateY(-5px);
}

.domain-icon {
  font-size: 2.5rem;
  margin-bottom: 15px;
  display: block;
}

.domain-title {
  font-size: 1.3rem;
  font-weight: 600;
  margin-bottom: 10px;
  color: #333;
}

.domain-desc {
  color: #666;
  font-size: 0.95rem;
}

.leaderboard {
  background: white;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  margin: 30px 0;
}

.leaderboard-header {
  background: #667eea;
  color: white;
  padding: 20px;
  font-size: 1.2rem;
  font-weight: 600;
}

.leaderboard-table {
  width: 100%;
  border-collapse: collapse;
}

.leaderboard-table th,
.leaderboard-table td {
  padding: 12px 15px;
  text-align: center;
  border-bottom: 1px solid #eee;
}

.leaderboard-table th {
  background: #f8f9fa;
  font-weight: 600;
  color: #333;
}

.leaderboard-table .model-name {
  text-align: left;
  font-weight: 600;
}

.leaderboard-table .top-performance {
  background: #e8f5e8;
  color: #2d5a2d;
  font-weight: 600;
}

.results-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 30px;
  margin: 30px 0;
}

.result-card {
  background: white;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.result-image {
  width: 100%;
  height: 250px;
  object-fit: cover;
}

.result-content {
  padding: 20px;
}

.result-title {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 10px;
  color: #333;
}

.result-desc {
  color: #666;
  line-height: 1.5;
}

.author-section {
  background: #f8f9fa;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  margin: 40px 0;
}

.authors {
  font-size: 1.2rem;
  margin-bottom: 10px;
}

.affiliations {
  color: #666;
  font-size: 1rem;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }
  .stats-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .domain-grid {
    grid-template-columns: 1fr;
  }
  .results-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="hero-section">
  <h1 class="hero-title">SEAM</h1>
  <h2 class="hero-subtitle">Semantically Equivalent Across Modalities</h2>
  <p class="hero-description">
    A rigorous benchmark for evaluating vision-language models across semantically equivalent textual-symbolic and visual-spatial representations
  </p>
  <div class="hero-buttons">
    <a href="/files/colm2025_conference.pdf" class="btn-hero primary" target="_blank">📄 Paper</a>
    <a href="https://github.com/CSSLab/SEAM" class="btn-hero secondary" target="_blank">💻 GitHub</a>
    <a href="https://huggingface.co/datasets/CSSLab/SEAM" class="btn-hero secondary" target="_blank">🤗 Dataset</a>
    <a href="#leaderboard" class="btn-hero secondary">📊 Leaderboard</a>
  </div>
</div>

<div class="author-section">
  <div class="authors">
    <strong>Zhenwei Tang¹</strong>, <strong>Difan Jiao¹</strong>, <strong>Blair Yang¹'²</strong>, <strong>Ashton Anderson¹</strong>
  </div>
  <div class="affiliations">
    ¹University of Toronto &nbsp;&nbsp; ²Coolwei AI Lab
  </div>
</div>

<div class="news-section">
  <div class="news-title">📢 News</div>
  <div class="news-item">
    <span class="news-date">[2025-01]</span> SEAM paper accepted to CoLM 2025!
  </div>
  <div class="news-item">
    <span class="news-date">[2025-01]</span> Dataset and evaluation code released on GitHub and HuggingFace.
  </div>
  <div class="news-item">
    <span class="news-date">[2024-12]</span> Comprehensive evaluation of 16 state-of-the-art VLMs completed.
  </div>
</div>

## Overview

Vision-Language Models (VLMs) have made rapid progress, but a fundamental question remains: **Do they reason consistently across semantically equivalent representations?** Existing benchmarks typically confound modality comparisons with task differences and asymmetric information content.

**SEAM** addresses this challenge by providing the first benchmark with truly semantically equivalent inputs across modalities. By leveraging standardized notation systems in four domains, SEAM enables rigorous comparative assessment of textual-symbolic versus visual-spatial reasoning capabilities.

<div class="stats-grid">
  <div class="stat-card">
    <span class="stat-number">4</span>
    <div class="stat-label">Domains</div>
  </div>
  <div class="stat-card">
    <span class="stat-number">16</span>
    <div class="stat-label">Tasks</div>
  </div>
  <div class="stat-card">
    <span class="stat-number">3,200</span>
    <div class="stat-label">Questions</div>
  </div>
  <div class="stat-card">
    <span class="stat-number">16</span>
    <div class="stat-label">Models Evaluated</div>
  </div>
</div>

<h2 class="section-title">Benchmark Domains</h2>

<div class="domain-grid">
  <div class="domain-card">
    <span class="domain-icon">♟️</span>
    <div class="domain-title">Chess</div>
    <div class="domain-desc">
      <strong>Visual:</strong> Board positions<br>
      <strong>Textual:</strong> FEN notation<br>
      Tasks include position evaluation, legal moves, tactical analysis
    </div>
  </div>
  
  <div class="domain-card">
    <span class="domain-icon">🧪</span>
    <div class="domain-title">Chemistry</div>
    <div class="domain-desc">
      <strong>Visual:</strong> Structural diagrams<br>
      <strong>Textual:</strong> SMILES strings<br>
      Tasks include molecular property prediction, compound identification
    </div>
  </div>
  
  <div class="domain-card">
    <span class="domain-icon">🎵</span>
    <div class="domain-title">Music</div>
    <div class="domain-desc">
      <strong>Visual:</strong> Staff notation<br>
      <strong>Textual:</strong> ABC notation<br>
      Tasks include key signature, time signature, musical form analysis
    </div>
  </div>
  
  <div class="domain-card">
    <span class="domain-icon">🕸️</span>
    <div class="domain-title">Graph Theory</div>
    <div class="domain-desc">
      <strong>Visual:</strong> Node-edge diagrams<br>
      <strong>Textual:</strong> Adjacency matrices<br>
      Tasks include traversal, connectivity, shortest path analysis
    </div>
  </div>
</div>

<h2 class="section-title" id="leaderboard">Leaderboard</h2>

<div class="leaderboard">
  <div class="leaderboard-header">
    Model Performance on SEAM Benchmark
  </div>
  <div style="overflow-x: auto;">
    <table class="leaderboard-table">
      <thead>
        <tr>
          <th style="text-align: left;">Model</th>
          <th>Language</th>
          <th>Vision</th>
          <th>Vision-Lang</th>
          <th>Average</th>
          <th>L-V Agreement</th>
        </tr>
      </thead>
      <tbody>
        <tr style="background: #f0f8ff;">
          <td colspan="6" style="font-weight: 600; text-align: center; padding: 15px;">
            🏆 Proprietary Models
          </td>
        </tr>
        <tr>
          <td class="model-name top-performance">Claude-3.7 Sonnet</td>
          <td class="top-performance">0.745</td>
          <td class="top-performance">0.590</td>
          <td class="top-performance">0.688</td>
          <td class="top-performance">0.674</td>
          <td class="top-performance">0.584</td>
        </tr>
        <tr>
          <td class="model-name">Claude-3.5 Sonnet</td>
          <td>0.665</td>
          <td>0.560</td>
          <td>0.514</td>
          <td>0.580</td>
          <td>0.537</td>
        </tr>
        <tr>
          <td class="model-name">GPT-4o</td>
          <td>0.635</td>
          <td>0.482</td>
          <td>0.627</td>
          <td>0.581</td>
          <td>0.503</td>
        </tr>
        <tr>
          <td class="model-name">Claude-3.5 Haiku</td>
          <td>0.545</td>
          <td>0.439</td>
          <td>0.509</td>
          <td>0.498</td>
          <td>0.483</td>
        </tr>
        <tr>
          <td class="model-name">GPT-4o-mini</td>
          <td>0.555</td>
          <td>0.411</td>
          <td>0.529</td>
          <td>0.498</td>
          <td>0.480</td>
        </tr>
        <tr style="background: #f0f8ff;">
          <td colspan="6" style="font-weight: 600; text-align: center; padding: 15px;">
            🚀 Open-Source Models
          </td>
        </tr>
        <tr>
          <td class="model-name top-performance">Qwen2.5-VL-72B-Instruct</td>
          <td class="top-performance">0.547</td>
          <td class="top-performance">0.475</td>
          <td class="top-performance">0.519</td>
          <td class="top-performance">0.514</td>
          <td class="top-performance">0.447</td>
        </tr>
        <tr>
          <td class="model-name">InternVL3-78B</td>
          <td>0.525</td>
          <td>0.427</td>
          <td>0.482</td>
          <td>0.478</td>
          <td>0.447</td>
        </tr>
        <tr>
          <td class="model-name">gemma-3-27b-it</td>
          <td>0.516</td>
          <td>0.428</td>
          <td>0.450</td>
          <td>0.465</td>
          <td>0.447</td>
        </tr>
        <tr>
          <td class="model-name">InternVL-2.5-78B</td>
          <td>0.448</td>
          <td>0.414</td>
          <td>0.459</td>
          <td>0.440</td>
          <td>0.415</td>
        </tr>
        <tr>
          <td class="model-name">Llama-3.2-90B-Vision-Instruct</td>
          <td>0.434</td>
          <td>0.384</td>
          <td>0.439</td>
          <td>0.419</td>
          <td>0.384</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div style="background: #fff3cd; padding: 15px; border-radius: 8px; margin: 20px 0; border-left: 4px solid #ffc107;">
  <strong>💡 Key Finding:</strong> All models show systematic modality imbalance with vision consistently underperforming language, despite semantically equivalent information content.
</div>

<h2 class="section-title">Key Results & Analysis</h2>

<div class="results-grid">
  <div class="result-card">
    <img src="/images/seam-results.png" alt="Accuracy-Agreement Analysis" class="result-image" />
    <div class="result-content">
      <div class="result-title">Accuracy-Agreement Correlation</div>
      <div class="result-desc">
        Strong positive correlation between cross-modal agreement and overall accuracy, but most models cluster near random baseline rather than achieving meaningful cross-modal alignment.
      </div>
    </div>
  </div>
  
  <div class="result-card">
    <object data="/images/seam-heatmap.pdf" type="application/pdf" class="result-image" style="border: none;">
      <div class="result-image" style="display: flex; align-items: center; justify-content: center; background: #f8f9fa;">
        <a href="/images/seam-heatmap.pdf" style="color: #667eea;">View Performance Heatmap (PDF)</a>
      </div>
    </object>
    <div class="result-content">
      <div class="result-title">Domain-Specific Performance</div>
      <div class="result-desc">
        Modality imbalance varies significantly across domains. Graph theory shows the largest vision-language performance gaps, while chess shows more balanced performance.
      </div>
    </div>
  </div>
  
  <div class="result-card">
    <img src="/images/seam-grid.png" alt="SEAM Examples" class="result-image" />
    <div class="result-content">
      <div class="result-title">Benchmark Overview</div>
      <div class="result-desc">
        Examples across all four domains demonstrating semantically equivalent representations in textual-symbolic and visual-spatial formats with identical information content.
      </div>
    </div>
  </div>
</div>

<h2 class="section-title">Error Analysis</h2>

Our comprehensive error analysis reveals two primary failure modes across evaluated VLMs:

### 🔤 Textual Perception Failures
**Tokenization Issues in Domain-Specific Notations:**

- **SMILES strings**: Complex molecular representations like `COC(=O)C(OC(C)(C)C)c1cc([N+](=O)[O-])ccc1` are incorrectly segmented into meaningless subwords
- **Chess FEN notation**: Critical positional information suffers from poor tokenization (e.g., `PP` for two pawns becomes one token instead of two)
- **Music ABC notation**: Exhibits fewer issues due to abundant punctuation providing clearer tokenization boundaries

### 👁️ Visual Perception Failures  
**Image Patch Processing Issues:**

- **Graph tasks**: Particularly affected when edges are cut near intersections during Vision Transformer patch processing
- **Hallucinations**: Occur at patch boundaries, especially affecting edge and node recognition in spatial layouts
- **Structural information loss**: Critical spatial relationships divided across patches lose semantic meaning

<div style="background: #e8f4f8; padding: 20px; border-radius: 8px; margin: 20px 0; border-left: 4px solid #17a2b8;">
  <strong>🔍 Robustness Validation:</strong> Our findings remain consistent across various visual transformations, confirming that observed modality imbalances are not artifacts of specific rendering choices.
</div>

<h2 class="section-title">Impact & Applications</h2>

**SEAM enables researchers to:**

- **📊 Fairly evaluate** cross-modal reasoning capabilities without confounding factors
- **🔍 Identify** specific failure modes in current vision-language models
- **📈 Benchmark progress** toward truly modality-agnostic reasoning systems  
- **🛠️ Guide improvements** in tokenization strategies and visual processing methods

**Real-world relevance** spans domains where experts routinely alternate between visual and textual representations, from chess analysis platforms like Chess.com to chemical databases like PubChem.

<h2 class="section-title">Citation</h2>

If you use SEAM in your research, please cite our paper:

```bibtex
@article{tang2025seam,
    title={SEAM: Semantically Equivalent Across Modalities Benchmark for Vision-Language Models},
    author={Tang, Zhenwei and Jiao, Difan and Yang, Blair and Anderson, Ashton},
    journal={Conference on Language Modeling (CoLM)},
    year={2025}
}
```

<div style="text-align: center; margin: 30px 0;">
  <button class="btn-hero primary" onclick="copyBibtex()" style="cursor: pointer; border: none;">📋 Copy BibTeX Citation</button>
</div>

---

<div style="background: #f8f9fa; padding: 30px; border-radius: 10px; text-align: center; margin: 40px 0;">
  <h3 style="margin-bottom: 15px; color: #333;">Questions or Collaborations?</h3>
  <p style="margin: 0; color: #666;">
    Reach out to <a href="mailto:josephtang@cs.toronto.edu" style="color: #667eea; font-weight: 600;">josephtang@cs.toronto.edu</a> for discussions about SEAM or potential collaborations.
  </p>
</div>

<script>
function copyBibtex() {
    const bibtex = `@article{tang2025seam,
    title={SEAM: Semantically Equivalent Across Modalities Benchmark for Vision-Language Models},
    author={Tang, Zhenwei and Jiao, Difan and Yang, Blair and Anderson, Ashton},
    journal={Conference on Language Modeling (CoLM)},
    year={2025}
}`;
    navigator.clipboard.writeText(bibtex).then(function() {
        alert('BibTeX citation copied to clipboard!');
    }).catch(function(err) {
        console.error('Could not copy text: ', err);
        const textArea = document.createElement("textarea");
        textArea.value = bibtex;
        document.body.appendChild(textArea);
        textArea.select();
        document.execCommand('copy');
        document.body.removeChild(textArea);
        alert('BibTeX citation copied to clipboard!');
    });
}
</script>