# beast2.7-setup-guide

Outline
1. Setup BEAST 2.7 within Intellij
2. Build new package via ant within IntelliJ
3. Debug the Beauti template of your new package


# 1. Setup BEAST 2.7 within IntelliJ

## 1.1. Installation

Install JAVA Azul JDK 17. Make sure to install the fx version!

https://www.azul.com/downloads/?version=java-17-lts&package=jdk-fx

Install the BEAST 2 code as described [here](https://github.com/CompEvol/BeastFX).

https://www.azul.com/downloads/?version=java-17-lts&package=jdk-fx

Install IntelliJ IDE (Community Edition): https://www.jetbrains.com/idea/download/

## 1.2. Setup within IntelliJ

Follow [here](https://github.com/Tay-j/Beast2.7-Dev-IntelliJ) for setup within IntelliJ.

## 1.3. Running BEAST 2 
To run BEAST within IntelliJ, go to Run --> Run... --> Edit Configuration. The following settings worked for me for one of the example xmls provided in the beast2/examples folder.
<img width="807" alt="beast_run" src="https://github.com/user-attachments/assets/37f61246-6e0b-4be6-a855-3d124d428822">

# 2. Build a new package via ant within IntelliJ
Download your package source code into the same parent directory as beast2 and beastFX. Import the source code into IntelliJ  via File --> New --> Module from existing sources and as done before with beast2 and beastFX. Make sure to set your package dependencies as [before](https://github.com/Tay-j/Beast2.7-Dev-IntelliJ) in File --> Project Structure. 

The following settings worked in my run configuration to run the sciphy package:
<img width="1431" alt="package-run" src="https://github.com/user-attachments/assets/5f66411e-ff9e-4d88-a268-852f635a2829">

To build the package using ant within IntelliJ, first install the ant plugin in IntelliJ. To do so, press Command-, search for and install the ant plugin. To build your package, create a build.xml e.g. following the instructions on the [BEAST 2 website](https://www.beast2.org/package-development-guide/writing-a-beast-2_7-package.html). Then, in IntelliJ, right-click on the build.xml and choose "Add as Ant Build File".

# 3. Debug the Beauti template of your new package
To create a Beauti template for your new package, follow the guidelines on the [BEAST 2 website](https://www.beast2.org/package-development-guide/writing-a-beast-2_7-package.html) and make sure that Beauti finds your template. For debugging your Beauti template within IntelliJ, the following run configuration in IntelliJ worked for me. 
<img width="1431" alt="beauti-debug-package" src="https://github.com/user-attachments/assets/a80a2cb7-b017-4a65-a248-e66910006edb">
