# Install Git with Homebrew

Run the following brew command in the terminal:

    brew install git

Then, check the Git version to verify the installation:

    git --version

Locate Git installation folder on Mac OS X

    which git
    
    /usr/local/bin/git.

# Configure Git

The next step is to configure Git by adding your credentials to the system. This is important as it helps keep track of which user is committing changes to a project.

**Define your Git user (should be the same name and email you use for GitHub):**

Open the terminal and configure your GitHub username:

    git config --global user.name “your_github_username”

Then, add your email:

    git config --global user.email "your_email@github.com"
