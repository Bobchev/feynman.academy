# feynman.academy

Feynman.Academy
Guaranteeing grades and gamified task scores on
Consortium Blockchain
 

Contents
1.	Overview
2.	How Blockchain is used in the project

Overview
This document explains the vision of how Consortium Blockchain could be implemented in the feynman.academy project. This method was chosen so the fundamental principles and features could be established and they are:
	Principles:
		Immutability of information
		Reliability of the information
		Independence from single control factor
		Closed network
		Sustainability

	Features:
Storing Scores and Grades (including assignment evaluation, scores of gamified tasks)
Storing final degree and generated CV with student performance
Sharing decision taking (example: Change the evaluation of certain task or how much scores certain task could give)


 

Terms are good to know before the read
 
Hash
Hash functions accelerate table or database lookup by detecting duplicated records in a large file. One such application is finding similar stretches in DNA sequences. They are also useful in cryptography. A cryptographic hash function allows one to easily verify that some input data maps to a given hash value, but if the input data is unknown, it is deliberately difficult to reconstruct it (or any equivalent alternatives) by knowing the stored hash value. This is used for assuring integrity of transmitted data, and is the building block for HMACs, which provide message authentication.
Hash functions are related to (and often confused with) checksums, check digits, fingerprints, lossy compression, randomization functions, error-correcting codes, and ciphers. Although the concepts overlap to some extent, each one has its own uses and requirements and is designed and optimized differently. 
 
 
 
Oracle
An oracle, in the context of blockchains and smart contracts, is an agent that finds and verifies real-world occurrences and submits this information to a blockchain to be used by smart contracts.
Smart contracts contain value and only unlock that value if certain pre-defined conditions are met. When a particular value is reached, the smart contract changes its state and executes the programmatically predefined algorithms, automatically triggering an event on the blockchain. The primary task of oracles is to provide these values to the smart contract in a secure and trusted manner.
Blockchains cannot access data outside their network. An oracle is a data feed – provided by third party service – designed for use in smart contracts on the blockchain. Oracles provide external data and trigger smart contract executions when pre-defined conditions meet. Such condition could be any data like weather temperature, successful payment, price fluctuations, etc.
Oracles are part of multi-signature contracts where for example the original trustees sign a contract for future release of funds only if certain conditions are met. Before any funds get released an oracle has to sign the smart contract as well.
 

 
Immutability of Blockchain
Immutability is used to denote something which can never be modified or deleted. In a blockchain, it refers to the logs of transactions, which is created by consensus among the chain’s participants. The basic notion is this: once a blockchain transaction has received a sufficient level of validation it can never be replaced or reversed or edited.
Immutability, the concept itself, is somewhat relative. For example, if I send an email to a large list of friends, that data is pretty immutable from my perspective. To change it, I’d have to persuade my friends each to delete the email. Or, I would have to persuade the email provider, say Gmail and the companies running all the mail servers of my friends. From my perspective, and with the control I have, that email is immutable – I can’t unsend or revoke it without collaboration and risk of detection. The same relativity holds for Blockchain too, though suffice it to say transactions on Blockchain are in fact pretty immutable.
Consortium blockchains can best be understood when compared to their more popular counterpart, public blockchains. This type of blockchain is one that possesses no access restriction, meaning that absolutely anyone with an internet connection can become a participant of a public blockchain. More specifically, anyone in the world is able to read data that is included on the blockchain, and anyone in the world is allowed to execute transactions on a public blockchain. Importantly, there is also no restriction as to who can participate in the consensus process for blockchains, which is the process that determines the individual or entity that can add a block to the blockchain. Public blockchains are considered to be fully decentralized, with control over the blockchain not being in the hands of any single individual or entity.

Consortium blockchains differ to their public counterpart in that they are permissioned, thus, not just anyone with an internet connection could gain access to a consortium blockchain. These types of blockchains could also be described as being semi-decentralized. Control over a consortium blockchain is not granted to a single entity, but rather a group of approved individuals. With a consortium blockchain, the consensus process is likely to differ to that of a public blockchain. Instead of anyone being able to partake in the procedure, consensus participants of a consortium blockchain are likely to be a group of pre-approved nodes on the network.  Thus, consortium blockchains possess the security features that are inherent in public blockchains, whilst also allowing for a greater degree of control over the network.


 
How Blockchain is used in the project

1.	Adding student to the blockchain
When a new student is being registered on the feynman.academy platform, a request (this request includes unique hash that is generated from the Student credentials) is sent  to a Membership Management master node.
The Membership Manager master node accepts the request, validates if the hash could be accepted and returns that the unique student address is created.
If there are no stops during the validation process, the student address is propagated to the ledger.
 
 

2.	Storing scores, grades and assignment evaluation
 
When completing an assignment, a request is triggered to one of the master nodes. 
The request should contain student hash data and cryptographic key that is obtained on completing the assignment. 
Then the master node decides if this request is valid.
For this to happen the student hash data should be valid and the student should be with active state, also the cryptographic key is used as validation that the assignment have been done successfully.

Next step is for the peers to validate this process.
Pre-defined number of peers should successfully do the same validation before the result is pushed to the ledger.
 

3.	Sharing Decision Taking
The platform will give ability to vote, object or propose new features, change of assignment evaluation (as absolute value and also for certain student). 
The ability to change assignment evaluation is a revolutionary feature. It is expected that if a problem occurs students could resolve it using their vote (blockchain transaction) to change the outcome, in a democratic way and through communication.

Let say for example, a student does not agree how a certain assignment is being evaluated (the points given for each milestone).
He could raise a vote trough the User Interface of feynman.academy, this vote to be validated through the master node and the peers and then pushed to the blockchain.
Once it is there, every other participating node (student), could vote.
This voting system is a smart contract that after reaching certain state will do 2 things:
1.	Send a message (Blockchain transaction) to all nodes (students) with summary of the vote

2.	Send the final result of the vote to the master node, which will then send it to the feynman.academy so the assignment evaluation is changed.
 


4.	Storing CV and Student Diploma

After Student finishes a course, all his data both from the feynman.academy and the shared blockchain is hashed and sent to a master node.
The master node then validates locally those hashes and does an oracle request to validate the data that need to be confirmed outside of the blockchain.
If all validation pass, a new hash is generated that is pushed to a public blockchain.

Abstract:
The governance of data used for evaluation is an important requirement for generating accurate Student diploma.
To improve the visibility of data quality and analysis, we developed a methodology, a blockchain-based platform that can be
used to validate data integrity from large, set of student performance data. We implemented a private blockchain using multiple platforms and integrated it with a data science platform deployed within a large cluster network. An administrative web application was built with NodeJS to manage the platform, which was built with a microservice architecture using Docker. The Feynman.academy platform was integrated during data acquisition into
our existing data science platform. Using encryption, data were hashed and logged within the local blockchain infrastructure. 
To provide public validation, the local blockchain state was periodically
synchronized to the public Ethereum network. The use of a combined private/public blockchain platform allows for both public validation of results while maintaining additional security and lower cost for blockchain transactions. Original data and modifications due to downstream analysis can be logged within Feynman.academy and data assets or results can be rapidly validated when needed using API calls to the platform. The Feynman.academy platform provides a data governance solution to audit the acquisition and analysis of student data. The platform provides cryptographic assurance of data authenticity and can also be used to document data analysis. 


Explain your idea in one sentence
Making education in universities entertaining and engaging by using an economic simulation game where students can learn, interact, build their businesses, careers and take part in virtual internships offered by real companies in a risk free environment.



Explain your idea in one paragraph
Feynman is a software consisting of three main modules. The first module is the Single Player Module and its purpose is to be used in exercises. The students will be introduced in a simulation game where they will walk through all their assignments in a role playing way. The second module is the Multiplayer Module where students will have the opportunity to build businesses in a simulated environment that mimics the real world. The third module is the Recruiting module where real world companies will offer virtual internships.




Explain why your idea is innovative. If your idea is based on an existing concept, explain how your use of that concept is innovative in the country or context where it will be implemented.
Judging Criteria: “Innovation: either disruptive or incremental (building on what has been done before). Critically, the idea must be innovative at least within its given socio-economic and geographical context.”

Feynman aims to make the educational process in universities a better and more engaging experience in three steps. 
Single Player Module. 
In the single player module, the students will be given assignments where their answers will affect their future progress. Using this technique, the student will be more engaged with the process. The single player module will identify missing knowledge using follow up questions when there is a wrong decision, thus it will offer every student an individual educational program which will tell the student where they should focus and fill their missing knowledge.
Multiplayer Module. 
Once the student has passed the Single player module they will be allowed to enter a simulated environment where they will interact with other students, build business and practice soft skills such as creativity, critical thinking, negotiating and managing people. The simulation will be based on the city where the university is in order to be as realistic as possible and prepare the students for their future career.  
Recruiting Module. 
Real world companies will be included in the simulation and they will offer virtual internships. This way they will save the usual 1 to 3 months of transition time which fresh graduates need to adapt to the work environment. Offering virtual internships will save the company money and costly mistakes by the intern will be eliminated. 
The recruiting module is a stretch goal and will be added after the initial development and testing.

Explain how your idea will empower young people to participate fully in a changing economy and how you would use a place-based approach.
Judging Criteria: “Impact: the potential of the proposed idea to tackle the issue outlined in the challenge statement. The entrant should demonstrate a clear definition of the problem their idea aims to solve, an understanding of how that fits with the challenge statement and who would benefit from it, feeding into a well-elaborated theory of change”
The world around us changes in a fast pace. Educational systems however haven’t changed much even though they are the foundation of a good economy. Going through university has turned into a stressful experience, the amount of information we have to learn is becoming larger every day because of the fast progressing world we live in and teachers don’t have time to pay attention to every student. This leaves students in an uncomfortable position where they are punished for making mistakes and because of the large amount of information and short timespan they won’t be given a chance to learn from their mistakes and try again. Most universities present information in a way where students have all the parts for the puzzle but are unable to solve it because they are not given the big picture. Knowledge is presented in isolated pieces instead of logically connected parts of a unified entity. Feynman will give students the freedom of making mistakes and learning from them by using algorithms to analyze why something went wrong and telling the student where they should focus before trying again. The software will also present the information as a semantic tree where transitions from one subject to another will be unnoticeable because of the logical connections between them. Additional soft skills such as creativity, critical thinking, negotiating and managing people are learned through the multiplayer module. 


Explain how you will design and test the idea with potential users to develop it into a sustainable project over the next three years. *

Judging Criteria: “Sustainability: the financial and environmental sustainability of the idea, as well as the potential for adequacy and uptake stemming from the development of the idea carried out with users, from first concept, through testing, validation and business modelling.“

The idea was presented to one of the biggest economics universities in Bulgaria and there are ongoing talks about a cooperation in the development of the project. Teachers from one of the university’s departments will take part in the digitalization of knowledge and turning it into a simulation game where information is easy to digest. Students will be able to test the project during the development and give us feedback. Game developers have been contacted and are willing to be involved in this innovative project. Once Feynman is developed to work on the department level in the university, we will move on to the faculty level where more courses will be included in the simulation and interactions will be created between them. Once we create a stable working version for one university, businesses will be invited to try the recruiting module. The Recruiting Module will give information about the students’ progress and achievements in the Multiplayer Module, should they agree to share it. Recruiters will design internships in the simulation together with our team and offer them to students who want to apply. The businesses will receive detailed information about the progress of a student who is in their internship program and will be able to give them accurate feedback. Using Feynman, the transition from a graduate to an employee will be a smoother and less stressful process. 


Explain how you will grow your idea in the future so it can reach more people or be replicated by other people across Europe.*

Judging Criteria: “Scale: the idea’s growth potential and potential to scale and be replicated throughout Europe.”



Using the more complex connections in the Multiplayer Module, users from other countries will be able to join the virtual world. Multiple options will be developed to support interaction between different courses and specializations, such as architect - building contractor - construction company - raw material supplier - business owner commissioning an office building. With every additional connection between different universities and courses the simulation will become more realistic and will depict an adequate picture of the real world that awaits the students after they graduate. Feynman can help students develop their CV by creating a profile based on the decisions taken in the Multiplayer Module, which will be a useful tool for recruiters. 
