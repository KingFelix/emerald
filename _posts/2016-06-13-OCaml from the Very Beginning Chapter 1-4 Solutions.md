Please let me know in the comments if you find any errors!

## Chapter 1

1. * int; 17. Evaluating an int will return the same int.
      
    * int; 11. Multiplication has precedence over addition.
      
    * int; 1. Operators in OCaml are left associative.
      
    * bool; true. Four hundred is greater than two hundred.
      
    * bool; false. One is equal to one.
      
    * bool; true. The or operator requires only one argument to be true in order for the expression to be true.
      
    * bool; false. The and operator requires only one argument to be false in order for the expression to be false.
      
    * bool; false. Since the argument for the if statement is true, the expression will return false.
      
    * char; '%'. Evaluating a char will return the same char.
      
    * char; Syntax error. The plus operator does not take chars as operands.

2. The mod operator has precedence over the + operator.

3. This expression evaluates to 11, as the * operator has precedence over the + operator.

4. min_int evaluates to -4611686018427387904 while max_int evaluates to 4611686018427387903. Nothing is returned when max_int + 1 or min_int - 1 are evaluated.

5. An exception is thrown by the compiler because division by zero is undefined.

6. If one or both of the operaters is negative, zero is returned. If the first operand is zero, zero is returned. If the second operand is zero, an exception is thrown because division by zero is undefined.

7. 0 and 1 already represent the quantities zero and one in OCaml, respectively. Ambiguities would arise if they carried on this additional meaning.

8. Comparison operators compare characters by alphabetical order and they compare boolean values with precedence given to true.

## Chapter 2.

1. ```
    let timesTen a = 10 * a;; 
    ```
   
    The function is of type integer.


2.  ```
     let notZero a b =
        if a <> 0 && b <> 0 then true else false;;
    ```
     The function is of type bool.

3.  ```
     let rec sum n =
        if n > 1 then n + sum (n-1) else n;;
    ```
       The function is of type int.

4. ```
    let rec power x n =
        if n > 1 then x * power x (n-1) else x;;
    ```
	 The function is of type int.

5. ```
    let isconsonant a =
        a <> 'a' && a <> 'e' && a <> 'i' && a <> 'o' && a <> 'u';;
    ```
6. The first x is unused, giving "Warning 26: unused variable x." The result of the expression is 4.

7. Write a precondition stating that a > 0. If a < 0, return an error. 

## Chapter 3.

1. ```
    let notRewrite a =
     match a with
        true -> false
      | false -> true;;
    ```
    
2. ```
    let rec func n =
    match n with
       1 -> 1
     | _ -> n + func (n-1);;
    ```
    
3. ```
    let rec power x n =
     match n with
       1 -> x
     | _ -> x * power x (n-1);;
    ```
    
4. I believe all of the functions are easier to read with pattern matching, and the difference in complexity becomes much more noticeable as function size increases.

5. This evaluates to 5.

6. ```
    let islower a =
     match a with
       'a'..'z' -> true
     | 'A'..'Z' -> false;;

   let isupper a =
     match a with
       'a'..'z' -> false
       'A'..'Z' -> true;;
    ```
    
## Chapter 4.

1. ```
 let rec evens l =
     match l with
       _::a::t -> a :: evens t
     | _ -> [];;
    ```
This function is of type 'a list.

2. ```
    let rec count_true l =
     match l with
       [] -> 0
     | false::t -> 0 + count_true t
     | true::t -> 1 + count_true t;;

   let rec count_true_inner l n =
     match l with
       [] -> n
     | false::t -> count_true_inner t n
     | true::t -> count_true_inner t (n+1);;

   let count_true l = count_true_inner l 0;;
    ```
This function is of type int.

3. ```
    let rec rev l =
     match l with
       [] -> []
     | h::t -> rev t @ [h];;

   let rec drop n l =
     if n = 0 then l else
       match l with
	 [] -> []
	| h::t -> drop (n-1) t;;

   let palindrome l = l @ (drop 1 (rev l));;

   let rec ispalindrome l =
     if l = palindrome l || l = [] then true else false;;
    ```
    
4. ```
    let rec drop_last l =
     match l with
      [] -> []
    | h::[] -> []
    | h::t -> h :: drop_last t;;

   let rec drop_last_inner l n =
     match l with
       [] -> []
     | h::[] -> n
     | h::t -> drop_last_inner t (n @ [h]);;

   let drop_last l = drop_last_inner l [];;
    ```
    
5. ```
    let rec member e l =
     match l with 
       h::t when h = e -> true
     | _::t -> member e t
     | [] -> false;;
    ```
6.  ```
    let rec make_set_inner l m =
     match l with
       h::t when member h m = false -> make_set_inner l (m @ [h])
     | _::t -> make_set_inner t m
     | [] -> m;;  
    
    let make_set l = make_set_inner l [];;
    ```
    The function is of type `a list.
7. The runtime of the rev function is O(n), that is, it increases proportionally with the number of elements. You can write a more efficient version using an accumulating argument:
```
let rec rev_inner l m =
  match l with
    [] -> m
  | h::t -> rev_inner t ([h] @ m);;

let rec rev l = rev_inner l [];;
```
The runtime remains the same as before at O(n), but the space efficiency is now O(1).