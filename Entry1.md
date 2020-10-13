# Entry 1: Installing Haskell
Hello, my name is Garrett and I am a junior computer science major at Chapman University. I am running Haskell on  a Windows desktop, so the following will be instructions for that particular configuration.
### Step 1: Installing Chocolatey
To install Haskell on Windows, instructions are provided at https://www.haskell.org/platform/. For this process, a tool called Chocolatey will be used and can be installed from https://chocolatey.org/install. This will make the process of installing packages and Haskell streamlined and easy to do from a command line.

### Step 2: Installing Haskell
After the installation completes, you may run these commands at an elevated command prompt to install Haskell:
`choco install haskell-dev`
`refreshenv`
### Step 3: Installing GHC
Using Chocolatey, we will also install ghc via this command:
`choco install ghc`

### After installation
Once you have everything set up, you can type `ghci` into the console to pull up the interactive environment where expressions can be written and interpreted in Haskell. You will know it is open with it says `Prelude>` before the cursor. To test it, you may type an expression out such as `1+2` which will return and print to the console `3`. You may also type something like `x = 5`, hit enter, then type `x` and it will return the value of x, which is 5.
