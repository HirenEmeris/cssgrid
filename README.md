CSS Grid Demonstration
======================

📚 WEDE5020 – LU4: CSS Grid
---------------------------

This repository contains the **source code used in the CSS Grid lecturer video** for **Learning Unit 4 (LU4), Theme 3**.

The purpose of this project is to provide you with a practical example that you can download, open in VS Code, experiment with, and use as a reference while learning CSS Grid.

🎯 What You Will Learn
----------------------

The example introduces the basic concepts of **CSS Grid**, including:

*   Creating a Grid container using display: grid
    
*   Creating columns with grid-template-columns
    
*   Creating rows with grid-template-rows
    
*   Using fractional units (fr)
    
*   Controlling spacing with gap
    
*   Using repeat()
    
*   Understanding Grid items and their placement
    
*   Spanning items across columns
    
*   Using Grid areas
    
*   Creating layouts using grid-template-areas
    
*   Assigning elements using grid-area
    
*   Creating responsive Grid layouts
    
*   Using auto-fit
    
*   Using minmax()
    

The purpose is to help you understand **how CSS Grid can be used to structure a webpage using rows and columns**.

📁 Project Structure
--------------------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   css-grid/  │  ├── _css-assets/  │   └── styles.css  │  ├── index.html  │  └── README.md   `

### index.html

Contains the HTML structure for the Student Dashboard.

### \_css-assets/styles.css

Contains the CSS used to style the page and demonstrate CSS Grid.

### README.md

This file provides an overview of the project and the concepts demonstrated.

🖥️ The Example
---------------

The project uses a simple **Student Dashboard** to demonstrate how CSS Grid can be used to create a webpage layout.

The layout contains areas such as:

*   Header
    
*   Sidebar
    
*   Main content
    
*   Additional information
    
*   Footer
    
*   Dashboard cards
    

The overall layout can be visualised as:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   ┌─────────────────────────────────────────────┐  │                  HEADER                     │  ├──────────────┬─────────────────┬────────────┤  │              │                 │            │  │   SIDEBAR    │      MAIN       │   EXTRA    │  │              │                 │            │  ├──────────────┴─────────────────┴────────────┤  │                  FOOTER                     │  └─────────────────────────────────────────────┘   `

🧱 Important CSS Grid Concepts
------------------------------

### Creating a Grid

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   .container {      display: grid;  }   `

This turns an element into a **Grid container**.

### Creating Columns

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns: 1fr 1fr 1fr;   `

This creates three columns.

The fr unit represents a **fraction of the available space**.

For example:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns: 2fr 1fr 1fr;   `

means that the first column receives twice the available proportion of the other two columns.

### Adding Space Between Items

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   gap: 20px;   `

The gap property controls the space between Grid items.

### Using repeat()

Instead of writing:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns: 1fr 1fr 1fr;   `

you can write:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns: repeat(3, 1fr);   `

This is particularly useful when the same value is repeated.

### Spanning Columns

An item can occupy more than one column:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   .card {      grid-column: span 2;  }   `

This allows the item to stretch across two Grid columns.

### Grid Areas

Grid can also be used to describe the layout using named areas:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-areas:      "header header header"      "sidebar main extra"      "footer footer footer";   `

Elements can then be assigned to those areas:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   .header {      grid-area: header;  }   `

This can make larger layouts easier to understand and maintain.

📱 Responsive Grid
------------------

The project also demonstrates a responsive Grid technique:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns:      repeat(auto-fit, minmax(200px, 1fr));   `

This allows the browser to automatically adjust the number of columns based on the available space.

Try resizing your browser window and observe how the cards respond.

🧪 Experiment With the Code
---------------------------

**Don't just copy the code — experiment with it.**

Try changing:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns: repeat(3, 1fr);   `

to:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns: repeat(4, 1fr);   `

Then try:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-template-columns: 2fr 1fr;   `

Experiment with:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   gap: 10px;   `

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   gap: 30px;   `

and:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   grid-column: span 2;   `

Observe what changes on the webpage.

### Challenge

Try creating your own Grid layout using:

*   3 columns
    
*   Different column sizes
    
*   A gap
    
*   At least one item spanning multiple columns
    

🔄 Grid vs Flexbox
------------------

You have previously worked with **Flexbox**, so it is important to understand that Grid does not simply replace Flexbox.

A useful way to think about them is:

FlexboxCSS GridOne-dimensionalTwo-dimensionalRow **or** columnRows **and** columnsGreat for navigationGreat for page layoutsGreat for aligning itemsGreat for structured layoutsUseful for component-level layoutsUseful for larger page layouts

In practice, **Flexbox and Grid can also be used together**.

▶️ How to Use This Project
--------------------------

1.  Download or clone the repository.
    
2.  Open the project folder in **VS Code**.
    
3.  Open index.html.
    
4.  Open the page in your browser.
    
5.  Open \_css-assets/styles.css.
    
6.  Experiment with the Grid properties.
    
7.  Save your changes and refresh the browser.
    

You can also use **Live Server** in VS Code if you have it installed.

📌 Important
------------

This repository is provided as a **learning resource** alongside the LU4 Theme 3 lecturer video.

You are encouraged to:

*   Read the code.
    
*   Type the examples yourself.
    
*   Change values.
    
*   Break the layout.
    
*   Fix the layout.
    
*   Try your own combinations.
    
*   Use the browser's Developer Tools to inspect the Grid.
    

The goal is to understand **why the layout changes**, not simply to reproduce the final code.

📚 Further Learning
-------------------

For additional CSS Grid practice and explanations, refer to resources such as:

*   [MDN – CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Grids)
    
*   [MDN – Basic Concepts of Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Grid_layout/Basic_concepts)
    
*   [MDN – CSS Grid Layout Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Grid_layout)
    

🎓 WEDE5020
-----------

**Learning Unit:** LU4 – CSS**Theme:** Theme 3**Topic:** CSS Grid

> **Remember:** CSS Grid is about thinking in terms of **rows, columns and relationships between elements**.

**Don't just copy the Grid. Understand the Grid.**
