# Moodspark
A small Python project that sparks positivity by giving quotes based on your mood.
import random

moods = {
    "happy": ["Happiness is contagious, spread it!"],
    "sad": ["This too shall pass."],
    "tired": ["Rest, but don’t quit."]
}

# Counter to track attempts
attempts = 0
max_attempts = 2

while attempts < max_attempts:
    user_mood = input("How are you feeling today? ").strip().lower()
    found = False
    
    for mood in moods:
        if mood in user_mood:
            print(random.choice(moods[mood]))
            found = True
            break
    
    if found:
        break  # exit loop if mood recognized
    
    attempts += 1
    if attempts == 1:
        print("Hmm, I don’t recognize that mood.")
        print("Try entering moods like 'happy', 'sad', or 'tired'.")
    else:
        print("It’s okay if you don’t want to share your mood.")
        print("This program is just here to cheer you up! 🙂")
        break
