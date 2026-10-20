\# AI Usage Documentation

I used Claude (Claude Code) throughout this assignment: to explain the lecture material, to plan the  
work against the assignment requirements, to generate code for specific parts, to check ideas about the  
data and the validation, to interpret plots, and to finish the report. Text cells in the model and  
ensemble notebooks were generated or edited with Claude; texts in the EDA and validation notebooks were  
written by me and corrected for grammar with Claude. I can't provide a link to the chat, since Claude  
was used on a corporate Team plan and chat links can't be generated. Instead, below is a day-by-day log  
of how it was used.

\#\# 2026-10-17/18 — Theory, assignment breakdown and EDA

\- Claude explained the lecture notebook (\`Old\_Good\_CNNs\`): image representation and color spaces,  
  convolution and the LoG kernel, impulse response, multichannel convolution, pooling, receptive field,  
  translation equivariance, inductive bias, AlexNet and transfer learning, and BatchNorm vs LayerNorm.  
\- It broke the assignment PDF into concrete steps and listed which theoretical questions we had  
  already covered.  
\- It helped set up data loading in Colab with \`kagglehub\` and Colab Secrets.  
\- It proposed the EDA checklist (label balance, labels per photo, empty photos, rare pets) and reviewed  
  my \`CNN\_eda\` notebook.  
\- For the metric analysis, it explained how F1 macro is computed (macro vs micro), suggested the edge  
  cases (threshold, rare labels, the "all ones" baseline ≈ 0.24) and PR-AUC as an alternative metric.

\#\# 2026-10-19 — Validation and CNN setup

\- Claude proposed checking the time factor through EXIF metadata and wrote the check (no EXIF was found).  
\- It wrote the duplicate search: MD5 for exact copies and perceptual hash with Hamming distance for  
  photo series, and explained how to read the distance distribution. We also discussed embeddings  
  with FAISS as an alternative.  
\- It explained the candidate schemes (\`MultilabelStratifiedKFold\` vs \`StratifiedGroupKFold\`) and how to  
  decide between them; the final choice and its motivation in \`CNN\_val\` are mine.

\#\# 2026-10-20 — Experiments, own block, health checks, ensemble and report

\- Claude wrote the experiment and submission helpers and the ReduceLROnPlateau option, and helped plan  
  the minimal set of experiments (optimizer, scheduler, learning rate).

\- It helped compare CV with the Public LB for all submissions.  
\- It cleaned up the model notebook   
\- It helped with the report: a draft structure with tables, then filling the remaining sections  
  (ensemble results, Kaggle results, AI usage) and re-rendering the final PDF.  
