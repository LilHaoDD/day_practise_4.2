# day_practise_4.2
daily practice and learning 4. 2
#day4.2
try:
    a = eval(input('number='))
    print(a*2)
except NameError:
    print('wrong')
    
try:
    i=eval(input('number:'))
    a=[1,2,3,4,5,6,7,8,9,10]
    print(a[i])
except NameError:
    print('wrong')
except:
    print('bad')


a=[]
for i in range(10):
    a.append(i)
else:
    print('NN')
print(a)


try:
    a='abcdefghijk'
    b=eval(input('number:'))
    print(a[b])
except NameError:
    print('wrong')
else:
    print('nothing')
finally:
    print('bad nothing')



#practice 1
import random as rd
r = rd.randint(0,9)
i=0
a=eval(input('请输入：'))
while (a != r):
    if a < r:
        print('遗憾，太小了')
        i += 1
        a=eval(input('请重新输入：'))
    elif a > r:
        print("遗憾，太大了")
        i += 1
        a = eval(input('请重新输入：'))
else:
    print('预测{}次，你猜中了！'.format(i+1))
    

while(True):
    a = eval(input('请输入：'))
    if a > r:
        print('big')
        i+=1
    if a < r:
        print('small')
        i+=1
    if a == r:
        print('right{}'.format(i+1))
        break

# practice 2
a = input('一串字符：')
alp,num,el,other = 0,0,0,0
for i in range(len(a)):       #  for i in a  同样的道理，遍历整个字符串
    if (ord('a') <= ord(a[i]) <= ord('z')) or (ord('A') <= ord(a[i]) <= ord('Z')):   # ord() 求 ASCII 码
        alp += 1
    elif ord('0') <= ord(a[i]) <= ord('9'):
        num += 1
    elif a[i] == ' ':
        el += 1
    else:
        other += 1
print('{}{}{}{}'.format(alp,num,el,other))

#practice_3
import math
a,b = eval(input('请输入两个数字'))
c = math.gcd(a,b)
d=a*b/c
print(c,d)

b,s = eval(input('请输入两个数字'))
tmp=0
if s > b:
    tmp = b
    b=s
    s=tmp
while b%s != 0:
    t = b % s
    b = s
    s = t
d = s*b/s
print('最大公倍数是{}，最大公约数是{}'.format(d,s))


import random as rd
r = rd.randint(0,100)
i = 0
try:
    guess = eval(input('请输入一个整数：'))
except:
    print('输入内容必须为整数！')
    guess = eval(input('重新输入一个数字：'))
while guess != r:
    if guess < r:
        print('遗憾，太小了')
        i += 1
    elif guess > r:
        print('遗憾，太大了')
        i += 1
        try:                                                  #  重复判断是否为整数？
        guess = eval(input('请输入一个整数：'))
    except:
        print('输入内容必须为整数！')
        guess = eval(input('重新输入一个数字：'))
        i += 1
print('预测{}次，恭喜你猜对了'.format(i+1))


#羊车门问题！！！
import random as rd
n=0
after_change,no_change=0,0
k=eval(input('times:'))
for i in range(k):
    car=rd.randint(1,3)
    guess=rd.randint(1,3)
    if car == guess:
        no_change += 1
    else:
        after_change += 1
print('{:.4f},{:.4f}'.format(no_change/k,after_change/k))

