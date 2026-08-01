## Entry 3: Python Environment and Dataset Acquisition

**Date:** August 1, 2026

**Activity completed:**  
Configured the project’s external Python virtual environment, installed and verified the initial analytical libraries, created the first Jupyter notebook and loaded FEBRL Dataset 1 with its known duplicate relationships.

**Decisions made:**  
The Python environment was stored outside OneDrive while the project repository remained within the GitHub working folder. FEBRL Dataset 1 was loaded with its known true links so that future duplicate-detection methods can be evaluated against labelled matches.

**Reason for those decisions:**  
Storing the virtual environment outside OneDrive reduced the risk of package-installation delays caused by file synchronisation. Retaining the known links provides an objective basis for comparing rule-based and machine-learning matching performance.

**Problems encountered:**  
The original virtual environment was created in the wrong directory, and package installation became unresponsive when the environment was stored inside OneDrive. PowerShell also occasionally failed to return the visible prompt after package installation.

**Resolution:**  
The incomplete environment was removed and recreated outside OneDrive. The new interpreter was connected to VS Code, packages were installed in smaller groups and Command Prompt was used when PowerShell became unresponsive.

**What I learned:**  
I learned how the GitHub repository, VS Code workspace, Python interpreter, virtual environment, terminal and Jupyter kernel work together. I also learned how to verify the active Python executable and package location.

**Next action:**  
Conduct a structured data-quality audit covering dataset structure, missing values, uniqueness, field completeness and common variation patterns.
