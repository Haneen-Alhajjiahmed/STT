# STT
Live Speech To Text API with Watson + Python

# Pre-requirement 
* You need an IBM Cloud account.
* python 3.4 and above.

## Setup Watson live STT service 
Go to this website [https://cloud.ibm.com/catalog?category=ai#services][https://cloud.ibm.com/catalog?category=ai#services].
You will be forwarded to the AI and machine learning services provided by cloud.ibm.com website. Scroll down to find Speech ti Text option.

<img width="299" alt="Screen Shot 2021-08-16 at 11 13 43 AM" src="https://user-images.githubusercontent.com/85841915/129532751-5cf59951-92f4-4437-8bc3-4b5fe63bee12.png">
This page will be displayed:
Make sure to choose the region and note it down we will be using it later. Then hit Create button.
<img width="1234" alt="Screen Shot 2021-08-16 at 11 17 35 AM" src="https://user-images.githubusercontent.com/85841915/129533386-004617cc-f62c-4642-a82d-7e9b6e5cd2d1.png">
Now this page will be displayed so, we can get our APIKEY.
<img width="1260" alt="Screen Shot 2021-08-16 at 11 25 39 AM" src="https://user-images.githubusercontent.com/85841915/129534264-35a36083-334c-4410-8bca-cf9e67c305b7.png">

## Clone live STT code
Create and name a folder. Then open it with any text editor. I used Visual Stdio Code.
Open a terminal and access the folder you have created.

    $ cd [the folders name or complete path]
This link will allow us to access the live STT code https://github.com/IBM/Watson-streaming-stt. You clone it using git clone command.
   
    $ git clone https://github.com/IBM/Watson-streaming-stt
After running this line of code your folder will have Watson-streaming-stt files. That help us to run our STT code.
<img width="349" alt="Screen Shot 2021-08-16 at 3 25 55 PM" src="https://user-images.githubusercontent.com/85841915/129563533-ebb216ee-12c4-4a75-be40-b59808fa2550.png">

## Installation 
If you click on requorements.txt file (as showen in the figure above). You will find the neseccarry intallation to run the STT transcription. So, we will install pyaudio and websocket-client. Go back to the terminal (if you close it open it and make sure you are in the folder we work on). run this line:

    $ pip install -r requirements.txt
    
## Update speech.cfg.example with APIKEY
This file give you an example of what shold you do. You can edit this file. Important thing is you have to delete [.example] or it will not work.
I typed my APIKEY and the region I have obtain it from cloud.ibm.com website.
<img width="934" alt="Screen Shot 2021-08-16 at 3 51 13 PM" src="https://user-images.githubusercontent.com/85841915/129566741-66eec451-99a2-4c2f-8762-a7e758386fc6.png">

## Usage
In order to run a live transcreption open the terminal and type:

        $ python transcribe.py -t 5
-t 5 means it is going to transcribe for 5 seconds. You can change the time to be 10,15,or 2000 seconds. However this plan is free so it has a limitastion that is 500 menutes per month.
<img width="681" alt="Screen Shot 2021-08-01 at 11 04 07 AM" src="https://user-images.githubusercontent.com/85841915/129568167-58775c72-1ad0-4292-866b-70870a254b4a.png">

## Issues
In my case, the installation run into an error and to solve it I applied these steps:
1. Ensure you are using Python version 3.4.0  at least.

        $ python3 --version
3. Download the brew package manager by following the instructions here: [https://brew.sh][https://brew.sh].
4. Run the following commands in a terminal window:

        $ brew install portaudio
        $ python3 -m pip install pyaudio
        $ python3 -m pip install numpy
[1]

Also, '$ python transcribe.py -t 5' command didn't allow me to run the file. So, I typed '$ python3 transcribe.py -t 5' and it worked.

## References
[1] optional exercise. (n.d.)[https://cs.gmu.edu/~marks/112/projects/PlaySong.pdf]. 

