# Enhanced-CAP®-Exam-Study-Guide

This repository contains an enhanced version of the CAP® Exam Study Guide. It is designed to help candidates prepare for the Certified Analytics Professional (CAP®) exam by providing detailed notes, explanations, and resources for each domain covered in the exam. The guide includes comprehensive explanations, examples, and references to help understand the key concepts required for the exam.

## Features

- Detailed coverage of all domains in the CAP® exam
- Expanded notes with in-depth explanations and examples
- References to additional reading materials
- Visual aids and tables for easy understanding
- Acknowledgement of sources and contributors

## Contents

- Detailed notes on each domain:
  - Domain I: Business Problem Framing (≈14%)
  - Domain II: Analytics Problem Framing (≈17%) 
  - Domain III: Data (≈23%)
  - Domain IV: Methodology Selection (≈14%)
  - Domain V: Model Building (≈16%)
  - Domain VI: Deployment (≈10%)
  - Domain VII: Model Lifecycle Management (≈6%)
- Key concepts and definitions
- Practical examples and use cases
- Best practices and guidelines
- Review questions and sample problems
- Visual aids including charts, diagrams and plots
- Formulas and statistical concepts
- Glossary of important terms
- References for further reading

## Usage

This study guide is intended for personal use in preparing for the CAP® exam. It should be used in conjunction with official [INFORMS](https://www.informs.org/) materials and other reputable study resources. The guide provides a comprehensive overview but does not guarantee exam success on its own.

## How to Use the PDF Output Configuration

If you want to generate a PDF output from this R Markdown file, follow these steps:

1. Open your R Markdown file in RStudio or your preferred R Markdown editor.

2. At the very top of your R Markdown file, you'll see a section enclosed by three dashes (`---`) at the top and bottom. This is called the YAML header.

3. Replace the existing YAML header with the following configuration:

 ```yaml
---
# Basic document information
title: "Enhanced CAP® Exam Study Guide"
author: "Philip Bachas-Daunert"
date: "Most Recent Generation: `r format(Sys.Date(), '%A, %B %d, %Y')`"  # Dynamically generates the current date

# Output format settings
output: 
  pdf_document:
    toc: yes  # Include a table of contents
    toc_depth: 2  # Include headers up to level 2 in the table of contents
    number_sections: true  # Automatically number sections
    fig_caption: yes  # Enable figure captions
    highlight: tango  # Use 'tango' style for code highlighting
    keep_tex: yes  # Keep the intermediate .tex file
    latex_engine: xelatex  # Use xelatex for PDF generation (supports more fonts)

# Additional LaTeX packages and commands
header-includes:
   - \usepackage{float}  # Provides more control over float positioning
   - \floatplacement{figure}{H}  # Force figures to be placed exactly where they appear in the source
   - \usepackage{afterpage}  # Allows for commands to be executed on the next page
   - \AfterEndEnvironment{toc}{\afterpage{\null\newpage}}  # Insert a new page after the table of contents
   - \usepackage{titlesec}  # Allows customization of section titles
   - \newcommand{\sectionbreak}{\clearpage}  # Start a new page for each section

# Page layout settings
geometry: margin=1in  # Set all page margins to 1 inch

# Font settings
fontsize: 11pt  # Set the main font size to 11 points
mainfont: Arial  # Set the main font to Arial
monofont: Courier  # Set the monospaced font (used for code) to Courier
---
 ```

4. Make sure to copy the entire block, including the opening and closing `---` lines.

5. You can customize the following fields if needed:
   - `title`: Change this to your preferred title.
   - `author`: Replace with your name.
   - `toc_depth`: Adjust this number to control how many levels of headers are included in the table of contents.
   - `fontsize`: Change the font size if desired.
   - `mainfont` and `monofont`: Change these to your preferred fonts.

6. Save your R Markdown file after making these changes.

7. To generate the PDF:
   - If using RStudio: Click the "Knit" button at the top of the editor and select "Knit to PDF".
   - If using command line: Use the command `rmarkdown::render("your_file.Rmd", output_format = "pdf_document")`.

8. The PDF will be generated in the same directory as your R Markdown file.

This configuration will create a PDF with the following features:
- A title page with the specified title, author, and date.
- A table of contents on a separate page.
- Each main section (Header 1) starting on a new page.
- Numbered sections.
- Figure captions enabled.
- Code highlighting using the "tango" theme.
- 1-inch margins and 11pt font size.

Note: You may need to install additional LaTeX packages if you encounter any errors during PDF generation. RStudio usually prompts you to install these automatically.

## Acknowledgements

This study guide enhances and builds upon publicly available resources, including the INFORMS CAP® exam guidelines. Special thanks to INFORMS, ChatGPT, Claude, and Gemini for their contributions and insights. This guide is intended for educational and personal use only and is not for sale.

## License

This project is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) license. 

### Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)

#### You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material

The licensor cannot revoke these freedoms as long as you follow the license terms.

#### Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- **NonCommercial** — You may not use the material for commercial purposes.
- **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

#### No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

#### Notices:
You do not have to comply with the license for elements of the material in the public domain or where your use is permitted by an applicable exception or limitation.

No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material.

For more details, see the [LICENSE](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) file.

## Disclaimer

This study guide does not guarantee passing the CAP® exam. It is recommended to use official INFORMS resources and other reputable study materials in addition to this guide. All trademarks and service marks referenced are property of their respective owners.