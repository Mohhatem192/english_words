import random
words = {"Absence":"The lack or unavailability of something or someone.",
"Approval":"Having a positive opinion of something or someone.",
"Answer":"The response or receipt to a phone call, question, or letter.",
"Attention":"Noticing or recognizing something of interest.",
"Amount":"A mass or a collection of something",
"Borrow":"To take something with the intention of returning it after a period of time.",
"Baffle":"An event or thing that is a mystery and confuses.",
"Ban":"An act prohibited by social pressure or law.",
"Banish":"Expel from the situation, often done officially.",
"Banter":"Conversation that is teasing and playful.",
"Characteristic":"referring to features that are typical to the person, place, or thing.",
"Cars":"Four-wheeled vehicles used for traveling.",
"Care":"extra responsibility and attention.",
"Chip":"a small and thin piece of a larger item.",
"Cease":"to eventually stop existing.",
"Dialogue":"A conversation between two or more people.",
"Decisive":"a person who can make decisions promptly.",
}
message = '''1. Review random random
2. Test yourself
3. Exit'''
while True:
  print(message)
  choice = int(input('Enter your choice: '))
  if choice == 1:
    word = random.choice(list(words))
    print(f'Word: {word}')
    print(f'Definition: {words[word]}')
  elif choice == 2:
    word = random.choice(list(words))
    print(f'Definition: {words[word]}')
    answer = input('Enter the word: ')
    if answer.capitalize() == word:
      print('Correct answer')
    else:
      print('Wrong answer you have one more attempt')
      answer = input('Enter the word: ') 
      if answer.capitalize() == word:
        print('Correct answer')
      else:
        print('Wrong word')
  elif choice == 3:
    print('Have a nice day')
    break
  else:
    print('Please enter a vaild number')
