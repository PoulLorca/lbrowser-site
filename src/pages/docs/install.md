---
layout: ../../layouts/DocsLayout.astro
title: LBrowser Documentation-Installation
---
## Deployment & Installation

Getting LBrowser up and running is straightforward, whether you prefer to use the pre-compiled releases or build the project yourself from the source code.

### Running from ZIP Files

LBrowser is designed to be portable. The release packages for Linux and Windows are self-contained and require no traditional installation process. Simply download, extract, and run.

#### Windows (10/11 - 64-bit)

1.  **Download:** Obtain the latest Windows `.zip` release from the [Download page](/download).
2.  **Extract:** Unzip the downloaded file to any folder on your computer.
3.  **Run:** Navigate to the extracted folder.
    * Typically, you can run `LBrowser.exe` located inside the `/bin` directory. This is the standard executable.

    ```bash
    # Example command assuming extraction to C:\LBrowser
    C:\LBrowser\bin\LBrowser.exe
    ```

    * **Hardware Acceleration Issue:** On some Windows systems, you might encounter issues with hardware acceleration (based on Skia) that prevent the browser from starting correctly. If you experience this, an alternative launcher is provided that disables hardware acceleration.
    * To use the hardware acceleration disabled mode, run the `.bat` file located in the **root** of the extracted folder instead of the `.exe` in `/bin`. This batch file acts as a wrapper, executing commands in the console to disable hardware acceleration specifically for the LBrowser process before launching it.

    ```bash
    # Example command assuming extraction to C:\LBrowser
    C:\LBrowser\LBrowser.bat
    ```

#### Linux (64-bit)

1.  **Download:** Obtain the latest Linux `.zip` or `.tar.gz` release from the [Download page](/download).
2.  **Extract:** Unzip or extract the downloaded file to any folder on your computer.
3.  **Run:** Navigate to the extracted root folder.
    * You might need to make the main executable file runnable. Open a terminal in the extracted folder and use the `chmod` command:

    ```bash
    cd /path/to/extracted/LBrowser
    chmod +x LBrowser
    ```
    * Then, execute the LBrowser file located in the root folder:

    ```bash
    ./LBrowser
    ```

#### Console Output - LBrowser's Vote of Confidence

When you run LBrowser from the console or terminal using the commands above (rather than double-clicking in a file explorer), you will notice that it prints messages detailing its internal processes. This is intentional. While not typical for end-user applications, this verbose output is designed to provide transparency into what LBrowser is doing "behind the scenes." This can be incredibly helpful for troubleshooting issues or simply understanding the browser's operations. Consider it LBrowser's "vote of confidence" – showing you exactly what it's doing.

### Building from Source

For developers or users who prefer to compile from source, you can build LBrowser directly from the GitHub repository.

**Prerequisites:**

* **Java Development Kit (JDK):** JDK version 21 or higher is required. [Liberica JDK](https://bell-sw.com/pages/downloads/#liberica) is recommended.
* **Qt Framework:** You need Qt 6.9 installed.
    * **Windows Specific:** When installing Qt on Windows, ensure you select the **MSVC2022** option.
    * **Required Qt Modules:** In addition to the Qt Core components, make sure the following optional modules are also installed:
        * Multimedia
        * WebChannel
        * WebSocket
        * WebView
        * Positioning

**Building Process:**

1.  **Clone the Repository:** Clone the LBrowser GitHub repository to your local machine.
    ```bash
    git clone YOUR_GITHUB_REPO_LINK
    cd LBrowser
    ```
2.  **Build with Maven:** The project uses Maven. Building will generate a JAR file.

    ```bash
    mvn clean package
    ```
3.  **Native Dependencies & Packaging:** The generated JAR file contains the Java code but requires native Qt Jambi libraries specific to your operating system to run. These native dependencies are referenced in the `pom.xml` (often commented out for specific platforms like Windows or Linux). The raw JAR alone will not be runnable as an application.
    * To create a runnable package that includes these native libraries and other necessary assets, you need to use the **QTdeployer** tool. This tool is essential for collecting all dependencies and packaging the application correctly for distribution.

For more detailed information on building LBrowser from source, including specific configurations related to Qt Jambi native dependencies and the usage of QTdeployer, please consult the broader Qt Jambi documentation.

**Running from IDE or Command Line (Development):**

If you are running the project directly from an IDE (like IntelliJ IDEA) or via the `java -jar` command during development, you will need to tell the Java runtime where to find the native Qt libraries. This is typically done by setting the `Djava.library.path` VM option to point to the `lib` or `bin` directories of your Qt installation.

```bash
# Example command (adjust paths for your system and Qt installation)
-Djava.library.path="/path/to/your/Qt/lib"
```

<div class="flex justify-between mt-8 pt-4 border-t border-border">
    <a href="/docs/modes" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">← Previous Section</a>
    <a href="/docs/issues" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">Next Section →</a>
</div>