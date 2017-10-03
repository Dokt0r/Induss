a=[int(i) for i in input().split()]
i =0
d=[]
b=len(a)-1
if b==1:
    print(a)
if len(a)==2:
    c=a[0]+a[1]
    d.append(c)
    c = a[0] + a[1]
    d.append(c)
    print(*d)
if len(a)!=1:
    for i in range(0,b):
        if i==0:
            c = a[i+1] + a[-1]
            d.append(c)
        elif 0 < i < b:
            c = a[i - 1] + a[i + 1]
            d.append(c)
        elif i==b:
            c=a[i-1]+a[0]
            d.append(c)
        i+=1
    print(*d,end='')
