from datetime import datetime

def chatbot():
    print("Hi! I'm ChatBot. Type 'bye' to exit.")
    while True:
        user_input = input("You: ").lower()

        
        if any(greet in user_input for greet in ['hello', 'hi', 'hey']):
            print("Bot: Hello! How can I help you today?")
        
        
        elif 'name' in user_input:
            print("Bot: I'm a simple chatbot created to answer your questions.")
        
        
        elif 'how are you' in user_input:
            print("Bot: I'm just a bot, but I'm doing fine! Thanks for asking.")
        
        
        elif 'help' in user_input:
            print("Bot: I can tell you the time, date, do simple math, and answer some general knowledge questions.")
        
        
        elif 'time' in user_input:
            print("Bot: Current time is", datetime.now().strftime("%H:%M:%S"))
        
        
        elif 'date' in user_input:
            print("Bot: Today's date is", datetime.now().strftime("%Y-%m-%d"))
        
        
        elif any(op in user_input for op in ['+', '-', '*', '/']):
            try:
                result = eval(user_input)
                print("Bot: The result is", result)
            except Exception:
                print("Bot: Sorry, I couldn't understand that calculation.")
        
        
        elif 'capital of france' in user_input:
            print("Bot: The capital of France is Paris.")
        
        elif 'largest planet' in user_input:
            print("Bot: The largest planet in our solar system is Jupiter.")
        
        elif 'who is the president of india' in user_input:
            print("Bot: As of 2025, the President of India is Droupadi Murmu.")
        
        elif 'speed of light' in user_input:
            print("Bot: The speed of light is approximately 299,792 kilometers per second. ")
        
        elif 'highest mountain in the world' in user_input:
            print("Bot: The highest mountain in the world is Mount Everest.")
        
        elif 'who invented the telephone' in user_input:
            print("Bot: Alexander Graham Bell is credited with inventing the telephone.")
        
        elif 'who was the first president of the united states' in user_input:
            print("Bot: The first President of the United States was George Washington.")
        
        elif 'earth' in user_input and 'diameter' in user_input:
            print("Bot: The diameter of the Earth is approximately 12,742 kilometers.")
        
        elif 'how many continents are there' in user_input:
            print("Bot: There are seven continents on Earth: Asia, Africa, North America, South America, Antarctica, Europe, and Australia.")
        
        elif 'bye' in user_input:
            print("Bot: Goodbye! Have a great day.")
            break
        
       
        else:
            print("Bot: I'm sorry, I didn't understand that. I can help you with time, date, math, or general knowledge questions. Try asking something like 'capital of Japan' or 'what's 5 + 3?'")


chatbot()
