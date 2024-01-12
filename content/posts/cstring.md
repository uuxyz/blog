---
title: cstring
date: 2023-12-17
---

1. **Functions returning `void*` type:**
    - `memchr`: Searches for the position of a specified character in the string.
    - `memcpy`: Copies a block of memory.
    - `memmove`: Moves a block of memory.
    - `memset`: Sets the values of a block of memory.
2. **Functions returning `int` type:**
    - `memcmp`: Compares blocks of memory.
    - `strcmp`: Compares strings.
    - `strncmp`: Compares the first n characters of strings.
    - `strcoll`: Compares strings according to the localization rules.
3. **Functions returning `char*` type:**
    - `strcat`: Concatenates strings.
    - `strncat`: Concatenates the first n characters of strings.
    - `strchr`: Searches for the position of a specified character in the string.
    - `strcpy`: Copies strings.
    - `strncpy`: Copies the first n characters of strings.
    - `strerror`: Retrieves error messages based on error numbers.
    - `strpbrk`: Searches for the position of any character from a matching string in the string.
    - `strrchr`: Searches for the last occurrence of a specified character in the string.
    - `strstr`: Searches for the position of a specified substring in the string.
    - `strtok`: Breaks a string into a series of strings.
4. **Functions returning `size_t` type:**
    - `strcspn`: Returns the number of characters at the beginning of a string that do not belong to a specified character set.
    - `strlen`: Returns the length of a string.
    - `strspn`: Returns the number of characters at the beginning of a string that belong to a specified character set.
    - `strxfrm`: Returns the number of characters transformed based on the current locale's `LC_COLLATE`.