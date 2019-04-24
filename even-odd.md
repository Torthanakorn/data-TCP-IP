# Even-Odd
    code
    n = int(input("even-odd : " ))
    if n == 1:
        data = input("data : ")
        b = 0
        for i in data:
            if i == '1':
                b = b+1 
        print('check',b)            
        if b % 2 == 1:
            print("even : ""1"+data)
        else :
            print("even : ""0"+data)
    elif n == 0:
        data = input("data : ")
        r = 0
        for i in data:
            if i == '0':
                r = r+1 
        print('check',r)            
        if r % 2 == 0:
            print("odd : ""1"+data)
        else :
            print("odd : ""0"+data

# de end