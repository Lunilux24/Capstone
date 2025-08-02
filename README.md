
# Project-Structure

Please use the provided folder structure for your docs (project plan, design documenation, communications log, weekly logs and final documentation), source code, tesing, etc.    You are free to organize any additional internal folder structure as required by the project.  The team **MUST** use a branching workflow and once an item is ready, do remember to issue a PR, review and merge in into the master brach.
```
.
├── doc                                             # Documentation files (alternatively `docs`)
│   ├── TOC.md                                      # Table of contents
│   ├── plan                                        # Scope and Charter
│   ├── peer-testing                                # Peer Testing instruction and tasks
│   ├── final-report                                # Final report documents
│   ├── design                                      # All design content
│   ├── logs                                        # Team and individual logs
│   │   ├── Andreas                                 # Andreas Hoffbauer Logs
│   │   ├── Bassim                                  # Bassim Beshry Logs
│   │   ├── Gavin                                   # Gavin Ashworth Logs
│   │   ├── imgs                                    # photos of github project backlog
│   │   ├── Imoudu                                  # Imoudu Ibrahim Logs
│   │   ├── Jordan                                  # Jordan Pohr Logs
│   │   ├── Team                                    # Team Logs
│   │   ├── Template                                # Log Templates
│   │   └── ...                                     # README.md file
│   └── ...                                         # Application colors file
├── build                                           # Compiled files (alternatively `dist`))    
├── app                                             # Source files (alternatively `lib` or `src`)
│   ├── backend                                     # Back end of the Application
│   │   ├── dependenies                             # Program dependency list
│   │   ├── mysite                                  # BFL Canada Application Program Logic and ML models files
│   │   │   ├── backend-tests                       # Backend testing
│   │   │   ├── ML                                  # ML model
│   │   │   ├── models                              # Model for document comparison
│   │   │   ├── views                               # Logic for each program view
│   │   │   └── ...                                 # Initialization/settings/URLs/ other supporting files
│   │   └── ...                                     # Database/docker/initalization files
│   ├── front-end                                   # Front end of the Application
│   │   ├── public                                  # Public project resources
│   │   ├── src                                     # Front end project source code
│   │   │   ├── _mocks_                             # Document and page mockup
│   │   │   ├── assets                              # Image and PDF sample documents
│   │   │   ├── Components                          # SHADCN/UI folder and react pages
│   │   │   │   ├── PDFViewer                       # PDF Viewer files
│   │   │   │   ├── ui                              # SHADCN UI components
│   │   │   │   └── ...                             # UI pages and elements (React)
│   │   │   ├── context                             # Route authorization
│   │   │   ├── front_end_tests                     # Front end testing
│   │   │   ├── lib                                 # Utility for class composition
│   │   │   ├── hooks                               # Web Hooks
│   │   │   ├── locales                             # French and English Localization library
│   │   │   ├── pages                               # Program views (React)
│   │   │   ├── styles                              # Style for PDF exporter function
│   │   │   ├── types                               # Interfaces for accessing dbmodels
│   │   │   ├── ...app.tsx...                       # Main Application Start (React)
│   │   │   └── ...                                 # Index/application/setup/css/viteConfig/other files
│   │   └── ...                                     # Initalization/Docker/configuration/component/gitignore/package/README files
│   └── ...                                         # Init and readme.md files
├── test                                            # Automated tests (alternatively `spec` or `tests`)
├── util                                            # Tools and utilities
├── LICENSE                                         # The license for this project 
└── README.md
```
You can find additional information on folder structure conventions [here](https://github.com/kriasoft/Folder-Structure-Conventions). 

Also, update your README.md file with the team and client/project information.  You can find details on writing GitHub Markdown [here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) as well as a [handy cheatsheet](https://enterprise.github.com/downloads/en/markdown-cheatsheet.pdf).   

# Project-Status Milestone 2
December 4, 2024

### Requirements Table


| Requirement                         | Description                                                                                                                                                           | Status         |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| **Login Form**                      | For login functionality, take text from username and password inputs. Clean information to protect from malicious input.                                              | Functional     |
| **Login Function**                  | For login functionality, take cleaned text from frontend and query database with login credentials.                                                                   | Functional     |
| **Registration Form**               | For registration functionality, take text from username and password inputs. Clean information to protect from malicious input. Hash sensitive information.           | Functional     |
| **Registration Function**           | For registration functionality, take cleaned credentials from frontend and write to the database of employees.                                                        | Functional     |
| **Client/Document Search Bar Form** | For client search, take text from search bar form input and clean text to prevent malicious input.                                                                    | Semi-Functional |
| **Client Database Function**        | For client search, take cleaned text and use it to query a database of documents/clients. Return results to frontend to be displayed.                                 | Functional     |
| **New Comparison Frontend**         | For new comparisons, prompt the user to upload a file via button, sending the file to the backend for database processing.                                            | Functional     |
| **New Comparison Backend**          | For new comparisons, take file from frontend and write it to database of documents, read database for file to compare to. Send both files to frontend for displaying. | Functional     |
| **Extract Text**                    | For the ML model. Extract the text in the PDF.                                                                                                                        | Functional     |
| **Preprocess Extracted Text**       | For the ML model. Preprocess the text by removing punctuation, special characters, uppercase, etc.                                                                    | Functional     |
| **Convert Policies to Vectors**     | For the ML model. Convert the cleaned text to vectors for numerical representation                                                                                    | Functional     |
| **Compare Document Features**       | Compare the vectors and return the diffs                                                                                                                              | Functional     |
| **Highlight Differences**           | For the ML model. Predict if differences exist.                                                                                                                       | Functional     |
| **Display Past Comparisons**        | Send a request to backend and retrieve a list of past comparisons for a client.                                                                                       | Functional     |
| **Retrieve Past Comparisons**       | Queries database and returns a list of comparisons.                                                                                                                   | Non-Functional |
| **Team History and Activity**       | Read from teams and documents tables in the database, displaying information to users.                                                                                | Non-Functional |
| **Export Comparison as PDF**        | List out comparisons in a CSV file and convert that to a PDF. File can then be downloaded from the application.                                                       | Functional     |
| **Promotion**                       | For admin, give/remove privileges.                                                                                                                                    | Functional     |
| **Demotion**                        | For admin, remove privileges.                                                                                                                                         | Functional     |
| **Create Team**                     | New “team” initiated in the teams database with no members.                                                                                                           | Functional     |
| **Delete Team**                     | Team which is currently in the teams database is removed.                                                                                                             | Functional     |
| **Add Team Member**                 | A manager will be able to add brokers as members to a team that has already been created.                                                                             | Functional     |
| **Remove Team Member**              | A manager is able to remove a broker from being a member of a particular team.                                                                                        | Functional     |
| **View Analytics on the Team**      | A manager will be able to view statistics such as the number of policies compared on a per team basis.                                                                | Non-Functional |
| **Create Comment**                  | Add a new comment linked to a particular point in a comparison document                                                                                               | Functional     |
| **Delete Comment**                  | Remove a previously created comment from a particular policy comparison                                                                                               | Functional     |
| **Edit Comment**                    | Edit the message from a previously created comment                                                                                                                    | Functional |
| **Show/Hide Comments**              | Selecting this will either show or hide all comments that have been created for a particular comparison document                                                      | Non-Functional |


___



# NEW ML APPROACH (updated for milestone 3)
___

## PDF Coverage Comparison Tool
This tool uses PyPDF2 for text extraction, Sentence Transformers for semantic text comparison, and Scikit-learn for calculating cosine similarity.

### Key Features
This script processes and compares two insurance policy PDFs to identify changes in coverage details, exclusions, and monetary values. The comparison follows a structured workflow:
1.	Text Extraction: The script leverages pdfplumber to extract text from both the old and new policy documents. It preserves page numbers, line positions, and formatting to maintain context.<br>
2.	Preprocessing & Normalization: Extracted text undergoes cleaning, tokenization, and lemmatization to standardize wording. Special attention is given to detecting monetary values, coverage terms, and policy-specific keywords.<br>
3.	Similarity Matching: Using SentenceTransformer, the script calculates similarity scores between corresponding sections of the old and new policies. This helps align clauses that may have been reworded or slightly modified.<br>
4.	Coverage Analysis: Differences in numerical values, such as coverage limits, deductibles, and exclusions, are flagged. Unmatched clauses—sections appearing in one policy but not the other—are also identified and categorized.<br>
5.	Annotation & Output: Detected discrepancies are annotated directly onto the PDF using PyMuPDF, making it easier for reviewers to spot changes. Additionally, results are stored in a structured database for tracking and retrieval.

This automated approach enhances accuracy and efficiency in policy comparison, ensuring that all changes are documented clearly for review.

### How It Works
1. Extract Text with Metadata
The ```extract_text_with_metadata``` function reads the PDF and extracts each line of text, along with its page and line number.

2. Identify Coverage Lines
The ```extract_coverage_lines``` function searches for:
   - Lines containing pre-defined keywords like "Coverage" or "Deductible".
   - Lines with numerical patterns representing monetary values.

3. Compare Lines
The ```compare_coverage_lines``` function:
   - Computes embeddings for extracted lines using the all-MiniLM-L6-v2 model.
   - Measures the semantic similarity of lines between the two PDFs.
   - Highlights differences in text or associated numerical values.

4. Extract Numerical Values
The ```extract_values``` function identifies and standardizes numerical values (e.g., $10,000 → 10000).

5. Highlight Differences
Results are returned as a list of dictionaries, each detailing:
   - The text difference.
   - Pages and lines from both PDFs.
   - Discrepancies in values, if applicable.
   - This is so we can easily store in the DB

### Example Output
The output is a list of differences, with each item structured as:
```` 
{
    "title": "Value difference for: Limit of Insurance",
    "policy1": "Limit of Insurance: $10,000",
    "policy2": "Limit of Insurance: $15,000",
    "policy1Page": 3,
    "policy2Page": 4
    }
````
### Customization
You can customize the following:
- **Keywords:** Modify the ```keywords``` list to target specific terms.
- **Similarity Threshold:** Adjust the threshold in ```compare_coverage_lines``` for determining semantic matches (default: ```0.8```).

### Limitations
- **OCR:** Requires PDFs with selectable text. For scanned documents, use an OCR tool before processing.
- **Keyword Sensitivity:** Relies on the predefined list of keywords and may miss context-specific terms.

### Acknowledgments
	•	pdfplumber for accurate and structured text extraction from PDFs.
	•	Sentence Transformers for providing robust pre-trained models for text similarity comparison.
	•	NLTK for tokenization, lemmatization, and text preprocessing.
	•	Scikit-learn for its utilities in text processing and similarity analysis.
	•	PyMuPDF for annotating and modifying PDFs to highlight policy changes.


# Project-Status Milestone 3
Feb 16, 2024

### Requirements Table


| Requirement                         | Description                                                                                                                                                           | Status         |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| **Login Form**                      | For login functionality, take text from username and password inputs. Clean information to protect from malicious input.                                              | Functional     |
| **Login Function**                  | For login functionality, take cleaned text from frontend and query database with login credentials.                                                                   | Functional     |
| **Registration Form**               | For registration functionality, take text from username and password inputs. Clean information to protect from malicious input. Hash sensitive information.           | Functional     |
| **Registration Function**           | For registration functionality, take cleaned credentials from frontend and write to the database of employees.                                                        | Functional     |
| **Client/Document Search Bar Form** | For client search, take text from search bar form input and clean text to prevent malicious input.                                                                    | Functional     |
| **Client Database Function**        | For client search, take cleaned text and use it to query a database of documents/clients. Return results to frontend to be displayed.                                 | Functional     |
| **New Comparison Frontend**         | For new comparisons, prompt the user to upload a file via button, sending the file to the backend for database processing.                                            | Functional     |
| **New Comparison Backend**          | For new comparisons, take file from frontend and write it to database of documents, read database for file to compare to. Send both files to frontend for displaying. | Functional     |
| **Extract Text**                    | For the ML model. Extract the text in the PDF.                                                                                                                        | Functional     |
| **Preprocess Extracted Text**       | For the ML model. Preprocess the text by removing punctuation, special characters, uppercase, etc.                                                                    | Functional     |
| **Convert Policies to Vectors**     | For the ML model. Convert the cleaned text to vectors for numerical representation                                                                                    | Functional     |
| **Compare Document Features**       | Compare the vectors and return the diffs                                                                                                                              | Functional     |
| **Highlight Differences**           | For the ML model. Predict if differences exist.                                                                                                                       | Functional     |
| **Display Past Comparisons**        | Send a request to backend and retrieve a list of past comparisons for a client.                                                                                       | Functional     |
| **Retrieve Past Comparisons**       | Queries database and returns a list of comparisons.                                                                                                                   | Functional     |
| **Team History and Activity**       | Read from teams and documents tables in the database, displaying information to users.                                                                                | Non-Functional |
| **Export Comparison as PDF**        | List out comparisons in a CSV file and convert that to a PDF. File can then be downloaded from the application.                                                       | Functional     |
| **Promotion**                       | For admin, give/remove privileges.                                                                                                                                    | Functional     |
| **Demotion**                        | For admin, remove privileges.                                                                                                                                         | Functional     |
| **Create Team**                     | New “team” initiated in the teams database with no members.                                                                                                           | Functional     |
| **Delete Team**                     | Team which is currently in the teams database is removed.                                                                                                             | Functional     |
| **Add Team Member**                 | A manager will be able to add brokers as members to a team that has already been created.                                                                             | Functional     |
| **Remove Team Member**              | A manager is able to remove a broker from being a member of a particular team.                                                                                        | Functional     |
| **View Analytics on the Team**      | A manager will be able to view statistics such as the number of policies compared on a per team basis.                                                                | Non-Functional |
| **Create Comment**                  | Add a new comment linked to a particular point in a comparison document                                                                                               | Functional     |
| **Delete Comment**                  | Remove a previously created comment from a particular policy comparison                                                                                               | Functional     |
| **Edit Comment**                    | Edit the message from a previously created comment                                                                                                                    | Functional |
| **Show/Hide Comments**              | Selecting this will either show or hide all comments that have been created for a particular comparison document                                                      | Non-Functional |


___


ARCHITECHTURE DIAGRAM:
![SystemArchitechture drawio](https://github.com/user-attachments/assets/490e15c7-5621-489b-a8b7-8c982f677cdf)
## Software Architecture Diagram Description

### Outer Layer: Docker Container (Parent)

Represents the overarching Docker container that orchestrates the three internal containers.

### Three Internal Docker Containers:

#### Frontend Container
- Technology: React (TypeScript), shadCN components, Tailwind CSS
- Structure:
- Pages: Main, Login, Highlighted Differences, Help, Comparison, Admin, Activity Log, About, Profile
- Components: Reusable UI elements
- Interaction: Sends HTTP requests (e.g., axios.post) to the Backend Container
- Flow: Renders UI based on JSON responses from the Backend

#### Backend Container
- Technology: Python, Django Framework
- Structure: Views (business logic) handling requests from the Frontend
- ML Model for Insurance Comparison: Integrated within the Django controller views, an ML model leverages libraries like pdfplumber and PyMuPDF for PDF parsing, Sentence Transformers for text embeddings, and scikit-learn for machine learning tasks to process insurance data and generate comparisons, which are then returned as JSON responses to the Frontend.
- Interaction:
Receives Axios requests (e.g., FETCH_DIFFERENCES) from Frontend
Queries the Database Container via SQLAlchemy ORM
Returns JSON responses to Frontend
- Pattern: MVC (Controller logic resides here)

#### Database Container
- Technology: MySQL
- Structure: Tables mapped via SQLAlchemy ORM in Python
- Interaction: Responds to Backend queries, stores/retrieves application data
- Data Flow:
	- Request Path: Frontend → Backend (via Axios HTTP requests, e.g., POST with multipart/form-data) → Database (SQL queries via SQLAlchemy)
	- Response Path: Database → Backend (query results processed by ML model in views) → Frontend (JSON data rendered in React components)
- Pattern: MVC

- Model: MySQL Database + SQLAlchemy ORM
- View: React Frontend (Pages/Components)
- Controller: Django Views in Backend (including ML model for insurance comparison)


This forms a classic three-tier architecture (Presentation, Application, Data) running within a Dockerized environment, enhanced with an ML model for insurance comparison embedded in the Backend’s controller logic.



LEVEL 1 DFD
![data_flow-LEVEL 1 drawio](https://github.com/user-attachments/assets/90ec95e3-066a-475b-a20f-56bcef846670)
# Level 1 Data Flow Diagram (DFD) Description

## External Entities (Users):

##### Brokers
Interact with the system to perform actions like generating comparisons, reviewing differences, viewing comparisons, managing comparisons, getting app help, and learning about the app.
##### Administrators
Have all the capabilities of brokers, plus additional administrative functions like managing users and managing teams.
Data Stores (Database Tables):

The system uses a single database with the following tables:

##### Users: Stores user credentials, profiles, and roles (e.g., broker or administrator).
##### Teams: Stores team names and member associations.
##### Comparisons: Stores metadata about comparisons (e.g., comparison ID, associated documents).
Differences: Stores the differences identified by the ML model, including confidence scores, broker evaluations (good/bad), and comments.

## Main Processes:

### 1. Complete Login
Input: User (Broker/Administrator) inputs credentials (username, password).
Process: Validates credentials by querying the Users table in the database.
Output: If valid, loads the user profile and directs the user to the Manage Comparisons section (main homepage).
Data Flow:
Credentials → Complete Login → Query to Users table
Users table → User profile → Manage Comparisons

### 2. Get App Help
Input: User (Broker/Administrator) requests help resources.
Process: Retrieves static help content (tutorials, FAQs, etc.) and displays it to the user.
Output: User views help content (tutorials, FAQs).
Data Flow:
User request → Get App Help → Help content displayed

### 3. Learn About App
Input: User (Broker/Administrator) navigates to the About page.
Process: Retrieves static content about the app, team members, and technologies used.
Output: User views About page content.
Data Flow:
User request → Learn About App → About content displayed

### 4. Review Stats
Input: User (Broker/Administrator) requests application statistics.
Process: Queries the database (likely the Comparisons and Differences tables) to gather data for three graphs.
Output: Populates and displays three graphs with relevant statistics.
Data Flow:
User request → Review Stats → Queries to Comparisons/Differences tables
Query results → Review Stats → Graphs displayed

### 5. Generate Comparison
Input: Broker uploads two PDF documents.
Process: The ML model processes the PDFs to identify differences, which are then saved into the database.
Output: Differences are stored in the Differences table, and the comparison metadata is stored in the Comparisons table.
Data Flow:
PDF documents → Generate Comparison → ML model processing
Identified differences → Differences table
Comparison metadata → Comparisons table

### 6. Review Differences
Input: Broker selects a comparison and reviews the differences identified by the ML model.
Process: Retrieves differences from the Differences table, including confidence scores. Broker evaluates differences (marks as "good" or "bad," or adds comments).
Output: Evaluations and comments are saved back to the Differences table.
Data Flow:
Broker request → Review Differences → Query to Differences table
Differences with confidence scores → Review Differences → Broker evaluations/comments
Evaluations/comments → Differences table

### 7. View Comparison
Input: User (Broker/Administrator) selects a comparison to view.
Process: Retrieves comparison metadata from the Comparisons table and associated differences from the Differences table.
Output: Populates the comparison view with differences for the user to see.
Data Flow:
User request → View Comparison → Queries to Comparisons and Differences tables
Comparison data and differences → View Comparison → Displayed to user

### 8. Manage Comparisons
Input: User (Broker/Administrator) searches or selects a comparison.
Process: Queries the Comparisons table to list available comparisons. User can click to view a comparison.
Output: Displays a list of comparisons; triggers the View Comparison process when a comparison is selected.
Data Flow:
User request → Manage Comparisons → Query to Comparisons table
List of comparisons → Manage Comparisons → Displayed to user
Selection → Triggers View Comparison

### 9. Manage Users
Input: Administrator accesses the admin panel after logging in.
Process: Queries the Users table to retrieve a list of users. Administrator can edit or delete users, sending updates to the database.
Output: Updated user list is reflected in the view and database.
Data Flow:
Admin request → Manage Users → Query to Users table
List of users → Manage Users → Displayed to admin
Edit/Delete actions → Users table → Updated view

### 10. Manage Teams
Input: Administrator accesses the admin panel to manage teams.
Process: Queries the Teams table to retrieve a list of teams. Administrator can modify team names or members, sending updates to the database.
Output: Updated team list is reflected in the view and database.
Data Flow:
Admin request → Manage Teams → Query to Teams table
List of teams → Manage Teams → Displayed to admin
Edit actions → Teams table → Updated view
Data Flows Summary:

Brokers: Interact with processes like Generate Comparison, Review Differences, View Comparison, Manage Comparisons, Get App Help, Learn About App, and Review Stats.
Administrators: Interact with all broker processes, plus Manage Users and Manage Teams.
Database Interactions: All processes involving data retrieval or updates interact with the appropriate tables (Users, Teams, Comparisons, Differences).

# Metrics Report (2025-02-12)

## Accuracy Analysis

To evaluate the accuracy of our application's policy comparison feature, we conducted a manual comparison between two sample documents:

- **Old Policy 2:** 9 pages
- **New Policy 2:** 7 pages

### Manual Review
A thorough manual review was conducted by highlighting all actual differences between the two documents. This process identified a total of **25 differences**.

### Application Results
Our application detected **18 differences**. Among these:

- **9 differences** correctly matched the manually identified differences.
- **9 differences** were either incorrect or slightly inaccurate.

### Accuracy Metrics
To quantify the application's performance, we calculated the following metrics:

- **Precision (Positive Predictive Value)**: Measures how many of the detected differences were actually correct.

  Precision = True Positives / (True Positives + False Positives)

  Precision = 9 / (9 + 9) = 9 / 18 = 50%

- **Recall (Sensitivity)**: Measures how many of the actual differences were correctly identified.

  Recall = True Positives / (True Positives + False Negatives)

  Recall = 9 / (9 + 16) = 9 / 25 = 36%

- **F1 Score**: The harmonic mean of precision and recall, balancing false positives and false negatives.

  F1 Score = 2 * (Precision * Recall) / (Precision + Recall)

  F1 Score = 2 * (0.50 * 0.36) / (0.50 + 0.36) ≈ 42%

### Summary

| Metric    | Value  |
|-----------|--------|
| Precision | 50%    |
| Recall    | 36%    |
| F1 Score  | 42%    |

The results indicate that while our application can identify some differences accurately, there is significant room for improvement in both precision and recall. Enhancing the model's ability to correctly detect true differences while minimizing incorrect detections will be crucial in future iterations. A large part of this inaccuracy was due to issues in identifying differences that were not value differences; meaning they were differences in legal jargon.

## Efficiency and Time Analysis

To assess the efficiency of our application's comparison feature, we conducted tests on different document sizes and recorded the average processing times:

| Document Size | Average Comparison Time |
|---------------|-------------------------|
| 16 pages      | 10 seconds              |
| 100 pages     | 50 seconds              |
| 200 pages     | 110 seconds             |

These results suggest that the application's processing time scales linearly with document length. While the performance is acceptable for medium-sized documents, further optimizations may be required to handle larger documents efficiently without significantly increasing processing time. We are planning to attempt to incorporate parallel processing to increase efficiency.

This report evaluates the performance of the policy comparer in analyzing and comparing insurance policy documents. The analysis was conducted on two sets of shortened policy documents (Set 2 from the provided ones), and the full documents. Key performance metrics considered include execution time, accuracy, comprehensiveness, and efficiency. The comparator successfully highlighted policy modifications, including changes in premiums, adjustments in coverage, updates to named insureds, and modifications to certain clauses. The detection accuracy was ok (needs improvement), ensuring that a good amount of critical differences were captured. The execution time was efficient, taking between 4-10 seconds for the shortened set of policies and approximately 40 seconds to a minute for a full document comparison. This indicates a scalable execution time relative to document size, which is a crucial factor for processing bulk data efficiently.

The comparer performed well in identifying policy changes, but there are areas for improvement. Implementing parallelized comparisons could further reduce execution time, and automated summarization could enhance readability. Additionally, scalability testing on larger datasets can help validate performance under high loads. Future enhancements should focus on improving report generation for better user insights. Our current plan is to add highlighting based on confidence interval to better help brokers understand the differences present between policies. Overall, the policy comparer demonstrated strong performance in efficiency and decent performance in accuracy, making it a valuable tool for policy analysis and comparison. With our future UI/UX updates we plan to have ready upon deployment, we anticipate an even better experience for brokers without having to focus too much on improving performance metrics such as parsing, accuracy and speed.

# Features & Bugs
## Features
### Account
- Individual accounts for brokers to manage insurance policies
- Admin account to manage teams of brokers as well as individual accounts for brokers
- Users can view their account activity from the activity log
- Users can change their info in the account page

### Teams
- Brokers are assigned a team by an admin account where they will then be able to see all documents and policies being worked on by team members
- Admins can delete and edit these teams from the admin page

### Policies
- Users can upload policies
- Users can create comparisons from 2 uploaded policies
- Users can search for comparisons
- Users can delete comparisons
- Users can leave comments and feedback on individual differences within a comparison
- Users can delete differences within a comparison
- Users can view highlighted differences from a highlighted differences tab
	- Highlighted differences are color coded to show confidence levels
	- Users can download the highlighted pdfs

### System
- Dark mode
- Multilingual support
- Help & FAQ page

## Known Bugs
- Color coded differences do not show on the comparison page
- Dead links on Help & FAQ page
- Docker container needs restart on intial build

# System Walkthrough
## Running the Docker Container
To run the docker container, start by running the command ```docker-compose up --build``` in the terminal.

Once the terminal shows the following image, the container is built and we can navigate to port 5173 to view the site. 

## Navigating the site
Upon navigating to localhost:5173 you will see the following login page:

![Screenshot 2025-04-09 215334](https://github.com/user-attachments/assets/079a6310-121b-46a8-96c6-d842f18e9100)

Login with the admin credentials to view all aspects of the site. Once logged in, you should recieve a confirmation toast for your login and will be directed to the main page of the site. 

![Screenshot 2025-04-09 215620](https://github.com/user-attachments/assets/7429ca00-4381-489a-9635-bafa2b0880cf)

### Main Page

- SUN: Dark mode toggle
- GLOBE: Language toggle between English/French
- ?: Help and FAQ page
- ABOUT: About page
- PROFILE: Brings up toggle menu with personal info button, activity log and admin page

Clicking on the new comparison button will prompt a small menu to upload pdfs in order to generate a new comparison. 

### Comparison Page

Upon clicking on Comparison 1, we can see the following page:

![Screenshot 2025-04-09 221023](https://github.com/user-attachments/assets/e9a26a73-f547-4e08-86bf-889baecc2191)

We can now see the differences that the ML model found during its analysis. It will tell you the difference and the page it was found on. To the right of the difference, we can see a small feedback panel where brokers can approve, disapprove or write comments on differences. At the top of the page, we can also see 3 buttons. A download summary button to download a summary of all the differences found in the two compared documents along with any feedback from other brokers. Next to that is a Highlighted Text button that lets you view where the comparisons were made on the original document highlighted for ease of access. You can also download the highlighted document as well. Last is the self explanatory Delete Comparison button. 

The last page on the walkthough is the Admin page where admin users can create teams and accounts for brokers.

### Admin Page

![Screenshot 2025-04-09 220017](https://github.com/user-attachments/assets/77bed837-4135-4e7b-8f08-e115d8c8d689)

We can switch between looking at users and looking at teams with the button on the left. The button on the right allows you to create a team/user by filling out a form with information such as name, team, etc.

