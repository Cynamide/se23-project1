### Project 1
Mark Feng
Reuben Thomas
Arjit Agarwal
Sumedh Limburkar

# Project Introduction

For Project 1, we selected the Application Tracking System made by Group 21. The Github repo lists its purpose as: “Our application allows you to track and manage your job application process, as well as regulate it, without the use of cumbersome Excel spreadsheets.” Essentially, it is a piece of software used to help keep track of all of one’s job applications holistically. The first feature is a job application tracker split into the following categories: wishlist, applied, and rejections. It also has a search feature that allows a user to to quickly search a company’s available job openings using basic keywords. These two features are linked together so that, for example, you can easily add job openings you find from search to your wishlist.

# Setup Difficulties

The initial issue we ran into was that the package versions that were specified by the repo were outdated compared to the pre-installed packages that were available locally on our machine. Not only were we unable to deploy the program, but many of the thrown errors were hard to comprehend.

After we resolved the package version mismatch issue, executing the software went relatively smoothly. Group 21 provided pre-made setup bash scripts that automated almost all of the common setup processes. Once we had completed dependency installation and setup, we realized that the project stored data in a MongoDB database. We weren’t certain how the project specifically implemented MongoDB, which caused us some headache. 

Once we had our MongoDB implemented within our project, deploying the application also went quite smoothly. Included in the set of bash scripts that Group 21 made was a startup script that automated the project deploying process. Whilst the functionality of the application was a bit obtuse and unintuitive, the project’s core featureset was working as intended without any modification.

Although this didn’t directly affect our setup or deployment process, we also encountered a lot of unknown errors in the browser console. The main functionality of the website was seemingly unaffected by this, however these errors were extremely prevalent throughout the project and implies that the Group 21 took on a lot of technical debt for this project.

# Solutions

Utilizing "virtualenv," we established an isolated environment to create a new instance with its own set of installed packages. This separation was important as it helped us solve the mismatched package version problem that we initially ran into while trying to set up and deploy the project for the first time. It also allows us to streamline our dependency management, which helps us avoid the pain of conflicting packages between different computers by enabling precise control over all dependency versions.

To resolve the MongoDB implementation problem, we eventually realized that Group 21 had provided project setup instructions in the Github repository. We decided to use a simple local database for our initial deployment and testing, with plans to eventually move to the cloud so that all team member’s can test using the same set of data.

# Lessons learned for Project 2

We will be using a virtual environment immediately in order to ensure that everyone who is working on the project has the same set of packages. Not only does this immediately address any potential version mismatch that may exist between local and repo files, but it also streamlines the process for our team. By employing a virtual environment, it helps us ensure that there also won’t be any potential version or package mismatches between any of our team member’s computers.

Another potential solution we could use instead of using a virtual environment is to utilize Docker to create our project environment. This would dramatically improve the development pipeline for our team as Docker could not only handle the dependencies of our project but also help us manage things such as version control and project consistency. A better project workflow could allow us to extend the software with more features and spend less time having to address technical debt.

On the subject of technical debt, as mentioned previously there are some signs that this project, despite working correctly, contains many issues that we will have to address. In order to minimize the amount of technical debt we may have in the future as well as prevent any unforeseen consequences and bugs, we intend on addressing this debt as our first contribution to the project. This will help us improve project health in the long run and deal with problems before they come up.
