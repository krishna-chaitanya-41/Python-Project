def is_prime(n):
    for i in range(2, n):
        if (n % i) == 0:
            return False
    return True


c = 'y'
while c in 'YyYesyes':

    a = int(input("Enter a Nth Number:"))
    c = 0
    b = 0
    num = 2
    while c != a:
        num2 = 0
        num1 = num
        while num1 != 0:
            r = num1 % 10
            num1 //= 10
            num2 = num2 * 10 + r
            if num == num2 and is_prime(num):
                c += 1
                b = num
        num = num + 1
    print(a, "th Prime Palindrome Number is ", b)
    c = input('Do you want to continue(Y/N): ')

print('THANKS FROM Group 19')
