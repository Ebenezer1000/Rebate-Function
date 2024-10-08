# REBATE-FUNCTION
- It is a system design that provides a user with a rebate%-bonus group, which influences the prize the user receives, the self rebate discount the user receives and the agent rebate discount received by a superior agent account.
- Let’s start on the logic and formula behind how a user’s prize is influenced and calculated by the rebate%-bonus group.
## Rebate-Prize Determination:
- A user can sign on to the website via a URL link on an advertising page. The user that accessed and registered in this instance is viewed as a customer. All users that register onto the platform in this format, will automatically assume a rebate%-bonus group set by the system owner at the backend. Which starts from 15% and a corresponding bonus group of 2000, 14.9% and a corresponding bonus group of 1999, in that order to 0% and a corresponding bonus group of 1700. In this system there are no agent account type, just users or customers.
- So if the system owner sets the system rebate% at 13.5% with the bonus group of 1970, every user that registers onto the lottery website assumes that rebate%-bonus group. 
- Now if any user wagers a bet, the formula below is used to calculate the prize the user received.
![image](https://github.com/user-attachments/assets/1322c721-d89a-4981-9507-1b45d9cddc6f)
- Let us take a look at this example
![image](https://github.com/user-attachments/assets/f1545f45-f752-41d6-a7b1-dce1f6273581)
- Rebate% = 14.25
- Odds = 827.0833
- Unit Amount = 0.01
Using the formular we can calculate and verify if we our result is the same as on the lottery website
![image](https://github.com/user-attachments/assets/eb70791c-be9a-477c-9dbc-aab32e6ba4f9)
- Prize = 8.208

And at 3 decimal places, you see the prize in the lottery website is the same as what we calculated.
In addition to the prize winning, you may as well be awarded with a self rebate discount based on whether you choose a low rebate%-bonus group instead of a high rebate%-bonus group before you wager a bet. I will go into more detail and how this is calculated in the second format of rebate distribution.  

- This is one form of how the rebate function is employed. Now let us look at the logic and format of the other rebate function is used.

## Agent - Customer Rebate Distribution
- This is another format of the rebate system. This setup is different in structure and implementation to the rebate prize determination. In this scenario, a new user cannot register onto the platform via an advertised UrL link. A new user can only register on the platform if they are registered by a superior agent. The superior agent can register the new user as a surbodinate agent (that can also register surboniate agents and customers) and customers (they cannot register anyone).
- An agent account can receive both self rebate discount and rebate discount from his surbodinates (agents and customers).
- The customer can only receieve a self rebate discount but not a rebate discount from surbodinates because the account type - customer, cannot register any new user.

There are 2 methods an agent account type can register a new user.

- The first format is when the agent via his dashboard provides a new user with a username & password, chooses what account type (Agent or Customer) will be, selects the rebate%-bonus group, decides to enable or disable chat between his account and the surbordinate account (Agent/Customer) he registered. Then he sends the login details to the new user, who can then use that to sign in.
![image](https://github.com/user-attachments/assets/b82c5def-adb8-4e6d-a96d-bbd0cf032ccb)


- The other format is when the agent has a link management system. Where the agent on his dashboard he can set countless registration link with the account type (surbodinate agent or customer) and rebate%-bonus group. And he can later choose any of the links with whatever parameter in terms of account type and rebate%-bonus group, send it to any new user and they can register on the sign up and become a subordinate account type (agent/Customer) to the superior agent that provided the link.
 ![image](https://github.com/user-attachments/assets/e11e6fea-d662-432b-8190-0071ce0d6d7a)
 ![image](https://github.com/user-attachments/assets/81c13ea9-351c-40c1-a25c-799b6c632364)

- Since we have addressed how a new user can be registered onto the system in the agent - customer rebate distribution, let us now look at how joining in this format might your rebate distribution.

- 1. A main agent account set by the system owner has a rebate%-bonus group for example of 13.5%. The main agent can now use the 2 formats of registering a new user to register new users but with one main condition, which is the new user (agent/customer) cannot have a higher rebate%-bonus group than the agent that is registering him. They can either have the same or lower rebate%-bonus group. So for example any new user account, that the main agent account registers will have a rebate%-bonus group of either 13.5% or lower but not higher than 13.5%. If the main agent creates a new user account (agent), that agent can also go on to register new user accounts (agents/customers) and give them the same or lesser rebate%-bonus group. And the logic follows in that order, remember though a customer cannot register any new user.
- Since we have now established how agent - customer registration works, we will now look at how it affects the rebate distribution
Let us first provide the parameters, formula and how we will calculate the rebate.
- Example 1:
- Main Agent: Has rebate percent of 13.5%
- Subordinate (agent/customer) registered by main agent: Has rebate percent of 13.0%
- Subordinate wagers a bet amount of $5.6
Main agent gets a rebate discount of $0.028 of surbodinate wagered bet amount.


![image](https://github.com/user-attachments/assets/41755531-c98b-4399-999c-067c19ef6c17)


- Example 2:
- Main Agent: Has rebate percent of 13.5%
- Surbodinate (agent) registered by main agent: Has rebate percent of 13.0%
- Surbodinate (customer) registered by surbodinate agent: Has rebate percent of 12.5%
- Surbodinate Customer wagers a bet amount of $5.6
  
- In example 2, the flow is Main agent>Surbodinate agent>Surbodinate customer.
  
We apply the same formular and find out how much rebate amount discount the main agent and surbodinate agent will get fom the bet amount of the surbodinate account.


![image](https://github.com/user-attachments/assets/be7220ea-05f6-4c1d-94a7-358a4a373811)


Now we do same for subordinate agent. Where we subtract the rebate% of the new user (customer) he registered from his rebate%

![image](https://github.com/user-attachments/assets/e7c7066c-9ac2-48e9-ad9e-a4775e0b90e9)


Remember the customer account type cannot receive this type of rebate amount, because this account type cannot register a new user hence there is no subordinate account directly to his account that can place a bet and which he can find the difference in rebate% to determine any rebate amount.

But, there is another form of rebate that a customer can receive, called self rebate. This type of rebate is assessible to all account types (agents /customer) based on one conditions.

- Example 3:
Let us use the same paramters in example 2 to illustrate this point.

- Main Agent: Has rebate percent of 13.5%
- Subordinate (agent) registered by main agent: Has rebate percent of 13.0%
- Subordinate (customer) registered by surbodinate agent: Has rebate percent of 12.5%
- Subordinate Customer wagers a bet amount of $5.6

![image](https://github.com/user-attachments/assets/21cac027-3520-475d-aed7-80b3fc5ea512)

You can see from the image above, the subordinate customer had a form of rebate called self rebate.

Also attached below is an image from a lottery website that has the same general rebate and self rebate implementation, with the same pararmeters of main agent rebate of 13.5%, subordinate agent rebate% of 13% and subordinate customer rebate% of 12.5%, where a bet amount of 5.6 was wagered and the user choosing a low bonus prize, hence ensuring the user got a self rebate 0.7 and the top agents above him getting 0.028 each as shown in our example too. 

![image](https://github.com/user-attachments/assets/ba5166e3-ec28-40b2-bba4-8ddc23d46f4a)


Let me explain how that self rebate can be received by any account type if they meet this one condition.

Before any account type (agent or customer) wagers a bet, the user has the option to choose a high bonus prize or a low bonus prize. If the user chooses the high bonus prize, the self rebate distribution does'nt apply. Only the general rebate distribution from down agent or customer to top agent applies as shown in Example 2. 

But if the user (agent or customer} chooses the low bonus prize, the general rebate distribution occurs and also the user that wagered the bet also gets a self rebate where the lowest rebate% in the rebate% list which is 0%, is subtracted from his rebate%. And in the image above in Eaxmple 3, you see 0% was subtracted fromn the user's (customer) rebate% of 12.5%. Then the result waas divided by 100 and multpilied by the user's bet amount he wagered. 
So you see, if a user wagers a bet and chooses the low bonus prize, not only do the agents above him receive a rebate amount but the user also receives a rebate amount in the form of self rebate.
I will attach an image to show the low bonus prize and high bonus prize that will influence whether a user recieves a self rebate or not.

![image](https://github.com/user-attachments/assets/08f80a3d-ad68-40ef-b93c-a034bd1317c5)

As you can see in the highlighted part of the image above, there's a bonus prize of 1951 - 0% and 1681 - 13.5% for that particular game type. If the user chooses the lower bonus prize of 1681, the user will receive the self rebate after the bet is settled but if the user chooses the 1951 bouns prize, the user does'nt get any self rebate, only the genreal rebate distribution from down users to top users will apply.
Also below is a part image of the rebate list quota, which begins from 15% at 2000 bonus group and runs down to 0% at 1700 bonus group. So if a user before wagering a bet chooses the low bonus prize, his rebate% in the rebate list is taken and subtracted from the lowest rebate% in the list which is 0%.  
![image](https://github.com/user-attachments/assets/35ae767b-7a56-44ce-bb47-750c81204f70)
 







