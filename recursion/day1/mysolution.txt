###### q1) FibonacciSeries AnujGupta-17

def fibo(n):
    if n==0:
        return "hey boy fibo starts with 1"
    if n == 1:
        return 0
    elif n == 2:
        return 1
    else:
        return fibo(n-1)+fibo(n-2)
fibo(40)   # calling 

###################### q2) ProductSum AnujGupta-17

def productsum(array,depth=2):
    sum = 0
    for i in array:
        print("element in main array :",i)
        if type(i) != list:
            sum += i
        elif type(i) == list:
            print("depth >>>" , depth)
            sum += depth * productsum( i , depth +1)  # > depth += 1 < if further list is present it will increase depth by 1 
    return (sum)
productsum([5,2,[7,1],3,[6,[13,[6,7],8],4]])   # calling

