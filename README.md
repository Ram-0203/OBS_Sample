This project is a cricket match broadcast overlay that displays live match data over a video stream. The overlay consists of two halves:

Video Only: The left side of the screen shows the match video.

Video with Overlay: The right side of the screen shows the video with an overlay that includes team details, match status, and other match-related information.

Features
Video Display: Displays video of the cricket match.

Match Info Overlay: Displays information such as team names, scores, match status, and other relevant match details.

Responsive Design: The overlay adjusts for smaller screen sizes.

File Structure
index.html: The HTML file that includes the layout, CSS, and video elements.

sample.mp4: The video file (place your video file here or replace it with a new one).

The overlay content is dynamically placed inside the HTML file using CSS for styling.

Prerequisites
Before running the broadcast overlay and streaming it with OBS Studio, you will need:

Node.js and npm: Install Node.js to run a local HTTP server.

OBS Studio: A free and open-source software for video recording and live streaming.

Steps to Set Up the HTTP Server Using Node.js
Install Node.js: If you don't have Node.js installed, you can download it from here.

Initialize the Project: Open your terminal or command prompt and navigate to the directory where your index.html and sample.mp4 files are located.

Run the following command to initialize a new Node.js project:

bash
Copy
Edit
npm init -y
Install http-server: Install the http-server package globally by running the following command:

bash
Copy
Edit
npm install --global http-server
Start the HTTP Server: Once http-server is installed, start the server by running:

bash
Copy
Edit
http-server
By default, the server will be accessible at http://localhost:8080. You can now open the index.html file in a browser by navigating to this URL.

Steps to Set Up OBS Studio to Stream the Overlay
Download OBS Studio: Download and install OBS Studio from here.

Open OBS Studio: After installing OBS Studio, open the application.

Create a New Scene:

Click the + button under the "Scenes" box to create a new scene. Name it something like "Cricket Broadcast Overlay."

Add a Video Source:

In the "Sources" box, click the + button and select "Media Source".

Name it "Match Video" or something similar.

In the properties window, click Browse and select the sample.mp4 video file (or a new video file you'd like to stream).

Ensure the "Loop" and "Restart playback when source becomes active" options are checked.

Click OK.

Add the Overlay:

Click the + button under the "Sources" box again, and select "Browser".

Name it "Match Overlay" or similar.

In the properties window, paste the URL of your local server (e.g., http://localhost:8080).

Set the width and height according to your desired streaming resolution (e.g., 1920x1080).

Click OK.

Position the Overlay:

Adjust the positioning of the overlay by resizing or dragging it to fit your stream layout.

Start Streaming:

Once everything is set up, you can click Start Streaming to begin broadcasting the match overlay along with the video.

Customization
You can customize the HTML overlay content by modifying the index.html file. For instance:

Change the team logos: Replace the team logo image URLs with your own logos.

Modify the team details: Update the team names and scores as per the ongoing match.

Adjust the match status: Update the status text, like "Match in Progress," "Team 1 Won," etc.

You can also update the sample.mp4 file to reflect the actual match video.

Troubleshooting
The video doesn't load: Ensure the path to your sample.mp4 file is correct.

The overlay doesn't appear: Verify that the http-server is running and that OBS is pointing to the correct URL.

OBS doesn't show the overlay: Make sure the "Browser" source in OBS is correctly linked to your local server and that the dimensions are set properly.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Now you're ready to stream your cricket match with an interactive overlay using OBS Studio! Enjoy your broadcast!
