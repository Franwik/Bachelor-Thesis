# Thesis Project: Database a grafo distribuiti a supporto di approcci di Conversational AI

**Candidate:** Francesco Donnarumma  
**Supervisor:** Prof. Antonio Origlia  
**Academic Year:** 2025–2026  
**Institution:** Università degli Studi di Napoli Federico II

---

## Abstract
This thesis presents an advanced architectural framework for Conversational AI systems leveraging the **Retrieval-Augmented Generation (RAG)** paradigm combined with distributed graph databases. The primary objective is to mitigate common LLM limitations, such as "hallucinations" and knowledge cutoff, by providing a verifiable external "source of truth".

The proposed system utilizes a two-tier data management strategy: a **Global Remote Storage** for long-term knowledge and a **Local Shard** acting as a high-performance cache to minimize retrieval latency. By employing **Neo4j** and hybrid vector-graph search techniques, the system enables efficient navigation of complex relationships within medical datasets. The integration includes a sophisticated synchronization logic driven by parameterized Cypher queries and a Least Frequently Used (LFU) eviction policy. The final prototype, built with **Unreal Engine** and the **FANTASIA** framework, incorporates **Whisper** for ASR and **ElevenLabs** for TTS, creating a seamless voice-driven interaction. Experimental analysis confirms that the distributed approach yields a substantial reduction in end-to-end latency, validating its effectiveness for real-time applications.

---

## Requirements for Local Compilation

To compile this thesis locally, you will need a LaTeX distribution such as **TeX Live**, **MiKTeX**, or **MacTeX**. The project relies on a custom class (`uninathesis.cls`) and a frontispiece package (`uninafrontespizio.sty`).

### 1. Required LaTeX Packages
The following packages must be installed in your LaTeX environment:

* **Document Structure & Layout:** `geometry`, `fontenc`, `microtype`, `titlesec`, `babel`, `inputenc`, `csquotes`.
* **Fonts (Libertine):** `libertine`, `lmodern`, `newtxmath`, `textcomp`.
* **Mathematics:** `mathtools`, `mathrsfs`, `amsthm`, `stmaryrd`.
* **Graphics & Styling:** `tikz`, `pgfplots`, `graphicx`, `caption`, `subcaption`, `booktabs`, `multirow`, `makecell`.
* **Algorithms & Code:** `listings`, `lstautogobble`, `algorithm`, `algpseudocode`.
* **Bibliography:** `biblatex` (with `biber` backend).
* **Utilities:** `hyperref`, `xcolor`, `calc`, `enumitem`, `lineno`, `xspace`, `etoolbox`, `setspace`, `todonotes`, `etoc`, `changepage`, `fullwidth`, `marvosym`.

### 2. Compilation Instructions
Because the project uses `biblatex` for references, you must follow a specific compilation sequence:

1.  `pdflatex thesis.tex`
2.  `biber thesis`
3.  `pdflatex thesis.tex`
4.  `pdflatex thesis.tex`

---

## Project Structure

* `thesis.tex`: The main LaTeX file containing the document structure and chapter inclusions.
* `uninathesis.cls`: The document class defining the layout, headers, and custom environments.
* `uninafrontespizio.sty`: A package specifically for generating the Federico II University front page.
* `_chapters/`: Directory containing the individual chapter `.tex` files.
* `_bib/`: Contains the `bibliography.bib` file for references.
* `logo-federico-II.pdf`: The University logo required for the frontispiece.

---

## Features
* **Cypher Highlighting:** Includes a custom `listings` definition for the Cypher query language.
* **Multiple Typefaces:** Supports options for Libertine (default), Palatino, Mathpazo, and Alegreya.
* **Frontispiece:** Automates the creation of the official University of Naples Federico II cover page.
