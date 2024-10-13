# SWE_2021_41_2024_2_Week_6

This repository includes the summaries for the assignments completed during Week 4 and Week 5 for the **Open-Source Software Practice** course.

---

## Week 4: iPython (Google Colab) Assignment

In Week 4, we worked with **Google Colab** to run iPython (Jupyter Notebook) and solve algorithm problems. The task involved writing Python code to solve a specific algorithm challenge, testing it with relevant test cases, and submitting the solution via GitHub.

### Task Summary:

- **Colab Setup**:  
  Open the provided Google Colab link and save a copy in your Google Drive.

- **Coding**:  
  Write Python code to solve the algorithm problem and verify the solution with appropriate test cases.

- **Submission**:  
  1. Download the notebook as a `.ipynb` file and rename it to `{studentID}_{name}.ipynb`.  
  2. Create a new GitHub repository named `SWE_2021_41_2024_2_week_4`.  
  3. Upload the notebook file to the repository, write a commit message, and commit the changes.

For more details, refer to the Colab notebook linked in the assignment.

---

## Week 5: Docker Assignment

The Week 5 assignment focused on creating a Docker container that simulates a development environment. The container needed to meet specific requirements, including a Linux OS, Git, Python3, and a bind mount between the host and the container.

### Task Summary:

- **Container Setup**:  
  1. Use a Docker image based on Ubuntu (either `ubuntu` or `ossp` images).  
  2. Install Git and Python3 with the following command:
     ```bash
     apt-get install -y git python3
     ```
  3. Verify the installations by running the following commands:
     ```bash
     git --version
     python3 --version
     ```

- **Bind Mount**:  
  To check the bind mount configuration, run the following command on the host system:
  ```bash
  docker inspect --format="{{ .HostConfig.Binds }}" <container_name>
