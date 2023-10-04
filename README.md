# Android DevOps Roadmap

# Ensure code quality
### Practical 1
#### Linting with ktlint
 - Integrate ktlint in [Practical 24](https://github.com/canopas/android-developer-roadmap-2023#practical-24)
 - Write the following rules
   - Enforce [naming conventions]((https://kotlinlang.org/docs/coding-conventions.html#naming-rules)) for functions, packages, and properties.
   - Ensure a consistent [order of modifier](https://kotlinlang.org/docs/coding-conventions.html#modifiers-order).
   - Limit the line length to a maximum of 100 characters.
 - Write GitLab CI script to run lint
   - Create a repository on GitLab if one doesn't already exist
   - Configure the script to run ktlint as part of the CI/CD pipeline.
   - Ensure that the linting process runs on each commit.
 
### Practical 2
#### Linting with ktlint
- Integrate ktlint in [Practical 23](https://github.com/canopas/android-developer-roadmap-2023#practical-23)
- Create a GitHub repository for the Practical if one doesn't already exist.
- Write the following rules
  - Add functions, packages, property [naming rule](https://kotlinlang.org/docs/coding-conventions.html#naming-rules)
  - Ensure consistent [order of modifier](https://kotlinlang.org/docs/coding-conventions.html#modifiers-order)
  - The line shouldn't be longer than 100
  - Files shouldn't be longer than 250 lines 
- Write GitHub Action to run lint
  - Create a GitHub Actions workflow file in the project repository.
  - Configure the workflow to run ktlint as a check on each commit.
  - Ensure that the linting process is triggered automatically.
-  Write a pre-commit hook for lint check
   - Write a pre-commit hook script.
   - Configure the hook to run ktlint checks before allowing commits.
   - Prevent commits that don't pass the linting checks.

### Practical 3
#### Linting with konsist
##### Enforce specific coding standards and practices.
- Integrate konsist in [Practical 17](https://github.com/canopas/android-developer-roadmap-2023#practical-17)
- Create a GitLab repository for the Practical if one doesn't already exist.
- Define and implement the following konsist tests:
  - Classes extending 'ViewModel' should have a 'ViewModel' suffix.
  - Activity should have an Activity suffix.
  - The project should not have an empty file.
  - Every viewModel should have Unit tests.
  - Every ViewModel's constructor parameter has a name derived from the class name.
  - ViewModel should not have context in the constructor parameter.
  - Model package should not contain data classes.
  - ViewModel should be annotated by HiltViewModel.
  - ViewModel should not have an android package.
- Write GitLab CI script to run konsist tests
  - Create a .gitlab-ci.yml script in the project root.
  - Configure the script to run konsist tests as part of the GitLab CI/CD pipeline.
  - Ensure that the tests are executed automatically on each commit.

### Practical 4
#### Linting with konsist
- Integrate konsist in [Practical 24](https://github.com/canopas/android-developer-roadmap-2023#practical-24)
- Write the following konsist tests
  - Classes extending 'ViewModel' should have a 'ViewModel' suffix
  - Activity should have an `Activity` suffix
  - The project should not have an empty file
  - Every viewModel should have Unit tests
  - Every ViewModel's constructor parameter has a name derived from the class name
  - ViewModel should not have context in the constructor parameter
  - Model package should not contain data classes
  - Viewmodel should be Annoted by `HiltViewModel`
  - Viewmodel should not have an `android` package
- Write GitHub Action to run lint
  - Create a repository on GitHub
  - Configure the workflow to run konsist tests as a check on each commit.
  - Ensure that the tests are executed automatically on each commit.
- Pre-commit Hook:
  - Write a pre-commit hook script.
  - Configure the hook to run konsist tests before allowing commits.
  - Prevent commits that don't pass the linting checks.

# Configure build variant
### Practical 5
#### Create dev and prod flavours
 - Use [Practical 27](https://github.com/canopas/android-developer-roadmap-2023#practical-27)
 - The project will have two flavours - "prod" and "dev," each with distinct configurations:
 - prod Flavor:
    - Uses the "prod-db" Firestore database.
    - Apply a specific theme for the production environment.
 - dev Flavor:
   - Uses the "dev-db" Firestore database.
   - Apply a different theme for the development environment.

# Genrate apk/bundle
### Practical 6
#### Genrate Apk & bundle on gitlab
 - Generate APK/bundle of [Practical 26](https://github.com/canopas/android-developer-roadmap-2023#practical-26)
 - Create a GitLab repository for the Practical if one doesn't already exist.
 - Configure the script to: 
    - Build the APK and AAB for the debug variant.
    - Set up the GitLab CI/CD pipeline to run on merging MRs
    - Save the generated APK as a job artificat.

### Practical 7
#### Genrate Apk & bundle on github
 - Generate APK/bundle of [Practical 25](https://github.com/canopas/android-developer-roadmap-2023#practical-25) 
 - Create a GitHub repository for the Practical if one doesn't already exist.
 - Configure GitHub Actions Workflow script to: 
    - Build the APK and AAB for the debug variant.
    - Set up the GitLab CI/CD pipeline to run on merging MRs
    - Save the generated APK as a job artificat.

# Signing apk/bundle
### Practical 8
#### Genrate signed Apk & bundle on gitlab
 - Generate signed APK/bundle of [Practical 29](https://github.com/canopas/android-developer-roadmap-2023#practical-29)
 - Automate the build generation using a GitLab CI/CD script.
 - Store the keystore and credentials as environment variables for security.
 - The script should run on merging MRs.

### Practical 9
#### Genrate signed Apk & bundle on github
- Generate signed APK/bundle of [Practical 21](https://github.com/canopas/android-developer-roadmap-2023#practical-21)
- Write GitHub Action to genrate build
  - Create a repository on GitHub
  - Automate build generation with GitHub Action
  - It should run on merge PR
  - Store generate keystore and credential as Git secrets
  - Save APK after the build job completed

# Automate testing
### Practical 10
#### Unit testing on gitlab
- Write GitLab CI script to run the unit test of [Practical 24](https://github.com/canopas/android-developer-roadmap-2023#practical-24)
  - Create a repository on GitLab
  - Automate unit testing with GitLab CI
  - It should run on each commit

### Practical 11
#### Unit testing on github
- Write GitHub Action flow to run the unit test of [Practical 24](https://github.com/canopas/android-developer-roadmap-2023#practical-24)
  - Create a repository on GitHub
  - Automate unit testing with GitHub CI
  - It should run on each commit
  - Write a hook for the unit test
 
# Auto deployment
 ### Practical 12 
  - Write a script to deploy the bundle on Play Store of [Practical 25](https://github.com/canopas/android-developer-roadmap-2023#practical-25)
  - Integrate Fastlane
  - Write GitLab CI script to deploy a bundle
    - It should run on the master branch
  - Write a GitHub Action script to deploy a bundle
    - It should run on the tag creation 


