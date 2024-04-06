``` python
# -*- coding: utf-8 -*-
"""
Created on Fri Apr  5 19:58:54 2024

@author: LENOVO
"""

import datetime
import random

def getBirthdays(numberOfBirthdays):
    birthdays = []
    for i in range(numberOfBirthdays):
        startOfYear = datetime.date(2001, 1, 1)
        randomNumbersOfDays = datetime.timedelta(random.randint(0, 364))
        birthday = startOfYear + randomNumbersOfDays
        birthdays.append(birthday)
    return birthdays

def getMatch(birthdays):
    for a, birthdayA in enumerate(birthdays):
        for birthdayB in birthdays[a + 1:]:
            if birthdayA.day == birthdayB.day and birthdayA.month == birthdayB.month:
                return birthdayA
    return None

print('''Birthday Paradox, by Al Sweigart al@inventwithpython.com
The birthday paradox shows us that in a group of N people, the odds
that two of them have matching birthdays is surprisingly large.
This program does a Monte Carlo simulation (that is, repeated random
simulations) to explore this concept.

(It's not actually a paradox, it's just a surprising result.)
''')

MONTHS = ('Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun',
          'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec')

while True:
    print('How many birthdays shall I generate? (Max 100)')
    response = input('> ')
    if response.isdecimal() and (0 < int(response) <= 100):
        numBDays = int(response)
        break

print('\nHere are', numBDays, 'birthdays:')
birthdays = getBirthdays(numBDays)
for i, bday in enumerate(birthdays):
    if i != 0:
        print(',  ', end='')
    monthName = MONTHS[bday.month - 1]
    dataText = '{} {}'.format(monthName, bday.day)
    print(dataText, end='')

print('\n')

match = getMatch(birthdays)

print('In this simulation, ', end='')

if match != None:
    monthName = MONTHS[match.month - 1]
    dateText = '{} {}'.format(monthName, match.day)
    print('multiple people have a birthday on', dateText)
else:
    print('there are no matching birthdays.')

print('\nGenerating', numBDays, 'random birthdays 100,000 times...')
input('Press enter to begin...')

print("Let's run another 100,000 simulation.")

simMatch = 0
for i in range(100000):
    if i % 10000 == 0:
        print(i, 'simulation run...')
    birthdays = getBirthdays(numBDays)
    if getMatch(birthdays) != None:
        simMatch = simMatch + 1

print('100,000 simulations run.')

probability = round(simMatch / 100000 * 100, 2)
print('Out of 100,000 simulations of', numBDays, 'people, there was a')
print('matching birthday in that group', simMatch, 'times. This means')
print('that', numBDays, 'people have a', probability, '% chance of')
print('having a matching birthday in their group.')
print("That's probably more than you would think!")

```
