# SWE_2021_41_2024_2_Week_6

This repository includes the summaries for the assignments completed during Week 4 and Week 5 for the **Open-Source Software Practice** course.

---

## Week 4: iPython (Google Colab) Assignment

In Week 4, we worked with **Google Colab** to run iPython (Jupyter Notebook) and solve algorithm problems. The task involved writing Python code to solve a specific algorithm challenge, testing it with relevant test cases, and submitting the solution via GitHub.

### Task Summary:

- **Colab Setup**:  
  Open the provided Google Colab link and save a copy in your Google Drive.

- **Coding**:  
  Write Python code to solve the algorithm problem of checking whether a number is a "Happy Number."

  ### Happy Number Algorithm
  A *happy number* is a number defined by the following process:
  - Starting with any positive integer, replace the number by the sum of the squares of its digits.
  - Repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle that does not include 1.
  - Numbers for which this process ends in 1 are called happy numbers.

  The code below is the implementation of the happy number problem:
  
  ```python
  def isHappy(n):
      k = set()
      while n != 1 and n not in k:
          k.add(n)
          tmp = 0
          for i in str(n):
              tmp += int(i) ** 2
          n = tmp
      return n == 1
  
  # Example of usage
  print(isHappy(19))  # This will print True since 19 is a happy number
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
