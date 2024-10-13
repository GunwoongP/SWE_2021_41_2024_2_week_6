This repository includes the summaries for the assignments completed during Week 4 and Week 5 for the Open-Source Software Practice course.

Week 4: iPython (Google Colab) Assignment
In Week 4, we focused on using Google Colab to run iPython (Jupyter Notebook) and solve algorithm problems. The task involved writing Python code to address a specific algorithm challenge, testing it with various test cases, and submitting the solution through GitHub.

Task Summary:
Colab Setup:
Open the provided Google Colab link and save a copy in your Google Drive.
Coding:
Write Python code to solve the algorithm problem and verify the solution using appropriate test cases.
Submission:
Download the notebook as a .ipynb file and rename it as {studentID}_{name}.ipynb.
Create a new GitHub repository named SWE_2021_41_2024_2_week_4.
Upload the file to the repository, write a commit message, and commit the changes.
For more details, refer to the Colab notebook provided in the link above.

Week 5: Docker Assignment
The Week 5 assignment involved creating a Docker container that simulates a development environment with specific requirements, such as a Linux OS, Git, and Python3 installed, along with a bind mount between the host and the container.

Task Summary:
Container Setup:

Use a Docker image based on Ubuntu (either ubuntu or ossp images).
Install Git and Python3 using the following command:
bash
코드 복사
apt-get install -y git python3
Verify the installations:
bash
코드 복사
git --version
python3 --version
Bind Mount:

To check the bind mount configuration, run the following command on the host system:
bash
코드 복사
docker inspect --format="{{ .HostConfig.Binds }}" <container_name>
This will print the path of the mounted directory in the format:
ruby
코드 복사
[<host_dir_path>:<container_dir_path>]
Commands to Execute:

After setting up the container, execute the following commands and capture their output:
bash
코드 복사
docker exec <container_name> cat /etc/os-release
docker exec <container_name> git --version
docker exec <container_name> python3 --version
docker inspect --format="{{ .HostConfig.Binds }}" <container_name>
Submission:

Submit screenshots of the command outputs via iCampus.
For more detailed instructions on using Docker commands, refer to the Docker documentation.
