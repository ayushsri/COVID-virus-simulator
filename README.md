# COVID-virus-simulator
This Project topic is about how covid- 19( SARS-CoV-2 ) spread among the people,This is caused by the SARS-CoV-2 virus, which spreads between people, mainly when an infected person is in close contact with another person. When people are in direct or close contact (less than 1 meter apart) with an infected person.
Showing the comparison of spread when we implement few restrictions to people like Lockdown, tracing the people who are affected by COVID-19 to quarantine which will help in decreasing the spread of virus and also using masks while being in the public area and social distancing.
We compared the spread of 2 types of virus SARS-CoV and SARS-CoV-2, taking factors like K and R factors into consideration.
R Value: R value or the reproduction number is defined as the average number of individuals an infected person will infect over the course of the spread .
K Value: K value or the dispersion value is defined as the variance in the number of individuals an infected person will infect.
Aim of the Project :-
Stimulate the Spread of a virus such as SARS-CoV and SARS-CoV-2 . We need to take K and R factors of the disease, population density, usage and effectiveness of masks, the prevalence of testing and contact tracing to restrict the spread of virus. The goal is also to provide a GUI to interact with the application to easily alter the factors. To get a proper understanding of the virus spread we need to show graphs ,charts and mathematical relations.

Complete Project Details:- UI:-
 This the Main (1st page) , here you can select the type of virus 1. SARS-CoV 2. SARS-CoV-2
Run Button -- when you press the run button you can see a simulation of the spread in another page where white color indicates the people not affected by virus and red color indicates the people affected by virus.
As soon as you press the Run, Start and Stop will be enabled.
Start button--- when you press this button you can see the simulation of virus spread in the spread page and values of number of people affected, active number of cases, immune people, number of days and number of people dead are printed.
Stop button -- Used to stop the project.
We included 3 buttons, 1. Lockdown button --- the number of people that go out and stay in marketplaces time is decreased as well time to stay in house is increased.
Which will decrease the spread and decrease the number of active cases.
 2. Contact Tracing --- if there is an infected person that location is Quarantined, so the number of people going to that location is decreased and active cases will decrease.
3. Social Distancing --- This button will enable the social distance between two people to increase the distance (spread of people with more length ) because active cases will decrease.
We printed 2 graphs showing the the number of active cases Vs number of days
Before the Lockdown, Contact Tracing , Social Distancing is implemented and after that restrictions are implemented. There is decrease is the number of active cases
Social distance --- decrease rate of virus 10% Contact tracing --- decrease rate of virus spread 15% Lockdown --- decrease rate of virus spread 70%

  Second Page (Above ) :
This page will show the spread of the virus with white and red color differentiating the affected and non-affected people.
You can see the difference in the values and spread page how the restrictions and type of the virus affect the spread of virus in people.
Our Simulator consists of People and Places .People can move from one Place to another. There are some places which are mapped to People and some Places which are not. Initially we spread 2 infected people.

Class Definitions:-
UIstats:-
It is a class used to make JFrame and set buttons and Combo boxes.
Place:-
Place is a class used to make continuous combinations of coordinates. It is used by people and can also use to get random locations
Place1:-
It inherits the Place class and maps the people together.
Place2:-
It inherits the Place class and it is the combination of positions where people can go.
Position:-
Combination of x and y. Used to get the euclidean distance between two coordinates, places or people.
People:-
It is the class associated with human beings. It is used with all his attributes such as immunity, age, is he/she a front line worker and also associates all the methods which are related to it such as his for his/her movement, calculating immunity , selecting age etc.
CanvasHelper:-
It is the class used by Canvas to spread, people, places , spreading viruses etc.
Movement:-
It is the class used to move people and make him wait or run at a particular place
PrintConsole:-
This class is used to show data on screen such as total infected, current number of infections etc. Sars:-
It consists of various virus information such as type, fatality etc.
SimProperties:-
This class has details about viruses and other variables used in various classes.
DemoHelper:-
It is used to run the simulation. It runs in a regular interval so that it can make changes.

Mathematical formula used:-
1)We used Euclidean distance to find the distance between two places or people.
public int getEuclideanDistance(int x1,int x2,int y1,int y2) {
return (int)Math.sqrt(Math.pow(x1-x2, 2)+Math.pow(y1-y2, 2));
}
2)We used Signum function to get direction of people.
signum|x-y|.
3. 2 people are infected randomly and we have fixed number of people. We calculate the immunity of that person, using age which gives as chance of getting infected. If the chance is >1 then we infected that person if infected person comes to contact.
We fixed the time for person to stay in public and house, as soon as we implement we decrease the time person is in public which will result in decrease of spread.
4.A person gets immune after 14-21 days if the strength of the person is >1.strength is calculated using his age.
5. Person will die if his immunity is <1. After 21-25days.
6. We increase the distance when implemented social distance, the distance between the people is increased which result in decrease of virus spread.

Conclusion:-
1)Lockdown, Contact Tracing , Social Distancing is implemented and after that restrictions are implemented. There is decrease is the number of active cases
Social distance --- decrease rate of virus 10%
Contact tracing --- decrease rate of virus spread 15%
Lockdown --- decrease rate of virus spread 70%
2) By running a simulation for different values of R ,infection increases with increase value of R and decreases with decrease values of K.
3) Virus 2 spreading is faster considering its R and K factors than Virus 1.
