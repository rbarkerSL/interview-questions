### Interview Problem: **CI/CD Pipeline for a Java Library Using Gradle**

#### **Scenario:**
You are tasked with setting up a CI/CD pipeline for a Java library project. The project uses Gradle as the build tool, and the final output is a JAR file. The goal is to automate the build and testing process, and simulate publishing the JAR to a repository.

Your task is to configure a GitHub Actions workflow that automates the following steps whenever changes are merged into the `main` branch.

#### **Requirements:**
1. **Build & Test:**
   - Set up a GitHub Actions workflow that:
     - Runs unit tests on the Java library.
     - Builds the JAR file using Gradle.
   - Ensure the build fails if any tests fail or if there are issues with the build process.

2. **Versioning:**
   - Implement a simple versioning strategy:
     - Either manually set a version in the Gradle build script, or use the current Git commit hash as a version.

3. **Simulated Publishing:**
   - Instead of publishing to Sonatype, simulate the publishing process by:
     - Publishing the built JAR to a local Maven repository or simply packaging the JAR and uploading it as an artifact in the GitHub Actions workflow.
   - Outline how you would configure the pipeline to publish the JAR to Sonatype in a real-world scenario.

4. **Notifications:**
   - Configure the workflow to notify the team via email or Slack once the JAR is successfully built and "published."

#### **Deliverables:**
1. **Pipeline Design:**
   - Provide a brief written explanation or a diagram of the CI/CD pipeline design, detailing each step of the process.

2. **Sample Workflow Configuration:**
   - Implement a GitHub Actions workflow file (`.yml`) that:
     - Runs the build and test steps using Gradle.
     - Simulates the publishing process by either uploading the JAR as an artifact or publishing it to a local Maven repository.

3. **Implementation Considerations:**
   - Describe how you would handle:
     - Versioning to ensure that each built JAR has a unique version.
     - Managing sensitive information like repository credentials if this were a real deployment.

4. **Bonus:**
   - Suggest how you would automate the rollback process if a JAR was "published" with issues.
   - Propose a strategy for validating the published JAR in a real scenario (e.g., running integration tests against the artifact).

### **Time Frame:**
This task should take about 2-4 hours to complete. We typically give 2 working days to complete the task.

### **Evaluation Criteria:**
- **Pipeline Design:** The clarity and completeness of your pipeline design, ensuring it covers all necessary steps.
- **Workflow Configuration:** The accuracy and quality of your GitHub Actions workflow, including how well it integrates with Gradle.
- **Problem-Solving:** Your ability to address potential challenges and propose solutions for reliable and efficient JAR handling.
- **Bonus Solutions:** Creativity in proposing solutions for rollback automation and artifact validation.
