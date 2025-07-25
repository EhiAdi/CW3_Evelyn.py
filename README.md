# CW3_Evelyn.py
My resit CW3
def accept_input():
    student_id = input("Student's ID or Name: ")
    coursework1 = float(input("Coursework 1 score: "))
    coursework2 = float(input("Coursework 2 score: "))
    coursework3 = float(input("Coursework 3 score: "))
    test_score = float(input("Test score: "))
    
    return student_id, coursework1, coursework2, coursework3, test_score
    #This code block accepts inputs from students 

def calculate_overall_score (coursework1, coursework2, coursework3, test_score):
    overall_score = (coursework1 * 0.10) + (coursework2 * 0.20) + (coursework3 * 0.30) + (test_score * 0.40)
    return overall_score
    # In this block the overall score for each student is calculated

def determine_category (overall_score):
    if overall_score == 100:
            return "Aurum Standard"
    elif overall_score >= 88.5 and overall_score < 100:
            return "Upper First"
    elif overall_score >= 83.5 and overall_score < 88.5:
            return "Upper First"
    elif overall_score >= 80 and overall_score < 83.5:
            return "Upper First"
    elif overall_score >= 76.5 and overall_score < 80:
            return "First"
    elif overall_score >= 73.5 and overall_score < 76.5:
            return "First"
    elif overall_score >= 70 and overall_score < 73.5:
            return "First"
    elif overall_score >= 66.5 and overall_score < 70:
            return "Upper Second"
    elif overall_score > 63.5 and overall_score < 66.5:
            return "upperr Second"
    elif overall_score >= 60 and overall_score < 63.5:
            return "Upper Second"
    elif overall_score >= 56.5 and overall_score < 60:
            return "Lower Second"
    elif overall_score > 53.5 and overall_score < 56.5:
            return "Lower Second"
    elif overall_score >= 50 and overall_score < 53.5:
            return "Lower Second"
    elif overall_score >= 46.5 and overall_score < 50:
            return "Third"
    elif overall_score >= 43.5 and overall_score < 46.5:
           return "Third"
    elif overall_score >= 40 and overall_score < 43.5:
            return "Third"
    elif overall_score >= 36.5 and overall_score < 40:
            return "Condonable Fail"
    elif overall_score >= 33.5 and overall_score < 36.5:
            return "Condonable Fail"
    elif overall_score >= 28.5 and overall_score < 33.5:
            return "Condonable Fail"
    elif overall_score >= 20 and overall_score < 28.5:
            return "Fail"
    elif overall_score >= 10 and overall_score < 20:
            return "Fail"
    elif overall_score >= 1 and overall_score < 10:
            return "Fail"
    elif overall_score == 0 :
            return "Defecit Opus"
    else:
            return "THIS IS AN INVALID SCORE"
    # The IF block above is used to categorizes students final score

def main():
    students = []
    
    while True:
        student_data = accept_input()
        student_id, coursework1, coursework2, coursework3, test_score = student_data
        
        total_score = calculate_total_score(coursework1, coursework2, coursework3, test_score)
        category = student_category(total_score)
        # This block is the programes main loop
        
        students.append((student_id, int(total_score), category))
        break
         # This block stores data the student has entered 
            
    
    print("\nStudent Results:")
    for student in students:
        student_id, score, category = student
        print(f"Student's ID/Name: {student_id}, Score: {score} - {category}")
        # This block prints out the result

if __name__ == "__main__":
    main()

