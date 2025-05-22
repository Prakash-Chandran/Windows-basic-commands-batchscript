# Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations

## COMMAND AND OUTPUT
Create a directory named "my-folder"

Remove the directory "my-folder"

![1](https://github.com/user-attachments/assets/0d92f625-9ee5-4689-8356-48ee68b9d236)

## COMMAND AND OUTPUT

Create the file Rose.txt

![2](https://github.com/user-attachments/assets/4ab416c4-c452-440d-90a3-d00e1e1126ec)

## COMMAND AND OUTPUT

Create the file hello.txt using echo and redirection

![3](https://github.com/user-attachments/assets/588bbccc-f516-4aa4-aa4b-e5b6ab781336)

## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt

![4](https://github.com/user-attachments/assets/3ada5a9f-9fbe-4731-aa94-82c936082400)

## COMMAND AND OUTPUT

Remove the file hello1.txt

List out the file hello1.txt in the current directory

![5](https://github.com/user-attachments/assets/d40237ad-c12d-4ace-9313-b151d2fe8957)

## COMMAND AND OUTPUT

List out all the associated file extensions 

![6](https://github.com/user-attachments/assets/a1487e8f-02c6-41f1-a2de-852a1ed43227)

## COMMAND AND OUTPUT

Compare the file hello.txt and rose.txt


## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

## PROGRAM
```
@echo off
set name=John
echo Hello, %name%!
pause

```

## OUTPUT

![8](https://github.com/user-attachments/assets/622c36c5-7d20-4b1d-b8b3-68de92794b95)


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

## PROGRAM
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause

```

## OUTPUT

![9](https://github.com/user-attachments/assets/e2c35a3f-6bff-4d53-8042-362d49fb66df)


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

## PROGRAM
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```

## OUTPUT

![10](https://github.com/user-attachments/assets/2c6dabf6-e7af-4746-a3c6-71fc27136738)


Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## PROGRAM 
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause

```

## OUTPUT

![11](https://github.com/user-attachments/assets/bad7f7e1-c558-41ed-8d1e-2ba09aa01bf0)


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

## PROGRAM 
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause

```

## OUTPUT

![12](https://github.com/user-attachments/assets/f5d65f7c-a5d2-4f82-902d-ddd6d52138ef)

# RESULT:
The commands/batch files are executed successfully.

