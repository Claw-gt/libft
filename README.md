# libft

|**Name of the program** |**Files**|**Description**|
| ------- | ------- | ------ |
| libft.a | Makefile, libft.h , ft_*.c|Make your own library |

## Parte 1 - Funciones de libc

| Function | Prototype | Return value | Description |
|--------- | ----------- | ------- | ------ |
|`ft_isalpha` |`int ft_isalpha(int c)` | The values returned are nonzero if the character c falls into the tested class, and zero if not | isalpha() checks for an alphabetic character; in the standard "C" locale, it is equivalent to (isupper(c) ||  islower(c)) |
|`ft_isdigit` |`int ft_isdigit(int c)` | The values returned are nonzero if the character c falls into the tested class, and zero if not | isdigit() checks for a digit (0 through 9) |
|`ft_isalnum` |`int ft_isalnum(int c)` | The values returned are nonzero if the character c falls into the tested class, and zero if not | isalnum() checks for an alphanumeric character; it is equivalent to (isalpha(c) || isdigit(c)) |
|`ft_isascii` |`int ft_isascii(int c)` | The values returned are nonzero if the character c falls into the tested class, and zero if not | isascii() checks whether c is a 7-bit unsigned char value that fits into the ASCII character set |
|`ft_isprint` |`int ft_isprint(int c)` | The values returned are nonzero if the character c falls into the tested class, and zero if not | isprint() checks for any printable character including space |
|`ft_strlen` |`size_t strlen(const char *s)` | strlen() function returns the number of bytes in the string pointed to by s | The strlen() function calculates the length of the string pointed to by s, excluding the terminating null byte ('\0') |
|`ft_memset` |`void *memset(void *s, int c, size_t n)` | memset() function returns a pointer to the memory area s | The memset() function fills the first n bytes of the memory area pointed to by s with the constant byte c |
|`ft_bzero` |`void bzero(void *s, size_t n)` | None | The  bzero()  function  erases  the data in the n bytes of the memory starting at the location pointed to by s, by writing zeros (bytes containing '\0') to that area |
|`ft_memcpy` |`void *memcpy(void *dest, const void *src, size_t n)` | memcpy() function returns a pointer to dest | The  memcpy()  function copies n bytes from memory area src to memory area dest.  The memory areas must not overlap.  Use memmove(3) if the memory areas do overlap |
|`ft_memmove` |`void *memmove(void *dest, const void *src, size_t n)` | memmove() function returns a pointer to dest | The  memmove()  function copies n bytes from memory area src to memory area dest.  The memory areas may overlap: copying takes place as though the bytes in src are first copied into a temporary array that does not overlap src or dest, and the bytes are then  copied  from the temporary array to dest |
|`ft_strlcpy` |`size_t strlcpy(char *dst, const char *src, size_t size)` | strlcpy() function return the total length of the string they tried to create | strlcpy() function copy and concatenate strings respectively. The strlcpy() function copies up to size - 1 characters from the NUL-terminated string src to dst, NUL-terminating the result |
|`ft_strlcat` |`size_t strlcpy(char *dst, const char *src, size_t size)` | strlcat() function return the total length of the string they tried to create | strlcat() function concatenate strings respectively.  The strlcat() function appends the NUL-terminated string src to the end of dst.  It will append at most size - strlen(dst) - 1 bytes, NUL-terminating the result |
|`ft_toupper` |`int toupper(int c)` | The value returned is that of the converted letter, or c if the conversion was not possible | If  c  is  a lowercase letter, toupper() returns its uppercase equivalent, if an uppercase representation exists in the current locale. Otherwise, it returns c |
|`ft_tolower` |`int tolower(int c)` | The value returned is that of the converted letter, or c if the conversion was not possible | If c is an uppercase letter, tolower() returns its lowercase equivalent, if a lowercase representation exists in  the  current  locale. Otherwise, it returns c |
|`ft_strchr` |`char *strchr(const char *s, int c)` | The strchr() and strrchr() functions return a pointer to the matched character or NULL if the character is not found.  The  terminating null byte is considered part of the string, so that if c is specified as '\0', these functions return a pointer to the terminator | The strchr() function returns a pointer to the first occurrence of the character c in the string s |
|`ft_strrchr` |`char *strrchr(const char *s, int c)` | The strchr() and strrchr() functions return a pointer to the matched character or NULL if the character is not found.  The  terminating null byte is considered part of the string, so that if c is specified as '\0', these functions return a pointer to the terminator | The strrchr() function returns a pointer to the last occurrence of the character c in the string s |
|`ft_strncmp` |`int strncmp(const char *s1, const char *s2, size_t n)` | | |
|`ft_memchr` |`void *memchr(const void *s, int c, size_t n)` | | |
|`ft_memcmp` |`int memcmp(const void *s1, const void *s2, size_t n)` | | |
|`ft_strnstr` |`char *strnstr(const char *big, const char *little, size_t len)` | If little is an empty string, big is returned; if little occurs nowhere in big, NULL is returned; otherwise a pointer to the first character of the first occurrence of little is returned| The strnstr() function locates the first occurrence of the null-terminated string little in the string big, where not more than len characters are searched.  Characters that appear after a ‘\0’ character are not searched |
|`ft_atoi` |`int atoi(const char *nptr)` | The converted value or 0 on error | The atoi() function converts the initial portion of the string pointed to by nptr to int |
|`ft_calloc` |`void *calloc(size_t nmemb, size_t size)` | The malloc() and calloc() functions return a pointer to the allocated memory, which is suitably aligned for any built-in type.  On  error,  these  functions return NULL | The calloc() function allocates memory for an array of nmemb elements of size bytes each and returns a pointer to the allocated memory. The  memory is set to zero.  If nmemb or size is 0, then calloc() returns either NULL, or a unique pointer value that can later be successfully passed to free().  If the multiplication of nmemb and size would result in integer overflow, then calloc() returns an  error |
|`ft_strdup` |`char *strdup(const char *s)` | On success, the strdup() function returns a pointer to the duplicated string.  It returns NULL if insufficient  memory  was  available, with errno set to indicate the cause of the error| The  strdup()  function  returns a pointer to a new string which is a duplicate of the string s.  Memory for the new string is obtained with malloc(3), and can be freed with free(3)|

## Parte 2 - Funciones adicionales

| Function | Prototype | Return value | Description |
|--------- | ----------- | ------- | ------ |
|`ft_substr`|`char *ft_substr(char const *s, unsigned int start, size_t len);`| Substring. NULL if dynamic allocation fails| Allocate (with malloc(3)) and return a substring of string 's'. It will start from 'start' and have a maximum length of 'len'|
|`ft_strjoin`|`char *ft_strjoin(char const *s1, char const *s2);`| New string. NULL if dynamic allocation fails| Allocate (with malloc(3)) and return a new string formed by concatenation between 's1' and 's2'|
|`ft_strtrim`|`char *ft_strtrim(char const *s1, char const *set);`| Trimmed string. NULL if dynamic allocation fails| Delete all characters of string 'set' from the beginning and from the end until finding a character not belonging to 'set'|
|`ft_split`|`char **ft_split(char const *s, char c);`| Array of new strings resulted from the split. NULL if dynamic allocation fails| Allocate an array of strings resulted from splitting string 's' on substrings with character 'c' as delimiter|
