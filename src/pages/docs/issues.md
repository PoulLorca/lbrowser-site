---
layout: ../../layouts/DocsLayout.astro
title: LBrowser Documentation-Issues
---
## Reporting Issues

Encountered a problem or unexpected behavior while using LBrowser? Your bug reports are valuable in helping make the browser more stable and reliable. Please report any issues you find using the [GitHub Issues tracker](https://github.com/poullorca/lbrowser/issues).

Before submitting a new issue, please take a moment to:

1.  **Search Existing Issues:** Check if someone else has already reported the same problem. You can use the search bar in the Issues section. If an existing issue matches yours, feel free to add a comment with any additional details you can provide (especially if they differ from the original report).
2.  **Confirm it's a Bug:** Ensure the issue is a genuine bug or unexpected behavior, not a request for a new feature. As noted in the Introduction and Contribution sections, feature requests have a separate process (via community sponsorship on Ko-fi). **Issues submitted solely as feature requests will be closed.**

**How to Write a Good Bug Report:**

To help diagnose and fix the problem quickly, please provide as much detail as possible in your bug report. A good bug report includes:

1.  **Clear Title:** A brief, descriptive title summarizing the issue (e.g., "Browser crashes when opening settings," "Network Mode button doesn't respond on Linux").
2.  **LBrowser Version:** Specify the exact version of LBrowser you are using (e.g., `v1.0-SNAPSHOT`, or the commit hash if building from source).
3.  **Operating System & Version:** Provide details about your operating system (e.g., Windows 11 Pro 64-bit, Ubuntu 24.04 LTS 64-bit) and its version.
4.  **Steps to Reproduce:** Describe the exact steps you took that led to the issue. Numbering the steps makes it easier to follow.
    * Example:
        1. Open LBrowser.
        2. Click the 'Net Config' button.
        3. Wait for Portainer to load.
        4. Click the 'play' button for the Tor container.
        5. Observe... [describe what happened]
5.  **Expected Behavior:** Briefly describe what you expected to happen when following the steps.
6.  **Actual Behavior:** Describe what actually happened (e.g., "The container failed to start," "The browser window froze," "An error message appeared").
7.  **Console Output (CRITICAL):** If you ran LBrowser from the console or terminal (as described in the Deployment section), please copy and paste the output printed to the console into your issue report. This output contains valuable debugging information that is often essential for identifying the root cause of a problem. Please wrap console output in code blocks using triple backticks (```).

    ```
    [PASTE CONSOLE OUTPUT HERE]
    ```
8.  **Screenshots or Video (Optional but Recommended):** Including screenshots or a short video demonstrating the issue can be extremely helpful.

Providing a detailed report with the information requested above significantly increases the chances of the bug being identified and fixed in a timely manner.

Thank you for taking the time to report issues and help improve LBrowser!

<div class="flex justify-between mt-8 pt-4 border-t border-border">
    <a href="/lbrowser-site/docs/install" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">← Previous Section</a>
    <a href="/lbrowser-site/docs/sponsorship" class="px-4 py-2 border border-border rounded transition-colors duration-300 hover:bg-primary hover:text-white">Next Section →</a>
</div>