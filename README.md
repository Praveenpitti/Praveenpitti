### Step 1: Define the Structure


quiz = {
    "What is the capital of France?": "Paris",
    "What is 2 + 2?": "4",
    "What is the capital of Japan?": "Tokyo",
    "What is the largest planet in our solar system?": "Jupiter",
    "Who wrote 'Romeo and Juliet'?": "Shakespeare"
}


### Step 2: Create the quiz function

def run_quiz(quiz):
    score = 0
    total_questions = len(quiz)
    
    for question, answer in quiz.items():
        user_answer = input(question + " ")
        if user_answer.strip().lower() == answer.lower():
            print("Correct!")
            score += 1
        else:
            print(f"Wrong! The correct answer is {answer}.")
    
    print(f"\nYour final score is {score} out of {total_questions}.")

# Run the quiz
run_quiz(quiz)


### Step 3: Adding Features



quiz = [
    {
        "question": "What is the capital of France?",
        "options": ["Paris", "London", "Berlin", "Madrid"],
        "answer": "Paris"
    },
    {
        "question": "What is 2 + 2?",
        "options": ["3", "4", "5", "6"],
        "answer": "4"
    },
    {
        "question": "What is the capital of Japan?",
        "options": ["Seoul", "Tokyo", "Beijing", "Bangkok"],
        "answer": "Tokyo"
    },
    {
        "question": "What is the largest planet in our solar system?",
        "options": ["Earth", "Mars", "Jupiter", "Saturn"],
        "answer": "Jupiter"
    },
    {
        "question": "Who wrote 'Romeo and Juliet'?",
        "options": ["Shakespeare", "Dickens", "Hemingway", "Twain"],
        "answer": "Shakespeare"
    }
]

def run_quiz(quiz):
    score = 0
    total_questions = len(quiz)
    
    for item in quiz:
        print(item["question"])
        for i, option in enumerate(item["options"], 1):
            print(f"{i}. {option}")
        
        user_answer = input("Your answer (1-4): ")
        
        if item["options"][int(user_answer) - 1].lower() == item["answer"].lower():
            print("Correct!")
            score += 1
        else:
            print(f"Wrong! The correct answer is {item['answer']}.")
    
    print(f"\nYour final score is {score} out of {total_questions}.")
