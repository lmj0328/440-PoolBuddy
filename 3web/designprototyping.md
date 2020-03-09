---
title: "designprototyping"
author: "lmj0328"
date: "3/9/2020"
output: html_document
---

# **Poolbuddy: carpooling within a community**

## **Problem and Solution Overview**
### **Problem**
Carpooling significantly reduces driving costs and environmental impact. It is a great opportunity to find people with similar interests in your city. However, scheduling rides is often too difficult to maintain and many do not know where to begin looking for carpoolers. 
 
### **Solution**
We aim to make carpooling more convenient. Our proposed solution supports routine carpooling schedules, accommodates the preferences of both the drivers and the riders, and ensures clear communication and safety throughout the entire carpooling experience.

---


## **Initial Paper Prototype**
<div>
    <img style='width:80vw;' src='initial_task1overview.jpg' />
</div>
<div>
    <img style='width:80vw;' src='initial_task2overview.jpg' />
</div>
 
Our initial paper prototype focused on two key tasks. The first involves creating a new account on the PoolBuddy platform and setting up a ride with a rider that the user finds through searching on PoolBuddy. Our second task involves a driver actually starting a scheduled ride and notifying the passengers with the expected ETA. We chose these two tasks as we felt that these were the ones that were the most common and practical. While we spent time discussing and designing various subsystems, such as the personal profile and friend system, ensuring that our application could perform the tasks most practically beneficial to users was a top priority.

### **Task 1: Finding Carpoolers with the Same Route**
 
<div>
    <img style='width:80vw;' src='initial_onboarding.jpg' />
</div>
 
Our first task begins with a fairly simple onboarding process. Our main focus here was allow users to enter personal preferences, which would later be used to match riders.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='initial_task1-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='initial_task1-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='initial_task1-3.png' />
</div>
 
Once the user is brought to the Upcoming Rides screen, they can start a new ride by clicking the ‘+’ icon in the upper right corner. After entering information regarding the ride, they can create the ride and see information such as its current passengers and route. The driver is also able to start the ride from this screen.
 
<div>
    <img style='height:30vh;padding-right:1vw;' src='initial_task1-4.png' />
    <img style='height:30vh;padding-right:1vw;' src='initial_task1-5.png' />
    <img style='height:30vh;padding-right:1vw;' src='initial_task1-6.png' />
    <img style='height:30vh;padding-right:1vw;' src='initial_task1-7.png' />
    <img style='height:30vh;padding-right:1vw;' src='initial_task1-8.png' />
</div>
 
To add a new carpooler, the user clicks the ‘+’ icon underneath the “People” section. This will bring them to the Friends page, where they can add people that they are already friends with. If they want to find new carpoolers they click the ‘+’ icon in the top right corner, which will show them a profile of a rider that matches with their route and preferences. The profile includes a rating, preferences, as well as an approximation of the added time to the trip and the potential financial compensation for choosing the rider. The user can then choose to accept the rider or reject and search for a new one using the buttons on the bottom of the screen. Accepting the rider will bring the user back to the ride page, and a pending invitation will be sent to that rider, as shown in the “People” section.
 
### **Task 2: Start a Carpool Ride and Communicate with Passengers**
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='initial_task2-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='initial_task2-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='initial_task2-3.png' />
</div>
 
Our second task starts with the user getting a notification that a ride they have set up is about to begin. Tapping the notification brings them to the Upcoming Rides screen, which has the ride they’ve created in the first task. Selecting the card brings them to the same ride screen, and from here they can start the ride.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='initial_task2-4.png' />
    <img style='height:50vh;padding-right:1vw;' src='initial_task2-5.png' />
</div>
 
Starting the ride brings them to a navigation screen, similar to Google Maps. To communicate with the passengers, the driver can press the chat icon in the bottom right corner to bring up a chat window with the other members of the ride.
 

---

## **Testing Process**




---

## **Testing Results and Prototype Refinement**
 
### **Heuristic Evaluations**

*Match between System and Real World*

- The functionalities of the features in login screen were not clear
    - We made the registration and login options more distinct by moving the signing up process further down the page.
- Icons when creating rides were unclear
    - Changed icons and included labels added at the bottom of each main icon.
 

*Error Prevention*

- Unclear idea about what needs to be inputted when signing up
    - Added placeholder text that shows an acceptable input and restricted input types to only numbers for phone numbers
 
*Visibility of System Status*

- Page for scanning driver licenses was unclear. It does not indicate what is supposed to be scanned.
    - Added description text on the page telling people what they are supposed to scan. A follow-up screen can check what they scanned as well.
 
*Aesthetic and Minimalist Design*

- Process of adding carpoolers felt unnecessarily long
    - Added a simpler view on potential carpoolers in card view, where tapping on the card will bring the user to a larger, more-detailed view of each carpooler’s information and the ability to request this carpooler to ride on this screen.
 
*User Control and Freedom*

- There was no feature that prevented users from tapping on a potential carpooler and requesting them to their ride on accident
    - Added confirmation dialog when requesting a carpooler to ride
 
 
### **Usability Test Results**

*Simplified Ride Scheduling and Clarified User Expectations*

- This allows the app to better accommodate the user’s needs, where drivers have greater control about the passengers and routes while riders can choose rides that best suit their schedules.
    - App first asks whether the user wants to be the driver or rider as only drivers can create carpool rides while riders can only request rides and join existing rides.
 
*Clarifying Ride Statuses*

- recurring theme in our usability tests was that people would often try to start the ride prematurely since there were no indicators that the ride needed to be confirmed first.
    - Prevented drivers from starting carpool rides when not all the passengers have confirmed their invitations to the ride by graying out the “Start Ride” option.
 
*Driver Safety and Simpler Communication*

- Distracted drivers put all carpoolers in the car at risk of accidents. Another related issue is that carpoolers are not providing necessary information to maintain clear communication between all carpoolers in the ride.
    - Created automated messaging specifying information about their estimated time of arrival for drivers to use especially driving.
 
*Smarter Design on Adding Carpoolers*

- It is more important to find a driver in a carpool ride than finding friends to carpool with together.
    - Increased priority for finding new drivers and lowered priority for adding existing friends.
 
 
### **Design Critique Results**
*Better Accommodations to Meet Potential Carpoolers*
- Users may have accommodations that need to be addressed first before committing to a carpooling ride. For example, luggage space and allergy concerns are factors that determine if a ride can meet riders’ needs.
    - Added communication feature to chat with potential carpoolers
 
*Clearer Indications during Onboarding*
- The onboarding process was confusing and had ambiguous questions.
    - Added text descriptions to clarify whether the questions should be answered based on the drivers’ or the riders’ perspective
 
*Feed Page*
- Users may want to see if they can match carpool rides with their existing friends.
    - Ability to search through upcoming rides from friend list through the “Feed” feature on the app. It also promotes an overall community feel that users can stay connected with their carpooling friends.
 
---


## **Final Paper Prototype**

<div>
    <img style='width:50vw;' src='final_overview.jpg' />
</div>
 
### **Task 1: Finding Carpoolers with the Same Route**
 
<div>
    <img style='height:37vh;' src='final_onboard1.jpg' />
    <img style='height:37vh;' src='final_onboard2.jpg' />
</div>
 
Our onboarding process remained relatively unchanged in terms of the overall structure, and the majority of the improvements were on improving clarity.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='final_task1-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task1-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task1-3.png' />
</div>
 
In the final design, the user can now choose whether to create a ride as a rider or as a driver. After providing the information about the ride, the user is brought to the ride page where they can see information about the ride such as its current passengers and route. They can also chat with the riders, and edit ride information.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='final_task1-4.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task1-5.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task1-6.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task1-7.png' />
</div>
 
Adding a new carpooler will then bring the user to a screen showing the summary cards of various carpoolers. Selecting one of these cards will bring up the full profile. The user can then decide to accept, reject, or chat with the carpooler. If the rider accepts, they accept the confirmation dialog and are brought back to the ride screen. Here the screen clearly shows the pending request and indicates that the ride is not able to be started while the request is pending.

 
### **Task 2: Start a Carpool Ride and Communicate with Passengers**
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='final_task2-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task2-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task2-3.png' />
</div>
 
The majority of the changes to the second task were from the clarity improvements we made to the overall design. The task begins with the same notification screen, which will bring the user to the Upcoming Rides screen when selected. Selecting the card for the ride will bring the user to the ride screen, where they can start the ride.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='final_task2-4.png' />
    <img style='height:50vh;padding-right:1vw;' src='final_task2-5.png' />
</div>

The user is brought to a navigation screen identical to the one in the initial paper prototype. However, when the user selects the chat icon, they are now given pre-generated text options to send to passengers, such as an option to send their ETA.

---

## **Digital Mockup**

Our digital mock-up was primarily based on the high-fidelity mock-up with more screens for riders. It was made through Adobe XD. 

### **Task 1: Onboarding and Finding a Carpool**

### *Onboarding*


Users will first set up their accounts and then be asked to fill out their preferences. 

<div>
    <img style='height:50vh;padding-right:1vw;' src='onboard-1-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-1-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-1-3.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-1.png' />
</div>
 
If users plan to use the app as a driver, they will be asked to scan their driver licenses and fill out their car’s information.

<div>
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-3.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-4.png' />
</div>
 
Then, they will be asked for their preferences both as a driver and as a rider. 
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-5.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-6.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-2-7.png' />
    <img style='height:50vh;padding-right:1vw;' src='create-1.png' />
</div>
 
 
If users plan to use the app solely as a rider, they will only be asked to fill out their preference as a rider. All of these preferences could be adjusted later in the settings. 
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='onboard-3-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-3-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='onboard-3-3.png' />
    <img style='height:50vh;padding-right:1vw;' src='create-1.png' />
</div>





### *Create a ride as a driver*
If users plan to be the driver of the ride, they can create a ride by filling in the ride information. 
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='create-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-1-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-1-3.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-2-1.png' />
</div>
 
Then they will be able to invite their friends or chooses potential carpoolers from the suggested list created by the app. These suggested carpoolers are chosen based on the given ride route, time schedule, and their preferences. Each carpooler profile contains information about how much they are willing to pay for the ride and the additional time this will add to the entire ride. 
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='driver-2-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-2-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-2-3.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-2-4.png' />
</div>
 
Added passengers will need to first confirm that they want to be added to the ride first before drivers can start the ride.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='driver-2-5.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-2-6.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-3-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-3-2.png' />
</div>
 
They will be able to see the trip’s detail and be able to communicate with their riders at any time.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='driver-3-3.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-3-4.png' />
    <img style='height:50vh;padding-right:1vw;' src='ride-map.png' />
    <img style='height:50vh;padding-right:1vw;' src='ride-message.png' />
</div>


### *Request for a ride as a rider*
 
If users plan to join a ride as a rider, they may send out a request by filling in the ride information.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='create-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='create-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='rider-1-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='rider-2-0.png' />
</div>
 
 
After receiving approval from drivers, they will be able to compare and see, then select the ones’ that best fit with their needs. 
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='rider-2-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='rider-2-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='rider-2-3.png' />
    <img style='height:50vh;padding-right:1vw;' src='rider-2-4.png' />
</div>
 
After joining the carpool, they will be able to see the trip’s detail and communicate with the driver and other riders. 
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='rider-3-0.png' />
    <img style='height:50vh;padding-right:1vw;' src='rider-3-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='ride-map.png' />
    <img style='height:50vh;padding-right:1vw;' src='ride-message.png' />
</div>

### **Task 2: Start Carpool Ride and Communicate with Passengers**
The driver will receive a notification when the ride is about to start soon. When the driver taps to ‘Start’ to start the ride, all corresponding passengers will receive a notification while the driver will see the navigation screen heading towards the first passenger to be picked up. 
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='driver-4-0.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-4-1.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-4-2.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-4-3.png' />
</div>
 
When the driver is close to the passenger’s pick up location, the app will remind the driver to notify the passenger about his or her estimated time of arrival.
 
<div>
    <img style='height:50vh;padding-right:1vw;' src='driver-4-4.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-4-5.png' />
    <img style='height:50vh;padding-right:1vw;' src='driver-4-6.png' />
</div>


### **Changes we made from high-fidelity to paper prototype**
 
- The biggest change made when implementing the digital mockup is differentiating between the driver and passenger interactions in the app. The usability test consistently showed there were minor confusions between what these two roles. Therefore, we decided to create restrictions to better distinguish these roles.
- When creating a ride, the wording of the input labels were not clear to the participants in the usability testing study. We decided to change the wording of each label and added the estimated duration of the ride to give more information about the ride to the driver and passengers in the ride.
- In the onboarding process, we added more questions into the preferences section to create a more realistic portrayal.
- To create more flexibility and adhere to the real world match heuristics, we added the option to edit rides information.
- In order to follow the visibility of system status heuristics, we also added appropriate feedback from the app whenever a button is clicked or whenever there is information that we want the user to understand. For example, when adding carpoolers to the ride, those added passengers will need to confirm this new change first and cancelling the ride will also require all passengers to confirm this before this action can be com
