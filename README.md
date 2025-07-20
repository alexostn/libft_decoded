# libft_decoded
Visual Metaphors for Code, Part 1: Libft. An artistic exploration of C programming fundamentals.

This project is the first part of my "Visual Metaphors for Code" series. 
It centers on Libft, the foundational École 42 project that challenges students to recreate standard C library functions from scratch. 
This project isn't just an implementation of a standard library—it's a visual investigation into its core concepts. My objective is to push beyond writing code to translate abstract logic into a universal visual language. Here, I deconstruct basic ideas like strings, memory, and linked lists to find and reveal their inner structure and hidden elegance.



## Gallery of Concepts

Here are some of the concepts from the `libft` library, deconstructed and reinterpreted as visual ideas.

---

### Concept: System library compiler

![A symbolist metaphor for the Compiler](illustrations/libft_compiler.jpg)

*   **The Vision:** This symbolist painting presents a metaphor for the act of programming itself, inspired by the library's functions. At the center stands a figure embodying the compiler, orchestrating streams of glowing symbols that float in cosmic space. These symbols represent library functions such as `ft_strlen`, `ft_split`, and `ft_calloc`, and their intricate interactions.
*   **The Engine (`Makefile`):** Just as the Conductor figure orchestrates the symbols, the `Makefile` is the engine that brings this code to life. It defines the rules and recipes for compiling the library, transforming source files into a functional tool. It represents the hidden structure that governs the entire process.

---

*   **The Code (Snippet from `Makefile`):**
    ```
    # The core rule that compiles source files into object files.
    # This pattern matching rule is the heart of the Makefile's efficiency.
    %.o: %.c libft.h
        $(CC) $(CFLAGS) -c $< -o $@

    # The final rule that links all object files into the library archive.
    $(NAME): $(OBJS)
        ar rcs $(NAME) $(OBJS)
    
    # For the full orchestration, see the complete <a href="https://github.com/alexostn/libft_decoded/blob/main/Makefile" target="_blank">Makefile</a>.
    **Note:** To adhere to 42's academic integrity policy and prevent plagiarism, only the Makefile is provided here, not the entire source project it belongs to.
    ```



Licensing Information
Code: The source code in this repository is licensed under the MIT License. You are free to use, modify, and distribute it as you see fit. See the LICENSE file for more details.

Visual Assets: All visual assets, including all images and illustrations found in the visuals directory and within this README, are All Rights Reserved. They are the exclusive intellectual property of the author. You may not use, reproduce, distribute, or create derivative works from these images for any commercial or non-commercial purposes without explicit written permission.
