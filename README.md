# typescriptStarter

## Initial Setup

1. Create Project Structure:

    ```Script
    proj/
    ├─ dist/
    └─ src/
       └─ components/
    ```

2. Initialize git

    ```bash
    cd proj
    git init
    git config user.name "Your Name"
    git config user.email "Your Email"
    ```

    1. Create a github repo eg. "typescriptStarter"

    2. Prepare credentials for remote project
        1. If you do not have multiple github user accounts:

            ```bash
            ssh-keygen -t rsa -b 4096
            ```

            Copy the contents of the **id_rsa.pub** file under **~/.ssh/** directory and add it to your github user's ssh keys.

        2. If you have multiple github accounts:

            ```bash
            ssh-keygen -t rsa -b 4096
            mv ~/.ssh/id_rsa ~/.ssh/id_rsa_your_github_user
            mv ~/.ssh/id_rsa.pub ~/.ssh/id_rsa.pub_your_github_user
            ```

            And create a file named **config** in **~/.ssh** with the following contents:

            ```Script
            Host github.com-your_github_user
                Hostname github.com
                User git
                IdentityFile ~/.ssh/id_rsa_your_github_user
            ```

            Then you need to change permissions on the config file

            ```bash
            chmod 600 ~/.ssh/config
            ```

            Finally copy the contents of the **id_rsa.pub_your_github_user** file and add it to your github user's ssh keys.

    3. Add remote repository to local git setup:

        1. If you do not have multiple github user accounts:

            ```bash
            git remote add origin git@github.com:your_github_user/your_project_name.git
            ```

        2. If you have multiple github user accounts:

            ```bash
            git remote add origin git@github.com-your_github_user:your_github_user/your_project_name.git
            ```

    4. Create the **.gitignore** file and populate it as suggested in the file included in this repository.

3. Initialize project:

    ```bash
    npm init
    ```

4. Install typescript and webpack globally

    ```bash
    npm install -g typescript webpack
    ```

5. Install React and React-Dom locally

    ```bash
    npm install --save react react-dom @types/react @types/react-dom
    ```

6. Install Typescript dependencies for development

    ```bash
    npm install --save-dev typescript awesome-typescript-loader source-map-loader
    ```

7. Create a **tsconfig.json** file and populate it as suggested in the file included in this repository.

8. If you are using Visual Studio Code, install the following:

    1. Prettier plugin and prettier npm package:

        ```bash
        npm install -g prettier
        ```

    2. Quokka, markdownlint, Markdown Preview Enhanced, Git History, Git Project Manager, GitLens, TSLint, npm, & npm Intellisense

        Create a **.quokka** file in home directory and add the following to it:

        ```Script
        {
            "babel": true
        }
        ```
