# Project Part 1

ATTENTION pointillé = attribut dérivé
truc obligatoire souligné.

#### Employee
- ID
- First name
- Last name
- Pseudonym (not mandatory)
- *Has a role* :
	- [[#Manager]]
	- [[#Event Planner]]

#### Manager
- Assigns (only employee supervised, maybe without expertise) :
	- [[#Event Planner]]
	- [[#DJ]]
- *Creates* :
	- [[#Event]]

#### Client
- Client number
- First name
- Last name
- Phone
- email (not mandatory)
- *Requests* (0, N):
	- [[#Requests]]

#### DJ
- *Propose*
	- [[#Playlist]] ?
- *Specialized in* (1, 3):
	- [[#Genre]]

#### Event
- Type 
- Theme
- Name
- Description (not mandatory)
- Date 

#### Event Planner
- *Discuss* :
	- [[#Location]] (doit prendre en compte qu'on visite plusieurs endroit ?)
- *Handles* :
	- [[#Requests]]
- *Experts in* (0, 2):
	- [[#Theme]]

#### Location
- *Is a* 
	- Public venue (==Fee to include but how ?== fees depend on event and on theme so pointillés !)
	- Private residency
- ID
- Adress (composed of):
	- Street and number
	- City
	- ZIP
	- Country
	- Comment (not mandatory)
- ==Link with themes ?==

#### Requests
- Description
- Price
- Identified by event and name 

#### Playlist
- *Contains* (1, N):
	- [[#Song]]
- Name (unique)
- *Linked* (1, N) : 
	- [[#Theme]] (mulitple)

#### Song
- Genre (can be specialization of two genres)
- Title
- Duration
- Artist
- CD (souligné)
- Track number

#### CD
- Title
- Year
- Producer
- CD Number
- *Copy of*
	- Copy

#### Copy
- Copy number
- *Borrowed by*
	- [[#DJ]]

#### Theme

#### Genre
