# Confined Calories
By Harrison Owens and Delaynie Gorgan
# A system that counts your calories and keeps the data as secure as possible. Who wants other people to know what they're eating?

Confined Calories is the most secure fitness application for counting calories and helping you manage your goals.

The user can enter their food throughout the day and keep track of their calories.
The application opens when the user enters a passcode. Nothing is saved in the Cloud. 
Everything is stored where the user knows it is and can find it.
Today, private information is not as private as most people would like to believe. 
That can be very frightening when everyone is trying to work on themselves but aren't ready to share their journey with others.
Confined Calories makes sure that you share your goals on your terms.
'''
This is where users will track their progress or how well they met their daily goals after logging calories input.
'''
#import libraries first
import statistics as s

#add constants next
admins = {'jasmine':'abc123','david':'ABC123'}

students = {'Alex':[87,88,98],
            'Sally':[88,67,93],
            'Nboke':[90,88,78]}
food = {'chicken':[90, 0, 60, 100, 0, 22]}
#now define functions
def view_nutrition():
    print("Hi")
    for foods in food:
        calories = foods[food,0]
    print(str(calories))
def calorie_goal():
    name_user = input('User name: ')
    goals_met_today = input('Score: ')

    if name_user in users:
        print('Adding score for'+ name_user)
        users[name_user].append(float(goals_met_today)) #float will have a .0
        print(str(name_user) + ' Did this well meeting their goal today:')
        print(users[name_user])
    else:
        print('User not found. Please check your spelling or go back and add if new.')

def remove_users():
    name_remove = input('Who do you want to remove? ')
    if name_remove in users:
        print('Removing '+ name_remove)
        del users[name_remove]
        print(users)
    else:
        print('User not found.')

def average_users():
    for user in users:
        scores = users[user]
        average = s.mean(scores)
        print(user,' Your Scores is ',average)

def main():
    print("User: " + login)
    print("""
    Welcome to the Calorie Count

    [1] - Enter Scores
    [2] - Remove User
    [3] - User Scores
    [4] - Exit
    [5] - View Nutrition Info
    """)

    action = input('What would you like to do? (Enter a number) ')

    if action == '1':
        #print('1 selected')
        enterGrades()
    elif action == '2':
        #print('2 selected')
        removeStudent()
    elif action == '3':
        #print('3 selected')
        averageStudents()
    elif action == '4':
        #print('4 selected')
        exit()
    elif action == '5':
        viewnutrition()
    else:
        print('Valid option not selected.') #need to cause it to reprompt

login = input('User: ')
password = input('Password: ')

if login in admins:
    if admins[login] == password:
        print('Welcome to Confined Calories,',login)
        #now run the code
        while True:
            main()
    else:
        print('Invalid password.')
else:
  print('Invalid user.')

    print('Invalid user.')
