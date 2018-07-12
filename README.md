# Image Search using Go

`Problem Statement`: Tag images using Clarifai's API & storing it to in-memory data structure. To build a simple search engine interface for images using Golang.

`Requirements`:
**Operating System used**: Windows 10
**Go version**: go version go1.9.2 windows/amd64
**Dependencies**: GJSON library

`How to run the Program`:
1. Install 'go1.9.2windows/amd64' version of golang in your windows operating system.
2. Unzip the attached folder & copy it to C drive.
3. Set the path variable of 'Go' to this folder(C:\Projects\Go) using below steps:
	i) go to System->Advanced System Settings->Environment Variables
	ii) click 'New' under 'System Varaibles'
	iii) Set the variable name to 'GOPATH' and value to your Go workspace path where you copied the unzipped folder.(e.g. C:\Projects\Go)
	iv)You can quickly check to ensure your path has been set by opening the command line and typing "echo %GOPATH%" and check the output,it shuold be pointing to unzipped folder.
4. Open Command line & go to 'C:\Projects\Go' (cd Projects/Go) & run 'go get -u github.com/tidwall/gjson' to install the 'GJSON' library
5. Now, change directory to 'clarifai_ImageSearch' (cd src/clarifai_ImageSearch) & type 'go build'. This will build executable named 'clarifai_ImageSearch.exe' in the directory alongside source code.
6. Execute the above executable to run the program (clarifai_ImageSearch.exe & hit Enter). As, we are calling Clarifai's API to get tags for each image & there are 1000 images to process,which will take around 5-10 min for all images to get processed.
7. Once all images got processed, it will ask user to provide input tag. User can enter any word. (e.g. travel, boy, no person)
8. Based on the input tag, program returns at most 10 images which are most relevant to it. If tag is not present then it will show appropriate message to user.
