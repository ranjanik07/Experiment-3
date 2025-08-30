### NAME: RANJANI K

### REG NO.: 212224230220
# Experiment-3
## PRIME NUMBER OR NOT

# Aim: Write a python program to check the number is prime or not and inspect for failures. 

# Algorithm
1. Start the program.
2. Get the number to be checked from the user.
3. If the number is less than or equal to 1, return "Not Prime".
4. If the number is 2, return "Prime".
5. Start the iteration from 3, For each iteration:
 - If the number is divisible by the current iteration value, return "Not Prime".
6. If the number is not divisible by any value from 2 to the square root, return "Prime".
7. Stop the program. 

## Program
```
def is_prime(n):
    if not isinstance(n, int):
        raise TypeError("Input must be an integer.")
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False
    for i in range(3, int(n**0.5) + 1, 2):
        if n % i == 0:
            return False
    return True


try:
    num = int(input("Enter a number: "))
    if is_prime(num):
        print(f"{num} is a prime number.")
    else:
        print(f"{num} is not a prime number.")

except ValueError:
    print("Input Error: Please enter a valid integer.")
except Exception as e:
    print("Unexpected Error:", e)
```
## Output
<img width="758" height="83" alt="Screenshot 2025-08-30 102808" src="https://github.com/user-attachments/assets/ebd40dbc-3aaa-4f13-b967-ec020766cb1a" />
<img width="760" height="77" alt="Screenshot 2025-08-30 102854" src="https://github.com/user-attachments/assets/e6b6db15-e9ce-48fe-b01b-62b087aa55b3" />
<img width="758" height="105" alt="Screenshot 2025-08-30 103255" src="https://github.com/user-attachments/assets/a2f0348c-52f7-4a78-bd85-2a199368fe56" />

## Result
Thus, the python program to check the number is prime or not is implemented and the output is verified successfully.
