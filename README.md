Here is the formatted `README.md` file. You can add this directly to the root of your repository so students see it immediately when they open the Codespace.

-----

# Assignment: Using an External C Library 

In this assignment, you will ccompile a program that spans multiple files and link custom libraries.

## 1\. Setup

1.  Open this repository in **GitHub Codespaces**.
2.  Explore the file tree on the left. You will see two files provided for you:
      * `term_utils.h`: The **header file** (definitions).
      * `term_utils.c`: The **implementation file** (the actual code for the colors).
3.  **Note:** Do not modify `term_utils.c` or `term_utils.h`. Your job is to *use* them, not change them.

## 2\. The Coding Task


1.  Complete the `TODO` comments by writing the correct C code. Refer to `term_utils.h` to see which functions are available and what arguments they require.

## 3\. Compilation

Because your program relies on code located in a separate file (`term_utils.c`), you cannot simply compile `main.c` alone. You must tell the compiler to link both files together.

1.  Open the **Terminal** in VS Code (press `` Ctrl + ` ``).
2.  Run the following command exactly:

<!-- end list -->

```bash
gcc -Wall -Wextra -pedantic main.c term_utils.c -o my_program
```

### Understanding the Flags:

  * `-Wall`: Turns on almost all warnings.
  * `-Wextra`: Turns on extra warnings that aren't covered by Wall.
  * `-pedantic`: Ensures your code strictly adheres to the ISO C standard.
  * `main.c term_utils.c`: We list **both** source files so they are compiled into one executable.
  * `-o my_program`: Names the output file `my_program`.

## 4\. Running the Program

Run your executable to verify the output is colored correctly:

```bash
./my_program
```

## 5\. Submission (VS Code GUI)

You must submit your work by pushing your changes to GitHub using the **VS Code Source Control interface**.

> **Requirement:** Do not use the command line (git add/commit/push) for this step. Use the graphical buttons.

1.  **Access Source Control:** Click the **Source Control icon** on the left sidebar (it looks like a graph node, or press `Ctrl+Shift+G`).
2.  **Stage Changes:** You will see `main.c` listed under "Changes." Click the **+ (Plus)** sign next to `main.c` to "Stage" the file.
3.  **Commit:** In the "Message" box at the top of the sidebar, type: `Completed main function implementation`.
4.  **Finalize:** Click the blue **Commit** button.
5.  **Push:** Click the **Sync Changes** button (or "Publish Branch") that appears to push your code to GitHub.
6. Finally, submit your repository URL to Blackboard.
