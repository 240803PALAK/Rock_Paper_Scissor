# Rock_Paper_Scissor

    import random
    userpoint=0
    systempoint=0
    def system_choice():
        option=['scissor','rock','paper']
        choice=random.choice(option)
        return choice
    def user_choice():
        choice=input("Enter your choice(Rock/Paper/Scissor): ")
        return choice
    def result(user,system):
        global userpoint,systempoint
        if (user=='scissor'and system=='paper')or(user=='rock' and system=='scissor') or (user=='paper'and system=='rock'):
            userpoint+=1
        elif (system=='scissor'and user=='paper')or(system=='rock' and user=='scissor') or (system=='paper'and user=='rock'):
            systempoint+=1
        else:
            pass
    for i in range(1,6):
        print(f"---------- Round {i} ----------\n")
        user=user_choice()
        system=system_choice()
        print(f"User : {user}, System: {system}\n")
        result(user,system)
    
    if userpoint<systempoint:
        result="System Won"
    elif userpoint==systempoint:
        result="It's a tie"
    else:
        result="You Won"
    print(f"-------------------------------------------------- {result} --------------------------------------------------")
