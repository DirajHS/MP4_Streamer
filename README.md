MP4_Streamer
============

H264 Video Streaming using UNIX Networking 

			
		     				 Welcome to our project on Mp4-Streaming

	This project MP4-streaming is mainly concerned about brodcasting MP4 videos over the net, mobile phones. In our project we replicate the above process by using a client and a server machines. The client sends it's request for viewing MP4.The server in turn streams the MP4 videos to the client, if the connection is established. The important  thing here is that no MP4s are copied as  whole while sending from server to client. The MP4 videos are stored in MPEG Transport format which is standard for transmission and storage of audio, video and Program and System Information Protocol.Transport stream specifies a container format encapsulating packetized elementary streams, with error correction and stream synchronization features for maintaining transmission integrity when the signal is degraded.

	Transport streams differ from the similarly named program streams in several important ways: program streams are designed for reasonably reliable media, such as discs (like DVDs), while transport streams are designed for less reliable transmission, namely terrestrial or satellite broadcast. Further, a transport stream may carry multiple programs.

	The Network project  is done basically to work on the UNIX Platform by using the client server technology. The source code is written in C++ Language.

The project will work on the standalone systems, LAN connected systems and the remote machine connected to the internet. However the user will not be able to listen the videos of his/her choice. Only the videos streamed by the streamer will be viewed (like TV programs are streamed).


    Basic Requirements:
	
	Your computer is running on Linux with Multimedia 
	Utilities (vlc or ffplay installed).
	Your computer is at least Pentium class, and has 64MB of memory 
	Your computer has a working network configuration 
	You can can type the words 'make' and './configure 
	

   
    Execution steps:
 
First execute both the server and streamer on the host machine. After this goto any client system(VLC or MX Player etc.) on the network and execute client operation. The following describes steps involved in both host and client part execution.

HOST PART 

    server part:

       1)Open a new terminal by pressing ctrl+alt+f1,enter the user name and password.

       2)Now goto the dir in which all the project files are stored by using cd command.

       3)Compile the server file mp4server.cpp by giving "g++ mp3server.cpp -o se -lpthread"
	 on the command prompt. (Ignore the double quotes)	

       4)Execute the compiled file se by giving "./se" at the command prompt and shift to other terminal.	

    mp4-streamer part:
	
	1)Once the server is running shift to other terminal by pressing
	 ctrl+alt+f2,goto to the dir in which all the project files are stored by using 
          cd command.
	
	2)Compile the mp4streamer.cpp file by giving "g++ mp4streamer.cpp playlist -o st"
	
	3)Execute the compiled file st by  giving 

	    "./st <localhost address> 9001 /h pl.txt" -------mp4streamer will start running.

    	
	   
CLIENT PART
 
     client :
	1)Open a new terminal and type the IP address of server with port number and mount to play the video. You can use any vidoe player like VLC or MX player.

	Ex: vlc http://192.168.0.100:9000 /h


NOTE: Please see the screenshots in case any of the above is not clear. 