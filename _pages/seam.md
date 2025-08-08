---
permalink: /seam/
title: "SEAM: Semantically Equivalent Across Modalities Benchmark"
excerpt: "A rigorous comparative assessment of textual-symbolic and visual-spatial reasoning capabilities in Vision-Language Models"
author_profile: true
---

<div style="text-align: center; margin-bottom: 30px;">
  <h1 style="color: #667eea; margin-bottom: 10px;">SEAM</h1>
  <h2 style="font-size: 1.3em; font-weight: 400; color: #666; margin-bottom: 15px;">Semantically Equivalent Across Modalities Benchmark for Vision-Language Models</h2>
  <p style="font-size: 1.1em; color: #777; margin-bottom: 20px; max-width: 600px; margin-left: auto; margin-right: auto;">A rigorous comparative assessment of textual-symbolic and visual-spatial reasoning capabilities in VLMs</p>
  
  <div style="display: flex; gap: 15px; justify-content: center; flex-wrap: wrap; margin-bottom: 30px;">
    <a href="/files/colm2025_conference.pdf" class="btn btn--primary" target="_blank">📄 Read Paper</a>
    <a href="https://github.com/CSSLab/SEAM" class="btn btn--inverse" target="_blank">💻 View Code</a>
  </div>
</div>

## Abstract

Evaluating whether vision–language models (VLMs) reason consistently across representations is challenging because modality comparisons are typically confounded by task differences and asymmetric information. We introduce **SEAM**, a benchmark that pairs semantically equivalent inputs across four domains with existing standardized textual and visual notations. By employing distinct notation systems across modalities, in contrast to OCR-based image-text pairing, SEAM provides a rigorous comparative assessment of the textual-symbolic and visual-spatial reasoning capabilities of VLMs.

Across 16 contemporary models, we observe systematic modality imbalance: vision frequently lags language in overall performance, despite the problems containing semantically equivalent information, and cross-modal agreement is relatively low. Our error analysis reveals two main drivers: textual perception failures from tokenization in domain notations and visual perception failures that induce hallucinations. We also show that our results are largely robust to visual transformations. SEAM establishes a controlled, semantically equivalent setting for measuring and improving modality-agnostic reasoning.

## Key Features

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 30px 0;">
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #667eea; margin-bottom: 10px;">🎯 Four Domains</h3>
    <p>SEAM covers four key domains with standardized notations across text and visual modalities</p>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #667eea; margin-bottom: 10px;">🤖 16 Models Evaluated</h3>
    <p>Comprehensive evaluation across contemporary vision-language models</p>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #667eea; margin-bottom: 10px;">⚖️ Semantic Equivalence</h3>
    <p>True cross-modal comparison with semantically equivalent inputs</p>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #667eea; margin-bottom: 10px;">🔍 Error Analysis</h3>
    <p>Detailed analysis of textual perception and visual perception failures</p>
  </div>
</div>

## Key Findings & Visualizations

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 30px 0;">
  <div style="background: white; border: 1px solid #e1e5e9; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
    <img src="/images/seam-grid.png" alt="SEAM Grid Overview" style="width: 100%; height: 200px; object-fit: cover;" />
    <div style="padding: 15px;">
      <p style="font-size: 0.9em; color: #666; text-align: center; margin: 0;">SEAM benchmark grid showing examples across different domains and modalities</p>
    </div>
  </div>
  
  <div style="background: white; border: 1px solid #e1e5e9; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
    <img src="/images/seam-results.png" alt="SEAM Results" style="width: 100%; height: 200px; object-fit: cover;" />
    <div style="padding: 15px;">
      <p style="font-size: 0.9em; color: #666; text-align: center; margin: 0;">Performance results showing systematic modality imbalances across models</p>
    </div>
  </div>
  
  <div style="background: white; border: 1px solid #e1e5e9; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
    <object data="/images/seam-heatmap.pdf" type="application/pdf" width="100%" height="200" style="border: none;">
      <div style="padding: 15px; text-align: center;">
        <p style="font-style: italic; color: #666;">Performance comparison heatmap. <a href="/images/seam-heatmap.pdf">View PDF</a></p>
      </div>
    </object>
    <div style="padding: 15px;">
      <p style="font-size: 0.9em; color: #666; text-align: center; margin: 0;">Performance comparison across models and modalities</p>
    </div>
  </div>
</div>

## Main Contributions

1. **Novel Benchmark Design**: SEAM introduces the first benchmark for evaluating vision-language models with truly semantically equivalent inputs across modalities, eliminating confounds from task differences and information asymmetries.

2. **Systematic Modality Analysis**: Through evaluation of 16 contemporary models, we reveal systematic modality imbalances where vision consistently underperforms language despite semantic equivalence.

3. **Error Characterization**: Our detailed error analysis identifies two primary failure modes: textual perception failures from domain-specific tokenization and visual perception failures leading to hallucinations.

4. **Robustness Validation**: We demonstrate that our findings are robust to various visual transformations, confirming the reliability of cross-modal comparisons.

## Citation

If you use SEAM in your research, please cite our paper:

```bibtex
@article{seam2025,
    title={SEAM: Semantically Equivalent Across Modalities Benchmark for Vision-Language Models},
    author={[Author Names]},
    journal={Conference on Language Modeling (CoLM)},
    year={2025}
}
```

## Resources

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 30px 0;">
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #2d3748; margin-bottom: 15px;">📖 Paper</h3>
    <p style="margin-bottom: 15px;">Read the full paper with detailed methodology and results</p>
    <a href="/files/colm2025_conference.pdf" class="btn btn--primary" target="_blank">Download PDF</a>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #2d3748; margin-bottom: 15px;">💾 Code & Data</h3>
    <p style="margin-bottom: 15px;">Access the benchmark dataset and evaluation code</p>
    <a href="https://github.com/CSSLab/SEAM" class="btn btn--primary" target="_blank">GitHub Repository</a>
  </div>
  
  <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; text-align: center;">
    <h3 style="color: #2d3748; margin-bottom: 15px;">📝 BibTeX</h3>
    <p style="margin-bottom: 15px;">Citation for your research</p>
    <button class="btn btn--primary" onclick="copyBibtex()" style="cursor: pointer;">Copy Citation</button>
  </div>
</div>

<script>
function copyBibtex() {
    const bibtex = `@article{seam2025,
    title={SEAM: Semantically Equivalent Across Modalities Benchmark for Vision-Language Models},
    author={[Author Names]},
    journal={Conference on Language Modeling (CoLM)},
    year={2025}
}`;
    navigator.clipboard.writeText(bibtex).then(function() {
        alert('BibTeX citation copied to clipboard!');
    }).catch(function(err) {
        console.error('Could not copy text: ', err);
        // Fallback for older browsers
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