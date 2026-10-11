---
name: cyber-mentor
description: Review and polish academic papers or research project reports in two passes, first revising individual paragraphs and then checking document-wide logic and transitions. Deliver a complete revised manuscript as a separate file while preserving the original.
---

# Cyber Mentor

Complete two passes of review and revision across an entire academic paper or research project report. Make the argument accurate, coherent, and natural while preserving the author's research content and confirmed wording. Paragraph-by-paragraph review is an internal working method; the final deliverable is a complete revised manuscript.

## Scope and evidence

- Adapt the writing to the document's purpose and audience. Follow the relevant academic writing requirements for papers and the project's existing structure and delivery requirements for research reports. Do not impose a paper structure or journal style on a project report.
- Review and polish the entire document by default. First understand its overall structure, then examine headings, paragraph roles, and figure and table content, paragraph by paragraph within each section.
- Follow the user's current instructions and existing project conventions. If the user explicitly limits the task to a section or issue, work only within that scope.
- Identify the authoritative manuscript in the project. Do not assume that Word, LaTeX, and preview versions are equally authoritative. Ask when uncertainty about the file or section would affect the result.
- When discussing method behavior, experimental results, or metric definitions, check the relevant implementation, configuration, tables, or definitions as needed. Identify specific evidence gaps; do not invent data, references, or causal explanations.

## Workflow

### First pass: review, revise, and polish each paragraph

Read and apply the complete [Paper Writing Prompt](references/paper-writing.md) directly. Review, revise, and polish every paragraph in the original order, applying the revisions to a working copy. Use all requirements in that prompt as the review criteria for this pass; do not replace them with a shortened checklist.

For the prompt's humanizer requirement, use the bundled [English Humanizer](references/humanizer/SKILL.md). Read it in full and apply it as an embedded editing guide, without relying on an external installation. Preserve research accuracy and make the smallest necessary changes. Do not add facts or deliberately alter the writing style merely to remove formulaic language. Follow this workflow for file edits and output: edit only the working copy and deliver a complete revised manuscript.

Finish every paragraph before starting the second pass. Produce revised text rather than only suggestions. Do not stop after each paragraph or section to ask whether to continue or wait for approval.

### Second pass: review document-wide logic and paragraph transitions

Review the complete manuscript produced in the first pass, focusing on relationships between paragraphs and sections. Apply necessary revisions to the working copy:

- Check whether adjacent paragraphs connect naturally, and identify gaps in reasoning, abrupt changes of subject, repeated arguments, or contradictions.
- Check section progression and paragraph roles, and ensure that headings, research objectives, methods, results, and conclusions align.
- Keep terminology and the scope of claims consistent. Build transitions through meaningful content relationships rather than mechanically adding transition words or summary sentences.
- Make the smallest adjustments needed. Merge, split, or move paragraphs only to improve the logic, without adding unsupported facts or conclusions.

After the second pass, confirm that the entire scope has been covered, that revisions preserve scientific meaning, and that equations, citations, numbering, and references to figures and tables remain consistent.

### Delivery: generate a separate revised manuscript

- Save the complete manuscript revised in both passes as a separate new file. Do not edit the original directly or overwrite existing user files. By default, keep the original format and add `reviewed` and a timestamp to the filename. Follow any output location or filename specified by the user.
- Include all text and all equations, citations, figures, tables, and other content that should be preserved. Do not substitute a review report, change list, a few examples, or ellipses for the complete manuscript.
- Preserve the manuscript's language. Provide an absolute-path link to the new file, the scope completed in both passes, and a brief account of the main revisions. Include original/revised comparisons only when requested; they are not the default primary deliverable.
- Finish the task only after both passes are complete and the new manuscript has been generated and checked. If missing material genuinely prevents further work, state the completed scope and the specific blocker rather than claiming that the whole document is complete.
- Use the document-handling workflow appropriate to the manuscript format, and check the new manuscript's structure and essential content. Compile, render, or convert formats according to the user's instructions and the project's established delivery process. Report actual validation results, distinguishing successful PDF generation from completeness of citations and cross-references.
