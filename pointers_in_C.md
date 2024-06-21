Certainly! Here's a list of 50 quiz questions related to pointers in C, presented in the form of "guess the output" scenarios. These questions cover a range of difficulty levels from easy to hard:

### Easy Level (1-20)

1. **Question:** 
   ```c
   #include <stdio.h>
   
   int main() {
       int num = 10;
       int *ptr = &num;
       
       printf("%d\n", *ptr);
       return 0;
   }
   ```
   **Output:**
   - A) 10
   - B) Compiler Error
   - C) Undefined Behavior
   - D) Garbage Value

2. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3, 4, 5};
       int *ptr = arr;
       
       printf("%d\n", *ptr++);
       printf("%d\n", *ptr);
       
       return 0;
   }
   ```
   **Output:**
   - A) 1, 2
   - B) 1, 1
   - C) 2, 2
   - D) 1, 3

3. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int a = 5;
       int *ptr = &a;
       *ptr = 10;
       printf("%d\n", a);
       
       return 0;
   }
   ```
   **Output:**
   - A) 5
   - B) 10
   - C) Compiler Error
   - D) Undefined Behavior

4. **Question:**
   ```c
   #include <stdio.h>
   
   void change(int *ptr) {
       *ptr = *ptr + 10;
   }
   
   int main() {
       int num = 5;
       change(&num);
       printf("%d\n", num);
       
       return 0;
   }
   ```
   **Output:**
   - A) 5
   - B) 10
   - C) 15
   - D) Compiler Error

5. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int *ptr = NULL;
       printf("%p\n", ptr);
       
       return 0;
   }
   ```
   **Output:**
   - A) 0x0
   - B) NULL
   - C) Garbage Value
   - D) Compiler Error

6. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int x = 5;
       int *ptr1, *ptr2;
       
       ptr1 = &x;
       ptr2 = ptr1;
       *ptr1 = 10;
       
       printf("%d\n", *ptr2);
       
       return 0;
   }
   ```
   **Output:**
   - A) 5
   - B) 10
   - C) Compiler Error
   - D) Undefined Behavior

7. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3};
       int *ptr = arr + 1;
       
       printf("%d\n", *ptr);
       
       return 0;
   }
   ```
   **Output:**
   - A) 1
   - B) 2
   - C) 3
   - D) Garbage Value

8. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3};
       int *ptr = arr;
       
       printf("%d\n", *ptr + 1);
       
       return 0;
   }
   ```
   **Output:**
   - A) 1
   - B) 2
   - C) 3
   - D) 4

9. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3};
       int *ptr = arr;
       
       printf("%d\n", *(ptr + 2));
       
       return 0;
   }
   ```
   **Output:**
   - A) 1
   - B) 2
   - C) 3
   - D) Garbage Value

10. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int a = 5;
        int *ptr1, *ptr2;
        
        ptr1 = &a;
        *ptr1 = 10;
        ptr2 = ptr1;
        
        printf("%d %d\n", *ptr1, *ptr2);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5 10
    - B) 10 10
    - C) 10 5
    - D) Compiler Error

11. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr;
        
        printf("%d\n", ptr[1]);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

12. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 1;
        
        printf("%d\n", ptr[-1]);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

13. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        
        printf("%p\n", ptr);
        ptr++;
        printf("%p\n", ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) Address of x, Address of next location after x
    - B) Address of x, Address of x + 1
    - C) Address of x, Garbage Value
    - D) Compiler Error

14. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {10, 20, 30};
        int *ptr = arr;
        
        printf("%d\n", *ptr++);
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 10, 10
    - B) 10, 20
    - C) 20, 20
    - D) 20, 10

15. **Question:**
    ```c
    #include <stdio.h>
    
    void increment(int *ptr) {
        (*ptr)++;
    }
    
    int main() {
        int x = 10;
        increment(&x);
        printf("%d\n", x);
        
        return 0;
    }
    ```
    **Output:**
    - A) 10
    - B) 11
    - C) Compiler Error
    - D) Undefined Behavior

16. **Question:**
    ```c
    #include <stdio.h>
    
    void change(int *ptr) {
        ptr = NULL;
    }
    
    int main() {
        int num = 5;
        int *ptr = &num;
        change(ptr);
        
        if (ptr == NULL)
            printf("NULL\n");
        else
            printf("Not NULL\n");
        
        return 0;
    }
    ```
    **Output:**
    - A) NULL
    - B) Not NULL
    - C) Compiler Error
    - D) Undefined Behavior

17. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr;
        
        printf("%d\n", *(ptr + 5));
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

18. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        
        printf("%d\n", *ptr++);
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5, Garbage Value
    - B) 5, 5
    - C) Garbage Value, Garbage Value
    - D) Compiler Error

19. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 2;
        
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

20. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr1, *ptr2;
        
        ptr1 = &x;
        ptr2 = ptr1;
        (*ptr1)++;
        
        printf("%d %d\n", *ptr1, *ptr2);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5 5
    - B) 6 5
    - C) 5 6
    - D) Compiler Error

### Medium Level (21-40)

21. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr;
        
        printf("%d\n", ptr[1]);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

22. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 1;
        
        printf("%d\n", ptr[-1]);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

23. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        
        printf("%p\n", ptr);
        ptr++;
        printf("%p\n", ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) Address of x, Address of next location after x
    - B) Address of x, Address of x + 1
    - C) Address of x, Garbage Value
    - D) Compiler Error

24. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {10, 20, 30};
        int *ptr = arr;
        
        printf("%d\n", *ptr++);
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 10, 10
    - B) 10, 20
    - C) 20, 20
    - D) 20, 10

25. **Question:**
    ```c
    #include <stdio.h>
    
    void increment(int *ptr) {
        (*ptr)++;
    }
    
    int main() {
        int x = 10;
        increment(&x);
        printf("%d\n", x);
        
        return 0;
    }
    ```
    **Output:**
    - A) 10
    - B) 11
    - C) Compiler Error
    - D) Undefined Behavior

26. **Question:**
    ```c
    #include <stdio.h>
    
    void change(int *ptr) {
        ptr = NULL;
    }
    
    int main() {
        int num = 5;
        int *ptr = &num;
        change(ptr);
        
        if (ptr == NULL)
            printf("NULL\n");
        else
            printf("Not NULL\n");
        
        return 0;
    }
    ```
    **Output:**
    - A) NULL
    - B) Not NULL
    - C) Compiler Error
    - D) Undefined Behavior

27. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr;
        
        printf("%d\n", *(ptr + 5));
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

28. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        
        printf("%d\n", *ptr++);
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5, Garbage Value
    - B) 5, 5
    - C) Garbage Value, Garbage Value
    - D) Compiler Error

29. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 2;
        
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

30. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr1, *ptr2;
        
        ptr1 = &x;
        ptr2 = ptr1;
        (*ptr1)++;
        
        printf("%d %d\n", *ptr1, *ptr2);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5 5
    - B) 6 5
    - C) 5 6
    - D) Compiler Error

31. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr;
        
        printf("%d\n", ptr[1]);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

32. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 1;
        
        printf("%d\n", ptr[-1]);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

33. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        
        printf("%p\n", ptr);
        ptr++;
        printf("%p\n", ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) Address of x, Address of next location after x
    - B) Address of x, Address of x + 1
    - C) Address of x, Garbage Value
    - D) Compiler Error

34. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {10, 20, 30};
        int *ptr = arr;
        
        printf("%d\n", *ptr++);
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 10, 10
    - B) 10, 20
    - C) 20, 20
    - D) 20, 10

35. **Question:**
    ```c
    #include <stdio.h>
    
    void increment(int *ptr) {
        (*ptr)++;
    }
    
    int main() {
        int x = 10;
        increment(&x);
        printf("%d\n", x);
        
        return 0;
    }
    ```
    **Output:**
    - A) 10
    - B) 11
    - C) Compiler Error
    - D) Undefined Behavior

36. **Question:**
    ```c
    #include <stdio.h>
    
    void change(int *ptr) {
        ptr = NULL;
    }
    
    int main() {
        int num = 5;
        int *ptr = &num;
        change(ptr);
        
        if (ptr == NULL)
            printf("NULL\n");
        else
            printf("Not NULL\n");
        
        return 0;
    }
    ```
    **Output:**
    - A) NULL
    - B) Not NULL
    - C) Compiler Error
    - D) Undefined Behavior

37. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr;
        
        printf("%d\n", *(ptr + 5));
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

38. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        
        printf("%d\n", *ptr++);
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    
    **Output:**
    - A) 5, Garbage Value
    - B) 5, 5
    - C) Garbage Value, Garbage Value
    - D) Compiler Error

39. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 2;
        
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

40. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr1, *ptr2;
        
        ptr1 = &x;
        ptr2 = ptr1;
        (*ptr1)++;
        
        printf("%d %d\n", *ptr1, *ptr2);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5 5
    - B) 6 5
    - C) 5 6
    - D) Compiler Error

### Hard Level (41-55)
### Advanced and Tricky Questions

41. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3};
       int *ptr = arr + 1;
       
       printf("%d\n", *ptr--);
       printf("%d\n", *ptr);
       
       return 0;
   }
   ```
   **Output:**
   - A) 2, 1
   - B) 2, 2
   - C) 1, 2
   - D) Compiler Error

42. **Question:**
   ```c
   #include <stdio.h>
   
   void swap(int *x, int *y) {
       int temp = *x;
       *x = *y;
       *y = temp;
   }
   
   int main() {
       int a = 5, b = 10;
       swap(&a, &b);
       printf("%d %d\n", a, b);
       
       return 0;
   }
   ```
   **Output:**
   - A) 5 10
   - B) 10 5
   - C) Compiler Error
   - D) Undefined Behavior

43. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3, 4};
       int *ptr = arr;
       
       printf("%d\n", *ptr++);
       printf("%d\n", *ptr);
       printf("%d\n", *(++ptr));
       printf("%d\n", *ptr);
       
       return 0;
   }
   ```
   **Output:**
   - A) 1, 2, 3, 3
   - B) 1, 2, 3, 4
   - C) 1, 3, 3, 3
   - D) Compiler Error

44. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int x = 5;
       int *ptr1, **ptr2;
       
       ptr1 = &x;
       ptr2 = &ptr1;
       
       printf("%d\n", **ptr2);
       
       return 0;
   }
   ```
   **Output:**
   - A) 5
   - B) Compiler Error
   - C) Undefined Behavior
   - D) Garbage Value

45. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3, 4, 5};
       int *ptr = arr + 2;
       
       printf("%d\n", *(ptr + 1));
       
       return 0;
   }
   ```
   **Output:**
   - A) 2
   - B) 3
   - C) 4
   - D) Garbage Value

46. **Question:**
   ```c
   #include <stdio.h>
   
   void func(int *ptr) {
       *ptr += 10;
   }
   
   int main() {
       int arr[] = {1, 2, 3};
       func(arr);
       printf("%d\n", arr[0]);
       
       return 0;
   }
   ```
   **Output:**
   - A) 1
   - B) 11
   - C) Compiler Error
   - D) Undefined Behavior

47. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int arr[] = {1, 2, 3, 4, 5};
       int *ptr1 = arr + 1;
       int *ptr2 = arr + 3;
       
       printf("%d\n", ptr2 - ptr1);
       
       return 0;
   }
   ```
   **Output:**
   - A) 1
   - B) 2
   - C) 3
   - D) 4

48. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int x = 5;
       int *ptr1 = &x;
       int **ptr2 = &ptr1;
       
       printf("%d\n", **ptr2);
       printf("%d\n", *ptr1);
       printf("%p\n", *ptr2);
       
       return 0;
   }
   ```
   **Output:**
   - A) 5, 5, Address of x
   - B) 5, Address of x, Address of ptr1
   - C) Compiler Error
   - D) Undefined Behavior

49. **Question:**
   ```c
   #include <stdio.h>
   
   int main() {
       int x = 5;
       int *ptr = &x;
       
       printf("%p\n", (void *)ptr);
       ptr = (int *)((char *)ptr + 1);
       printf("%p\n", (void *)ptr);
       
       return 0;
   }
   ```
   **Output:**
   - A) Address of x, Address of x + 1
   - B) Address of x, Address of x + sizeof(int)
   - C) Compiler Error
   - D) Undefined Behavior

50. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        printf("%d\n", *(ptr++));
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5, Garbage Value
    - B) 5, 5
    - C) Garbage Value, Garbage Value
    - D) Compiler Error

51. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 2;
        
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

52. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr1, *ptr2;
        
        ptr1 = &x;
        ptr2 = ptr1;
        (*ptr1)++;
        
        printf("%d %d\n", *ptr1, *ptr2);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5 5
    - B) 6 5
    - C) 5 6
    - D) Compiler Error

53. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr;
        
        printf("%d\n", *(ptr + 5));
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value

54. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int x = 5;
        int *ptr = &x;
        
        printf("%d\n", *ptr++);
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 5, Garbage Value
    - B) 5, 5
    - C) Garbage Value, Garbage Value
    - D) Compiler Error

55. **Question:**
    ```c
    #include <stdio.h>
    
    int main() {
        int arr[] = {1, 2, 3};
        int *ptr = arr + 2;
        
        printf("%d\n", *ptr);
        
        return 0;
    }
    ```
    **Output:**
    - A) 1
    - B) 2
    - C) 3
    - D) Garbage Value
