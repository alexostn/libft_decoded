# libft_decoded
Visual Metaphors for Code, Part 1: Libft. An artistic exploration of C programming fundamentals.

This project is the first part of my "Visual Metaphors for Code" series. 
It centers on Libft, the foundational École 42 project that challenges students to recreate standard C library functions from scratch. 
This project isn't just an implementation of a standard library—it's a visual investigation into its core concepts. My objective is to push beyond writing code to translate abstract logic into a universal visual language. Here, I deconstruct basic ideas like strings, memory, and linked lists to find and reveal their inner structure and hidden elegance.



## Gallery of Concepts

Here are some of the concepts from the `libft` library, deconstructed and reinterpreted as visual ideas.

---

### Concept: System library compiler libft

<img src="illustrations/libft_compiler_600.jpg" alt="Описание изображения" width="400"/>

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
    
   
    **Note:** To adhere to 42's academic integrity policy and prevent plagiarism, only the Makefile is provided here, not the entire source project it belongs to.
    ```

 *   For the full orchestration, see the complete <a href="https://github.com/alexostn/libft_decoded/blob/main/Makefile" target="_blank">Makefile</a>.

  *   **Note:** The full source code is available upon request.
---

### Concept: Comparison ft_memcmp()

<img src="illustrations/ft_memcmp()_600.jpg" alt="Memory Compare ft_memcmp()" width="400"/>

*   **The Metaphor:** This painting portrays the methodical process of ft_memcmp as a mystical observation. Two nearly identical figures, representing memory blocks s1 and s2, are compared within a defined space bounded by the limit n.
The soft, muted tones underscore the calm, byte-by-byte analysis. A central point of light symbolizes the pivotal moment the first difference is found, the loop terminates, and a value is returned.
*   The entire scene captures the essence of pure navigation and comparison—an act of observation without alteration, which is the foundational step before learning to modify data structures.

    ```
    /*
     * The logic is centered around a single loop that moves an index i forward
     * as long as the bytes are identical and the boundary n is not reached.
     * This is a perfect example of pure navigation.
    */
    
	int ft_memcmp(const void *s1, const void *s2, size_t n)
	{
	    size_t          i;
	    unsigned char   *p1;
	    unsigned char   *p2;
	
	    p1 = (unsigned char *)s1;
	    p2 = (unsigned char *)s2;
	    i = 0;
	    while (i < n && p1[i] == p2[i])
	        i++;
	    if (i == n)
	        return (0);
	    return (p1[i] - p2[i]);
	}

    ```


### Concept: av[i]=0_vs_av=0
	Navigation vs. Creation ft_split()
 
<img src="illustrations/libft_compiler_600.jpg" alt="Описание изображения" width="400"/>
<img src="illustrations/av[i]_600.jpg" alt="Описание изображения" width="400"/>

*   **The Metaphor:** After mastering pure observation, the next step is creation. This concept explores the crucial difference between navigating a data structure and fundamentally altering it.
i = 0 is the simple act of choosing a starting point for our observation.
av[i] = 0, however, is a creative act of definition: we place a boundary, a terminator, declaring that the structure now ends here. This leap in understanding, first encountered in ft_split, is the key to mastering command-line arguments and process control in later projects like pipex and minishell.

  This duality is perfectly captured within the architecture of ft_split.  
We first navigate the array to fill it with content "i = 0",
and then we terminate it to give it a definitive structure,
making it usable by other parts of a system.
The Act of Creation (Termination): Here, we are not iterating.
We are placing a NULL sentinel to define the boundary of our newly created array of strings.
This is the av[i] = 0 moment, where we give our data structure its final form.


    ```

    
	/*
	 * This function allocates memory for the array and then places a NULL
	 * at the end, effectively "sealing" it.
	*/
	char    **ft_split(char const *s, char c)
	{
	    char    **token_v;
	    size_t  words_count;
	
	    // ... (memory allocation logic)
	    token_v[words_count] = NULL; // The act of termination
	    // ...
	    return (token_v);
	}

    ```
* The Act of Navigation (Iteration): In contrast, the word_index variable within our helper function is a pure navigator. It starts at 0 and simply increments, pointing to the next available slot to be filled. This is the i = 0 moment — a simple change of focus, not a change of structure.

    ```
	/*
	 * This helper function uses an index to iterate through the allocated
	 * array and fill it with content.
	*/
	static int  ft_cpy_words(char **token_v, char const *s, char del)
	{
	    int     word_index;
	
	    word_index = 0; // The act of navigation: start at the beginning
	    while (*s)
	    {
	        // ... (logic for copying words)
	        ++word_index; // Move to the next position
	    }
	    return (0);
	}
    ```


Licensing Information
Code: The source code in this repository is licensed under the MIT License. You are free to use, modify, and distribute it as you see fit. See the LICENSE file for more details.

Visual Assets: All visual assets, including all images and illustrations found in the visuals directory and within this README, are All Rights Reserved. They are the exclusive intellectual property of the author. You may not use, reproduce, distribute, or create derivative works from these images for any commercial or non-commercial purposes without explicit written permission.
