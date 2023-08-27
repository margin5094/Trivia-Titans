
# Multi-Cloud Serverless Collaborative Trivia Challenge Game

Trivia-Titans is a dynamic online trivia game designed as a serverless, multi-cloud deployment model, merging technology with trivia gaming excitement. Users can personalize their experience with features such as user authentication, profile management, AI-assisted team creation, and an interactive trivia game lobby. It offers global and category-specific leaderboards, notification alerts, automated question tagging, and virtual assistance to enhance user engagement. Administrators can effectively manage trivia content, ensuring a safe gaming environment. The application leverages AWS and GCP for a cost-effective solution, eliminating backend management hassles. With its React front end, Trivia-Titans delivers a seamless and user-friendly interface, making it a go-to platform for trivia enthusiasts worldwide.


## Cloud Architecture 

![Architecture](https://github.com/margin5094/Trivia-Titans/assets/43315271/7e78a4ec-b555-41f4-af76-1f0214de4c5b)


## Features

- The **User Authentication** module in Trivia-Titans employs GCP's Firebase Authentication for user registration and login. Additionally, a two-factor authentication process is incorporated, involving three predefined questions and answers stored in AWS's DynamoDB. AWS Lambda is responsible for validating these answers. Services utilized include GCP Firebase, Amazon DynamoDB, and AWS Lambda.
- The **User Profile Management** module in "Trivia Titans" empowers users with control over their profiles, allowing edits to personal information and displaying gameplay statistics like games played and win/loss ratios. This module utilizes Amazon Web Services' DynamoDB for efficient data storage and retrieval, including user details and gameplay metrics. AWS Lambda, a serverless compute service, handles backend code execution, interface responses, and database operations. Google Cloud Storage is employed for storing user-generated content like profile pictures, ensuring scalability and reliability. Together, these services provide a robust and efficient solution for managing user profiles in the game.
- The **Team Management** module in "Trivia Titans" enables users to create and manage teams with unique AI-generated names. It employs Amazon DynamoDB for data storage, AWS Lambda for backend operations, and utilizes Amazon SQS and SNS for real-time communication related to team invitations. OpenAI's ChatGPT adds a fun element by generating unique team names. This combination of services provides an efficient and interactive solution for team-related activities in the game.
- The Trivia **Game Lobby** in "Trivia Titans" is the central hub for users to discover, filter, and join trivia games. It offers filtering options for categories, difficulty levels, and time frames, tailoring the browsing experience. Users can access game details like participants and start times before joining. AWS Lambda manages backend operations efficiently, while the React frontend ensures a responsive user experience, creating a seamless game browsing and joining process.
- The **In-Game Experience** module in "Trivia Titans" adds excitement with real-time multiple-choice trivia questions, team score updates, and instant chat for collaboration. It allows players to request and share hints and provides explanations for correct answers. This module tracks individual and team performance and utilizes GCP Firebase, Firestore, and Cloud Function for seamless gameplay.
- The **Leaderboards** module in "Trivia Titans" provides players with global and category-specific leaderboards for teams and individual players, fostering competitiveness and offering insights into their performance compared to others. Detailed statistics for top performers are also available.
- The **Trivia Content Management** module in "Trivia Titans" empowers administrators to manage game content effectively by adding, editing, and deleting trivia questions, categorizing them by difficulty levels. It also enables the creation and customization of trivia games. This module uses Amazon DynamoDB for content storage, AWS Lambda, and Cloud Functions for backend operations, and Looker Studio for analyzing gameplay data and user engagement, ensuring a robust and insightful content management system.
- The **Notification** module in the trivia application improves user engagement by sending timely email updates. It notifies users about team invitations and acceptance by other players, encouraging subscriptions for email notifications. Amazon's Simple Notification Service (SNS) is used for efficient message publishing and delivery to subscribers.
- The **Automated Question Tagging** module in "Trivia Titans" automatically categorizes trivia questions by tagging them with relevant categories such as sports, computer science, general knowledge, or entertainment based on the question's content. It utilizes Google Cloud Platform's Natural Language API invoked by a Google Cloud Function, streamlining content organization and enhancing the game experience.
- "Trivia Titans" integrates a **Virtual Assistance** module featuring an AWS Lex chatbot for enhanced user support. The chatbot assists with game navigation and offers dynamic score queries based on team names. AWS Lambda handles backend functions, DynamoDB manages data storage, and AWS Lex provides natural language understanding, making it a user-friendly virtual assistant for smoother gameplay and interactive score tracking.



## Demo
Screenshot-1:
![ss1](https://github.com/margin5094/Trivia-Titans/assets/43315271/a3cd7e99-cf2f-479e-9331-3267dd48a175)

Screenshot-2:

![ss2](https://github.com/margin5094/Trivia-Titans/assets/43315271/96016591-9525-4962-9df2-5ad62b1e667b)

Screenshot-3:

![ss3](https://github.com/margin5094/Trivia-Titans/assets/43315271/2425baae-2fe0-4d7e-8155-8ecee9262f8e)

Screenshot-4:

![ss4](https://github.com/margin5094/Trivia-Titans/assets/43315271/dff95f96-a345-4a1c-8d1a-e2ff544dea59)

Screenshot-5:

![ss5](https://github.com/margin5094/Trivia-Titans/assets/43315271/047c73b5-f9f6-48c8-aecf-986b666d6531)

Screenshot-6:

![ss6](https://github.com/margin5094/Trivia-Titans/assets/43315271/cb849b58-3f06-46cc-80db-3a0aecb636f7)

Screenshot-7:

![ss7](https://github.com/margin5094/Trivia-Titans/assets/43315271/1807a35a-8f7b-4279-a6d3-5031c302f133)

Screenshot-8:

![ss8](https://github.com/margin5094/Trivia-Titans/assets/43315271/e88066fb-a4dc-4006-a1f2-fc278dcdf810)

Screenshot-9:

![ss9](https://github.com/margin5094/Trivia-Titans/assets/43315271/ced42e57-5b01-44b9-9578-5c8c7ea5953e)

Screenshot-10:

![ss10](https://github.com/margin5094/Trivia-Titans/assets/43315271/af3e6743-9a55-48e4-845d-7e86ed6d741f)

Screenshot-11:

![ss11](https://github.com/margin5094/Trivia-Titans/assets/43315271/253ac2ce-ab12-465e-8662-c8f87cc3fd6f)

Screenshot-12:

![ss12](https://github.com/margin5094/Trivia-Titans/assets/43315271/cc87120d-fe60-4201-b012-e0e5f1956d98)

Screenshot-13:

![ss13](https://github.com/margin5094/Trivia-Titans/assets/43315271/268fe815-fc4c-4c0e-8499-8bdffed2bc34)

Screenshot-14:

![ss14](https://github.com/margin5094/Trivia-Titans/assets/43315271/6eb64246-cb20-4e6e-94c4-aa9a43f098f2)
## Deployment

### Backend Deployment

#### Google Cloud Functions (GCP) & AWS Lambda

Whole backend was created in Lambda and GCP cloudFunctions. This are serverless so no need to deploy on server.


### Frontend Deployment

#### GCP Cloud Run

Firstly, Docker image of frontend code was made and store in GCP Artifact Registry. After this , docker container was run on Cloud Run which is serverless.


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`YOUR_KEY` Firebase API key for access of GCP services.

