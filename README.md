# Correct_Answers

def main():
    # open file answers.txt
    afile = open("answers.txt","r")]
    # set total amount and passing amount
    num_questions = 25
    pass_num = 18


    # initialize anwers value
    answers = []
    # allow the answers file to be changed
    for line in afile:
        answers.append(line.rstrip())


    # print(answers)
    
    # open student files
    sfile = open("student_answers.txt",'r')
    # initialize student score value
    student = []
    for line in sfile:
        student.append(line.rstrip())

    
    # initialize the amount correct
    correct = 0

    # look at the 25 answers 
    for i in range(0, 25):
        #determine in the answers match
        if answers[i] == student[i]:
            correct += 1
        # if they don't match print the ones that are incorrect
        else:
            print("Incorrect %d" % (i+1))

    # display the amount correct
    print("Correct %d" % correct)
    # display the amount that is incorrect
    print("Incorrect %d" % (num_questions - correct))

    # display to user if they passed or failed
    if correct >= pass_num:
        print("you pass")

    else:
        print("you failed")


main()
