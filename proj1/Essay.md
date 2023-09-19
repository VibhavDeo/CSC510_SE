## Pain Points

Running and choosing a project was initially a difficult task for our team. Running five projects provided us with valuable insights into the importance of adhering to a structured set of rules and guidelines and maintaining proper documentation for software development. The experience was not without its share of challenges. These challenges ranged from package dependency issues to incorrect installation steps and faulty ‘requirements.txt’ files. 

One of the first major hurdles we encountered was related to package dependencies. Even though the project's documentation provided the command to install the required packages (pip install -r requirements.txt), we faced difficulties due to pre-installed packages on our systems, leading to version conflicts. For instance, the Pymongo package presented compatibility issues. It took us considerable time and discussion to find this error. Ultimately, we resolved it by uninstalling Pymongo and then reinstalling it through the requirements.txt command. A similar issue arose with the MongoDB installation, which was resolved by reinstalling the MongoDB application.

These package-related challenges could have been avoided if the project documentation had emphasized the importance of creating a virtual environment to isolate package installations. This approach would have prevented version conflicts and made the setup process smoother.

Furthermore, the documentation focused primarily on installation steps but did not mention the steps required to run the application after installation. For example, one project omitted the step where it was required to connect to the AWS database while other applications required hosting the product on Heroku. The project we chose required us to connect to MongoDB, forcing us to manually look into code to locate the MongoDB connection string details. Without this connection, the application's graphical interface was hollow and incapable of storing or retrieving any data. 

Moreover, the application had a commented-out function for inserting food data into the database. We recognized that the function needed to be uncommented for the application to update the database. On doing this, we realized that this function was initially disabled to prevent data duplication, as it would insert data every time the application was run. However, this approach raised concerns about data inefficiency and duplication. To address this, we had to modify the MongoDB update clause to ensure data was only inserted if it did not already exist. This situation reinforced the importance of designing code with data integrity in mind from the beginning.

In addition to these challenges, we encountered numerous broken functionalities and unresolved bugs within the application. For instance, the "enter calories" tab malfunctioned as the calorie amount fetched from the database was not parsed correctly. Another significant problem was the hardcoded HTML page for the profile information form, which limited our ability to display user input effectively. Additionally, the history feature was restricted to displaying data only for the account creation date, which was a clear limitation in the application's functionality.


To avoid the challenges and pain we experienced in Project1, we need to adopt several best practices and strategies in Project2. These practices will not only streamline the development process but also enhance the overall quality of the project. Here are some key commitments

•	In Project 2, we will prioritize comprehensive documentation. This includes clear instructions for setting up the application, installing dependencies, and post-installation steps. By addressing these aspects, we will ensure that developers or users can smoothly replicate the project environment. 

•	We will ensure proper management of packages and dependencies including documenting the use of virtual environment if required. This will make the setup process easier for the people who are trying to run the application. We will also make sure to explicitly mention package versions in the requirements.txt file.

•	We will try to write clean and well-structured code from the beginning. This includes implementing data constraints to prevent issues like data duplication, parsing errors, etc., and ensuring the efficiency of data operations. We would perform regular code reviews to maintain code quality.

•	To address broken functionalities and unresolved bugs, we will incorporate thorough testing throughout the development process. This includes creating and executing test cases for all application features to ensure they work as intended.

•	Implementing version control will facilitate collaboration, allow for the tracking of code changes, and provide a safety net in case issues arise during development. We will maintain a separate branch that will host a working build throughout the process and create separate branches for updating and fixing the code.

•	To keep track of tasks, set priorities, and ensure efficient communication within the team we will set up regular meetings to discuss progress and roadblocks.

•	We will try to automate the testing and deployment process to enable us to catch and address issues early in the development cycle and ensure that the application is always in a deployable state.
