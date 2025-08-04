# 10 Things to Get Started with Markdown

1. **What is Markdown?**
   - Markdown is a way to format text using simple symbols, so it looks good on GitHub, documentation, or websites. It’s easy to read even in its raw form, and files usually end with `.md` or `.markdown`.
   - Markdown is a type of markup language (like HTML, but much simpler).

2. **Basic Headings and Text**
   - Use `#` for big titles, `##` for subtitles, and `###` for smaller headings:
     ```md
     # Main Title (H1)
     ## Section Title (H2)
     ### Subsection (H3)
     ```
   - Italic: `*italic*` or `_italic_`
   - Bold: `**bold**` or `__bold__`
   - You can combine them: `**_bold and italic_**`

3. **Lists**
   - Unordered (bulleted) lists:
     ```md
     - Item 1
     - Item 2
     ```
   - Ordered (numbered) lists:
     ```md
     1. First
     2. Second
     ```
   - You can nest lists by indenting with spaces.

4. **Links and Images**
   - Add a clickable link:
     ```md
     [Google](https://www.google.com)
     ```
   - Show an image:
     ```md
     ![Alt text](image.png)
     ```

5. **Blockquotes and Code**
   - Blockquote (for quotes or notes):
     ```md
     > This is a quote or note.
     ```
   - Inline code (for short code):
     ```md
     Here is some `inline code` in a sentence.
     ```
   - Code block (for longer code):
     ```md
     ```js
     console.log('Hello, world!');
     ```
     ```

6. **Tables**
   - Organize data in a table:
     ```md
     | Syntax    | Description |
     |-----------|-------------|
     | Header    | Title       |
     | Paragraph | Text        |
     ```
   - You can align columns with colons (`:`).

7. **Task Lists**
   - Make checklists (great for to-dos):
     ```md
     - [x] Task done
     - [ ] Task not done
     ```

8. **Strikethrough, Highlight, Sub/Superscript**
   - Strikethrough: `~~text~~` (shows as ~~text~~)
   - Highlight: `==text==` (shows as ==text==)
   - Subscript: `H~2~O` (shows as H₂O)
   - Superscript: `X^2^` (shows as X²)

9. **Collapsible Sections and Diagrams**
   - Collapsible (click-to-expand) sections:
     ```md
     <details>
     <summary>Click to expand</summary>
     Hidden content goes here
     </details>
     ```
   - Diagrams (ASCII art or text):
     ```text
     +-----+
     | Box |
     +-----+
     ```
   - You can also draw simple branch diagrams for Git:
     ```
     main
      |
     dev
      |\
     test beta
     ```

10. **Uploading Files**
    - On GitHub, you can drag and drop images, videos, markdown files, and more into markdown text areas. GitHub will host the file and create a link for you.
    - Common file types: `.png`, `.jpg`, `.gif`, `.md`, `.log`, `.docx`, `.pptx`, `.xlsx`, and more.
