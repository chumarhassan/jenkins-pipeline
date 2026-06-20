# Jenkins Pipeline Practice

> A tiny, beginner-friendly Jenkins project for practicing pipeline stages, Python script execution, and trigger-based build testing.

![Jenkins](https://img.shields.io/badge/Jenkins-Pipeline-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![Python](https://img.shields.io/badge/Python-Scripts-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Practice](https://img.shields.io/badge/Project-Practice-2E7D32?style=for-the-badge)

## Overview

This mini project demonstrates a simple Jenkins declarative pipeline.  
The pipeline runs three small Python files in order, representing a basic CI/CD flow.

```text
Build Stage        Test Stage         Deploy Stage
-----------        ----------         ------------
python f1.py  ->   python f2.py  ->   python f3.py
```

## Pipeline Stages

| Stage | File | Command | Result |
| --- | --- | --- | --- |
| Build | `f1.py` | `python f1.py` | Prints `Pipeline project 1` |
| Test | `f2.py` | `python f2.py` | Prints `Pipeline project 2` |
| Deploy | `f3.py` | `python f3.py` | Prints `Pipeline project 3` |

## Project Files

| File | Purpose |
| --- | --- |
| `Jenkinsfile` | Defines the complete Jenkins pipeline with Build, Test, and Deploy stages |
| `f1.py` | Build-stage practice script |
| `f2.py` | Test-stage practice script |
| `f3.py` | Deploy-stage practice script |
| `f4.py` | Extra placeholder practice file |
| `f5.py` | Extra placeholder practice file |
| `initiate trigeer` | Empty marker file used to practice triggering changes |
| `newfile` | Empty marker file for repository-change testing |
| `triggerbuild` | Empty trigger practice file |
| `triggerfile` | Empty trigger practice file |
| `triggerfile2` | Trigger marker containing `triggerfile2` |
| `triggerfile3` | Empty trigger practice file |
| `triggerpipeline` | Trigger marker containing `triggerpipeline` |
| `triggerpipeline1` | Trigger marker containing `triggerpipeline2` |

## Run Scripts Locally

```bash
python f1.py
python f2.py
python f3.py
```

## What You Practice Here

- Creating a basic Jenkins declarative pipeline
- Organizing work into Build, Test, and Deploy stages
- Running Python scripts from a Jenkins `bat` step
- Testing Jenkins builds by changing small trigger files

## Jenkinsfile Preview

```groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'python f1.py'
            }
        }
        stage('Test') {
            steps {
                bat 'python f2.py'
            }
        }
        stage('Deploy') {
            steps {
                bat 'python f3.py'
            }
        }
    }
}
```

