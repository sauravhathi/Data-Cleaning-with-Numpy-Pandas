# Problem4 Prestigious Event

# PROBLEM

## Prestigious Event

Sunil, a popular event manager in the city maintains many events and all their details that happen in and outside the city. He is always concerned about the crowd that gathered in his events so always he uses a crowd tracker which gives him the strength of the crowd gathered in his events.

At the end of the year, for the betterment of his business in next year he invites all his customers whose events he organizes in that year and discusses upcoming events from them.

Sunil thought it will be a great initiative if he awards an event as a prestigious event in that meeting based on the crowd that gathered in the events. But as we know, manual analyzing of the event details is tedious work. Tomorrow is his meeting with his customers; help him in writing a code which would ease his work.

Given the crowd strength of the events, display the events by sorting them in the descending order and display which event can be awarded as the Prestigious Event.

**Input Format:**

The input consists of an integer 'n' indicating the number of events scheduled.
The next n lines of the input consist of the Event name and the corresponding registrations for that event.

**Output Format:**

The output displays all the **events in descending order** along with the **crowd strength**.
The next line of the output displays the event name which has the **maximum strength** and can be awarded as the Prestigious event.
**Print Invalid Input and terminate the program if the number of registration is lesser than 0.**
Refer the Sample Input and output for format specifications.

**Sample Input - Output :**

Enter the number of events scheduled

8

Event Name

Marriage

Number of registration

25000

Event Name

New Year concert

Number of registration

150000

Event Name

Birthday party

Number of registration

1500

Event Name

Reception

Number of registration

2500

Event Name

Promotion

Number of registration

200

Event Name

House Warming

Number of registration

500

Event Name

Get together

Number of registration

100

Event Name

Birthday party

Number of registration

350

---

event population

1 New Year concert 150000

0 Marriage 25000

3 Reception 2500

2 Birthday party 1500

5 House Warming 500

7 Birthday party 350

4 Promotion 200

6 Get together 100

Prestigious Event is New Year concert

```
import numpy as np
def main():
    n = int(input("Enter the number of events scheduled"))
    events = np.empty([n, 2], dtype=object)
    for i in range(n):
        events[i, 0] = input("\nEvent Name")
        events[i, 1] = int(input("\nNumber of registration"))
    if events[:, 1].min() < 0:
        print("Invalid Input")
        return
    print("\n     event  population")
    lists = []
    for i in range(n):
        lists.append([i, events[i, 0], events[i, 1]])
    lists.sort(key=lambda x: x[2], reverse=True)
    for i in range(n):
        print(lists[i][0], "   ", lists[i][1], "      ", lists[i][2])
    print("Prestigious Event is ", lists[0][1])

main()
```
