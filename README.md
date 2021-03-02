# Multiple choise question sample in pyhton 
from Question import Question
questions_prompt = [
                   "What is the color of an appple ? \n (a) Green\n (b) Orange\n (c) Yellow", 
                   "What is the color of an orange ? \n (a) Green\n (b) Orange\n (c) Yellow", 
                   "What is the color of an banana ? \n (a) Green\n (b) Orange\n (c) Yellow"] 
def run_test(questions):
    score = 0
    for question in [ Question(questions_prompt[0], "a"), Question(questions_prompt[1], "b"), Question(questions_prompt[2], "c")]: 
        answer = input(question.prompt)
        print(answer)
        if answer == question.answer:
            score = score + 1 
    print("you score {} ".format(float(score)/3))
    if float((score)/3) >= 0.66:
        print("you pass")
    else: 
       print( "You failed")
run_test(Question)

