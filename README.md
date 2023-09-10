# python-AI-8-
python+AI笔记(8)
# 一阶-四章-for循环的嵌套使用
#坚持表白100天，每天送10朵花
i=0  #打印用在for循环的i变量，需要提前定义
name="abcdefghijk..."  #打100个字符让for循环跑，这种不好使
for i in range(1,101):
    print(f"今天是想小美表白的第{i}天,还有坚持")

#写内层循环
    for j in range(1,11):
        print(f"给小美送的{j}朵玫瑰花")
    print("小美，我喜欢你")
print(f"第{i}天，表白成功")

# 一阶-四章-for循环打印九九乘法表
#通过外层循环控制行数
fir i in rannge(1,10):
    #通过内层循环控制每一行的输出
    for j in range(1,i+1)
        #在内层循环中输出每一行的内容
        print(f"{j}*{i}={j*i}\t",end='')
#外层循环需要输出一个回车
print()

# 一阶-四章-continue和break
#continue后面的代码都不会被执行，跳到下一个循环
for i in range(1,6):
    print("语句1")
    continue
    print("语句2")
#结果打印5个语句1

#continue的嵌套应用
for i in range(1,6):
    print("语句1")
    for j in range(1,6):
        print("语句2")
        continue
        print("语句3")
    print("语句4")
#输出结果为一个语句1，5个语句2，1个语句4为一个循环

#遇到break，整个循环game over
for i in range(1,101):
    print("语句1")
    break
    print("语句2")
print("语句3")
#输出的结果是语句1和语句3各输出一遍

#break在嵌套循环中的应用
for i in range(1,6):
    print("语句1")
    for j in range(1,6):
        print("语句2")
        break
        print("语句3")
    print("语句4")
#输出结果为语句1，2，4各输出5次

# 一阶-四章-循环综合案例
money=10000
for i in range(1,21):
    import random
    score=random.randint(1,10)
    if score<5:
        print(f"员工{i}绩效分{score}，不满足，不发工资，下一位")
        continue
    if money>=1000:
        money-=1000
        money(f"员工{i}，满足条件发放1000，公司账户余额为{money}")
    else:
        print(f"余额不足，当前余额：{money}元，不足以发工资，不发了，下个月再来")
        break

# 一阶-四章-函数的初体验
str1="itheima"
str2="itcast"
str3="python"

#定义一个技术的变量
count=0
for i in str1:
    count+=1
print(f"字符串{str1}的长度是:{count}")

count=0
for i in str2:
    count+=1
print(f"字符串{str2}的长度是:{count}")

count=0
for i in str3:
    count+=1
print(f"字符串{str3}的长度是:{count}")

#可以使用函数来优化这个过程
#封装函数
def my_len(data):
    count=0
    for i in data:
        count+=1
    print(f"字符串{data}的长度是{count}")

my_len(str1)
my_len(str2)
my_len(str3)
