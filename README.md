Rules Used:
1. Possible Brute Force Attack
2. Suspicious Login Activity
3. Unauthorized Device Access
4. Multiple Failed Logins
5. Trusted Login 
Every rule has a set of conditions. For 1. the conditions were failed login attempts over 5
and login success after failures is true. For 2. the conditions were access time and 
the geolocation of the access. For 3.the condition is the device status being unrecgonized. For 4.
the condition to be met is login failures greater than 3. For 5. the conditions are device status is trusted,
geolocation is the same, and failed login attempts is less than or equal to 3. If every condition is met for 
a rule than it will be triggered. 

The inference mechanism is forward chaining. What my algorithm does is examine each 
input (fact) at a time and match the associated conditions from the knowledge base. We send the condition
and the fact through the evaluate match function to check which rule should be triggered. We start with the 
known facts from the user and apply the if then rules to the conditions to see which ones match the facts 
and we continue until no new rules can fire.
<img width="443" height="407" alt="Screenshot 2026-02-02 at 1 04 22 PM" src="https://github.com/user-attachments/assets/0ec6add9-0d8b-4dd6-b276-fb929d96d089" />
