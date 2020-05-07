goods=['coffe','book','drink','snack','toy','wine'] #所有商品种类
user_input=input('please inptut the number which is not greater than 3 of goods you want to buy:') #让用户输入想买商品个数,个数最多是3
user_need=[]
while int(user_input)>3 or not user_input.isdigit(): #用户输入的不是只有数字或输入的数字大于3时提示用户输入一个不大于3的数字
    user_input=input('please input a digit which is not greater than 3:')
else:
    print('the types of goods are:', goods)  #用户输入为小于3的数字时打印商品的种类
    while len(user_need) < int(user_input):
        good_type=input('please input the name of good you want to buy:') #用户输入想要购买的商品名称
        if good_type in goods:   #判断用户输入的商品名称是否在商品列表中
            user_need.append(good_type)
            finsh_or_not = input('Do you finish the shopping? please input "yes" or "no":')
            if finsh_or_not == 'no': #用户选择商品后判断用户是否需要继续购买
                continue
            else:
                print('The goods you want to buy are:',user_need) #用户可随时退出购买，退出后打印所购买商品名称
                break
        else:
            print('The item you entered does not exit!') #当用户输入的商品不存在时提示用户
            continue
    else:
        print('The number of goods have reached what you want!') #用户选择的商品达到购买数量时退出并打印所购买商品名称
        print('The goods you want to buy are:',user_need)





