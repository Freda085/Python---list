# Python---list
請問哪裡錯了?謝謝!
<!-- 實作一個函式，函式的回傳值為原串列相同index兩個數字的最大公因數，回傳的型態為串列 -->
def gcd(l1, l2):
    ### l1 和 l2 的型態為串列(list)
    ### 請在下面開始你的程式
    a=[]
    b=0
    for i in range(len(l1)):
        if int(l1[i])>=int(l2[i]):
            b=int(l2[i])
            if (int(l1[i])%b==0)and (int(l2[i])%b==0):
                a.append(b)
            while (int(l1[i])%b!=0)or (int(l2[i])%b!=0):
                b=b-1
                if (int(l1[i])%b==0)and(int(l2[i])%b==0):
                    a.append(b)
                    break
        else:
            b=int(l1[i])
            if (int(l1[i])%b==0)and(int(l2[i])%b==0):
                a.append(b)
            while (int(l1[i])%b!=0)or (int(l2[i])%b!=0):
                b=b-1
                if (int(l1[i])%b==0)and (int(l2[i])%b==0):
                    a.append(b)
                    break
            
    return a
    
l1=input()
l1=[int(k) for k in l1]
l2=input()
l2=[int(m) for m in l2]
print(gcd(l1, l2))
