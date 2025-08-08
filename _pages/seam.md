---
permalink: /seam/
title: "SEAM: Semantically Equivalent Across Modalities Benchmark"
excerpt: "A rigorous comparative assessment of textual-symbolic and visual-spatial reasoning capabilities in Vision-Language Models"
author_profile: true
---

<div style="text-align: center; margin-bottom: 30px;">
  <h1 style="color: #667eea; margin-bottom: 10px;">SEAM</h1>
  <h2 style="font-size: 1.3em; font-weight: 400; color: #666; margin-bottom: 15px;">Semantically Equivalent Across Modalities Benchmark for Vision-Language Models</h2>
  <p style="font-size: 1.1em; color: #777; margin-bottom: 15px; max-width: 600px; margin-left: auto; margin-right: auto;">A rigorous comparative assessment of textual-symbolic and visual-spatial reasoning capabilities in VLMs</p>
  
  <p style="margin-bottom: 20px; color: #555;">
    <strong>Authors:</strong> Zhenwei Tang¹, Difan Jiao¹, Blair Yang¹'², Ashton Anderson¹<br>
    <span style="font-size: 0.9em;">¹University of Toronto, ²Coolwei AI Lab</span>
  </p>
  
  <div style="display: flex; gap: 15px; justify-content: center; flex-wrap: wrap; margin-bottom: 30px;">
    <a href="/files/colm2025_conference.pdf" class="btn btn--primary" target="_blank">📄 Read Paper</a>
    <a href="https://github.com/CSSLab/SEAM" class="btn btn--inverse" target="_blank">💻 View Code</a>
    <a href="#citation" class="btn btn--inverse">📝 Cite</a>
  </div>
</div>

## Abstract

Evaluating whether vision–language models (VLMs) reason consistently across representations is challenging because modality comparisons are typically confounded by task differences and asymmetric information. We introduce **SEAM**, a benchmark that pairs semantically equivalent inputs across four domains with existing standardized textual and visual notations. By employing distinct notation systems across modalities, in contrast to OCR-based image-text pairing, SEAM provides a rigorous comparative assessment of the textual-symbolic and visual-spatial reasoning capabilities of VLMs.

Across 16 contemporary models, we observe systematic modality imbalance: vision frequently lags language in overall performance, despite the problems containing semantically equivalent information, and cross-modal agreement is relatively low. Our error analysis reveals two main drivers: textual perception failures from tokenization in domain notations and visual perception failures that induce hallucinations. We also show that our results are largely robust to visual transformations. SEAM establishes a controlled, semantically equivalent setting for measuring and improving modality-agnostic reasoning.

## Benchmark Overview

<div style="text-align: center; margin: 30px 0;">
  <object data="/images/seam-overview.pdf" type="application/pdf" width="100%" height="400" style="border: 1px solid #ddd; border-radius: 8px;">
    <p style="text-align: center; padding: 20px;">
      <a href="/images/seam-overview.pdf">View SEAM Overview Diagram (PDF)</a>
    </p>
  </object>
  <p style="font-size: 0.9em; color: #666; margin-top: 10px;"><strong>Figure 1:</strong> SEAM includes 16 tasks across chess, chemistry, music, and graph theory domains with paired visual-spatial and textual-symbolic representations that are semantically equivalent.</p>
</div>

## Key Design Principles

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin: 30px 0;">
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px;">
    <h3 style="color: #667eea; margin-bottom: 15px;">📋 Standardized Notation</h3>
    <p>Leverages domains with well-established standardized notation systems in both visual and textual modalities:</p>
    <ul style="margin-top: 10px;">
      <li><strong>Chess:</strong> Board images ↔ FEN strings</li>
      <li><strong>Chemistry:</strong> Structural diagrams ↔ SMILES strings</li>
      <li><strong>Music:</strong> Staff notation ↔ ABC notation</li>
      <li><strong>Graph Theory:</strong> Node-edge diagrams ↔ Adjacency matrices</li>
    </ul>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px;">
    <h3 style="color: #667eea; margin-bottom: 15px;">🔧 Tool Availability</h3>
    <p>Built using robust conversion tools ensuring semantic equivalence:</p>
    <ul style="margin-top: 10px;">
      <li><strong>python-chess:</strong> FEN ↔ Chess boards</li>
      <li><strong>RDKit:</strong> SMILES ↔ Molecular diagrams</li>
      <li><strong>Music21:</strong> ABC ↔ Staff notation</li>
      <li><strong>NetworkX:</strong> Matrices ↔ Graph visualizations</li>
    </ul>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px;">
    <h3 style="color: #667eea; margin-bottom: 15px;">🏗️ Self-Contained Tasks</h3>
    <p>Every problem can be fully solved using only its textual representation OR only its visual representation, eliminating confounding factors from joint inference.</p>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px;">
    <h3 style="color: #667eea; margin-bottom: 15px;">🎯 Calibrated Difficulty</h3>
    <p><strong>3,200 total questions</strong> (16 tasks × 200 questions) with carefully constructed distractors to avoid random guessing while enabling meaningful cross-modal comparison.</p>
  </div>
</div>

## Main Results

### Performance Leaderboard

<div style="overflow-x: auto; margin: 30px 0;">
<table style="width: 100%; border-collapse: collapse; margin: 20px 0; font-size: 0.9em;">
<thead>
<tr style="background-color: #f8f9fa;">
<th style="padding: 12px; border: 1px solid #ddd; text-align: left;"><strong>Model</strong></th>
<th style="padding: 12px; border: 1px solid #ddd; text-align: center;">Language</th>
<th style="padding: 12px; border: 1px solid #ddd; text-align: center;">Vision</th>
<th style="padding: 12px; border: 1px solid #ddd; text-align: center;">Vision-Lang</th>
<th style="padding: 12px; border: 1px solid #ddd; text-align: center;">Average</th>
<th style="padding: 12px; border: 1px solid #ddd; text-align: center; background: #e9ecef;"><strong>L-V Agreement ↓</strong></th>
</tr>
</thead>
<tbody>
<tr style="background-color: #f8f9fa;"><td colspan="6" style="padding: 8px; border: 1px solid #ddd; font-style: italic;"><em>Proprietary Models</em></td></tr>
<tr>
<td style="padding: 8px; border: 1px solid #ddd;"><strong>Claude-3.7 Sonnet</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.745</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.590</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.688</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.674</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center; background: #e9ecef;"><strong>0.584</strong></td>
</tr>
<tr>
<td style="padding: 8px; border: 1px solid #ddd;">Claude-3.5 Sonnet</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.665</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.560</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.514</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.580</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center; background: #e9ecef;">0.537</td>
</tr>
<tr>
<td style="padding: 8px; border: 1px solid #ddd;">GPT-4o</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.635</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.482</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.627</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.581</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center; background: #e9ecef;">0.503</td>
</tr>
<tr style="background-color: #f8f9fa;"><td colspan="6" style="padding: 8px; border: 1px solid #ddd; font-style: italic;"><em>Open-Source Models (Top 3)</em></td></tr>
<tr>
<td style="padding: 8px; border: 1px solid #ddd;"><strong>Qwen2.5-VL-72B</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.547</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.475</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.519</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;"><strong>0.514</strong></td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center; background: #e9ecef;"><strong>0.447</strong></td>
</tr>
<tr>
<td style="padding: 8px; border: 1px solid #ddd;">InternVL3-78B</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.525</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.427</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.482</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.478</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center; background: #e9ecef;">0.447</td>
</tr>
<tr>
<td style="padding: 8px; border: 1px solid #ddd;">gemma-3-27b-it</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.516</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.428</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.450</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center;">0.465</td>
<td style="padding: 8px; border: 1px solid #ddd; text-align: center; background: #e9ecef;">0.447</td>
</tr>
</tbody>
</table>
</div>

### Key Findings

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 30px 0;">
  <div style="background: white; border: 1px solid #e1e5e9; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
    <img src="/images/seam-results.png" alt="Accuracy-Agreement Correlation" style="width: 100%; height: 250px; object-fit: cover;" />
    <div style="padding: 15px;">
      <h4 style="color: #667eea; margin-bottom: 10px;">Accuracy-Agreement Correlation</h4>
      <p style="font-size: 0.9em; color: #666; margin: 0;">Strong positive correlation between cross-modal agreement and overall accuracy, but most models cluster near random baseline rather than ideal agreement.</p>
    </div>
  </div>
  
  <div style="background: white; border: 1px solid #e1e5e9; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
    <object data="/images/seam-heatmap.pdf" type="application/pdf" width="100%" height="250" style="border: none;">
      <div style="padding: 15px; text-align: center; height: 250px; display: flex; align-items: center; justify-content: center;">
        <p style="font-style: italic; color: #666;">Domain-specific performance heatmap. <a href="/images/seam-heatmap.pdf">View PDF</a></p>
      </div>
    </object>
    <div style="padding: 15px;">
      <h4 style="color: #667eea; margin-bottom: 10px;">Domain-Specific Imbalances</h4>
      <p style="font-size: 0.9em; color: #666; margin: 0;">Modality imbalance varies significantly by domain. Graph tasks show the largest vision-language gaps.</p>
    </div>
  </div>
  
  <div style="background: white; border: 1px solid #e1e5e9; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
    <img src="/images/seam-grid.png" alt="SEAM Examples" style="width: 100%; height: 250px; object-fit: cover;" />
    <div style="padding: 15px;">
      <h4 style="color: #667eea; margin-bottom: 10px;">Benchmark Examples</h4>
      <p style="font-size: 0.9em; color: #666; margin: 0;">Examples across all four domains showing semantically equivalent representations in textual-symbolic and visual-spatial formats.</p>
    </div>
  </div>
</div>

## Error Analysis

Our comprehensive error analysis reveals two primary failure modes:

### 1. Textual Perception Failures
**Tokenization Issues in Domain-Specific Notations:**
- **SMILES strings** like `COC(=O)C(OC(C)(C)C)c1cc([N+](=O)[O-])ccc1-c1ccc2c(c1)CCCO2` are incorrectly segmented into meaningless subwords
- **Chess FEN notation** suffers from poor tokenization where `PP` (two pawns) should be two `P` tokens but becomes one `PP` token
- **Music ABC notation** exhibits fewer issues due to abundant punctuation providing clearer boundaries

### 2. Visual Perception Failures
**Image Patch Processing Issues:**
- **Graph tasks** particularly affected when edges are cut near intersections during ViT patch processing
- **Hallucinations** occur at patch boundaries, especially affecting edge and node recognition
- **Structural information** lost when spatial relationships are divided across patches

## Robustness Analysis

We validated that our findings are robust to various visual transformations, confirming the reliability of cross-modal comparisons and demonstrating that the observed modality imbalances are not artifacts of specific rendering choices.

## Impact & Applications

**SEAM enables:**
- **Fair evaluation** of cross-modal reasoning capabilities
- **Identification** of specific failure modes in current VLMs  
- **Benchmarking progress** toward modality-agnostic reasoning
- **Guidance** for improving tokenization and visual processing in VLMs

**Real-world relevance** across domains where experts routinely switch between visual and textual representations, from chess analysis platforms to chemical databases.

## Future Directions

- **Improved tokenization** strategies for domain-specific notations
- **Enhanced visual processing** methods that preserve spatial relationships  
- **Cross-modal alignment** techniques for unified representations
- **Domain-specific VLM training** approaches

## Resources

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 30px 0;">
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #2d3748; margin-bottom: 15px;">📖 Paper</h3>
    <p style="margin-bottom: 15px;">CoLM 2025 conference paper with full methodology and results</p>
    <a href="/files/colm2025_conference.pdf" class="btn btn--primary" target="_blank">Download PDF</a>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #2d3748; margin-bottom: 15px;">💾 Code & Data</h3>
    <p style="margin-bottom: 15px;">Complete benchmark dataset, evaluation code, and reproducibility instructions</p>
    <a href="https://github.com/CSSLab/SEAM" class="btn btn--primary" target="_blank">GitHub Repository</a>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #2d3748; margin-bottom: 15px;">📊 Leaderboard</h3>
    <p style="margin-bottom: 15px;">Submit your model's results to our community leaderboard</p>
    <a href="https://github.com/CSSLab/SEAM#leaderboard" class="btn btn--primary" target="_blank">Submit Results</a>
  </div>
</div>

## Citation {#citation}

If you use SEAM in your research, please cite our paper:

```bibtex
@article{tang2025seam,
    title={SEAM: Semantically Equivalent Across Modalities Benchmark for Vision-Language Models},
    author={Tang, Zhenwei and Jiao, Difan and Yang, Blair and Anderson, Ashton},
    journal={Conference on Language Modeling (CoLM)},
    year={2025}
}
```

<div style="text-align: center; margin-top: 30px;">
  <button class="btn btn--primary" onclick="copyBibtex()" style="cursor: pointer;">📋 Copy BibTeX Citation</button>
</div>

---

<div style="background: #f8f9fa; padding: 20px; border-radius: 8px; margin: 30px 0;">
<p style="text-align: center; margin: 0; color: #666;">
<strong>Questions or collaborations?</strong> Reach out to <a href="mailto:josephtang@cs.toronto.edu">josephtang@cs.toronto.edu</a>
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