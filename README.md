# Image-Search-using-Go

This project searches the 10 most relevant images to the user input. Here, I have used Clarifai's predict API to extract the tags from an image alongwith it's confidence value. Stored this data in-memory data strucutre & applied search functionality on it.

### Dependencies
Operating System used: Windows 10
Go version: go version go1.9.2 windows/amd64
Dependencies: GJSON library

### How to run the program :
1. Install 'go1.9.2windows/amd64' version in your windows system
2. Unzipped the attached folder & copy it to C drive.
3. Set the path variable of 'Go' to this folder using below steps:
	i)go to System->Advanced System Settings->Environment Variables
	ii) click 'New' under 'System Varaibles'
	iii)Set the variable name to 'GOPATH' and value to your Go workspace path where you copied the unzipped folder.(e.g. C:\Projects\Go)
	iv)You can quickly check to ensure your path has been set by opening the command line and typing "echo %GOPATH%" and check the output,it shuold be pointing to unzipped folder.
4. Open Command line & go to 'C:\Projects\Go' & run 'go get -u github.com/tidwall/gjson' to install the 'GJSON' library
5. Now, change directory to 'clarifai_ImageSearch' & type 'go build'. This will build executable named 'clarifai_ImageSearch.exe' in the directory alongside source code.
6. Execute the above executable to run the program. As, we are calling Clarifai's API to get tags for each image. There are 1000 images to process,which will take around 5-10 min for all images to get processed.
7. It will ask user to provide input tag.
8. Based on the input tag, program returns at most 10 images which are most relevant to it.
