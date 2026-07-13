# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a professional resume in LaTeX format for Muhammad Basit, a Senior Full Stack .NET & Azure Engineer. The resume uses a clean, ATS-parsable template based on Jake Gutierrez's resume template.

## Project Structure

- **`FullStackDeveloper/MuhammadBasit'sResume.tex`** — Main resume document. Contains all content sections: work authorization, professional summary, technical skills, experience, certifications, and education.

## Building & Compiling

The resume is a standard LaTeX document that compiles to PDF. Use any of these commands to generate the PDF:

```bash
# Using pdflatex (standard)
pdflatex -interaction=nonstopmode "FullStackDeveloper/MuhammadBasit'sResume.tex"

# Using xelatex (if using advanced fonts)
xelatex -interaction=nonstopmode "FullStackDeveloper/MuhammadBasit'sResume.tex"

# Clean compiled artifacts
rm -f FullStackDeveloper/*.pdf FullStackDeveloper/*.aux FullStackDeveloper/*.log FullStackDeveloper/*.out
```

The compiled PDF will be created in the same directory as the `.tex` file.

## Architecture & Key Sections

The resume uses custom LaTeX commands defined at the top of the document:

- **`\resumeItem{text}`** — Single bullet point in a list
- **`\resumeSubheading{title}{date}{company}{location}`** — Experience/education entry with company and dates
- **`\resumeProjectHeading{project}{date}`** — Project entry
- **`\resumeSubHeadingListStart/End`** — Wrappers for lists of entries
- **`\resumeItemListStart/End`** — Wrappers for bullet point lists

## Content Sections

- **Work Authorization** — Legal status and sponsorship requirements
- **Professional Summary** — Brief high-level background
- **Technical Skills** — Languages, frameworks, cloud platforms, authentication, databases, architecture, and AI tools
- **Experience** — Chronological work history with bullet-point accomplishments
- **Certifications** — Professional certifications and training
- **Education** — Academic background

## Font & Styling Options

Commented-out font options are available at lines 25–33. To use a different font family (sans-serif or serif), uncomment the desired line and comment out others. Current setup uses default LaTeX serif font.

## ATS Compatibility

The document is configured for ATS (Applicant Tracking System) parsing:
- `\pdfgentounicode=1` ensures generated PDF is machine-readable
- Margins and formatting are optimized for parsing
- Avoid using images, tables, or complex graphics as they may not parse correctly

## Customization Notes

When editing:
- Keep text within reasonable line lengths to avoid formatting breaks
- Use `\textbf{}` for bold, `\textit{}` for italics
- Company names and positions use `\textbf{}` for emphasis
- Skills are grouped by category (Languages, Frameworks, Cloud, etc.) separated by `\\`
- Use `\href{}` for hyperlinks with `\underline{}` for contact info
