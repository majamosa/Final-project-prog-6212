# Final-project-prog-6212
RaceDay – Docker Running Instructions

1. Start Docker Desktop

Open Docker Desktop on your computer.

Wait until Docker Engine is running.

Make sure Docker Desktop is ready before continuing.

2. Open the RaceDay Project

Open PowerShell.

Navigate to the RaceDay_Webs folder:

cd "C:\Users\User\OneDrive\Desktop\FINAL PROG PART2\RaceDay_Webs"

Note: Change the folder path if the project is saved somewhere else.
## 3. Build the Docker Image

Run the following command:

```powershell
docker build -t raceday-web --load .
```

Wait until the build finishes successfully.
## 4. Start the RaceDay API
Open the RaceDay solution in Visual Studio and start the `RaceDay_Api` project.

The API must be running because the website communicates with it.
## 5. Run the Docker Container

In PowerShell, enter:

```powershell
docker run -d --name raceday-web -p 8080:8080 --env-file .env raceday-web
```
## 6. Access the Website

Open Google Chrome or another browser and enter:

http://localhost:8080

The RaceDay website should now open.
