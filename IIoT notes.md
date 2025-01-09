**IIoT notes**

![alt text](<Screenshot%202024-11-10%20164531.png>)

*First install node Red program* 

- https://nodejs.org/dist/v22.11.0/node-v22.11.0-x64.msi

On PowerShell execute: 

`Set-ExecutionPolicy Unrestricted `
This command enable npm scripts on Windows

Then install node red using command npm 
 
 ` npm install -g --unsafe-perm node-red `

On then you have node red server in your machine

run terminal powershell using the following command

`node-red`

The server are running in:  Server now running at http://127.0.0.1:1880/

If you Want to deploy 2 or more project in node-red, you need to edit this config.

`C:\Users\userx\.node-red\settings.js`

Edit this file and enable this parameter: 

```
   editorTheme: {
       projects: {
           enabled: true
       }
   },

```
You'll be able to deploy two or more project.


**Database**

How to connect with database?

Install MySql server
- https://dev.mysql.com/downloads/windows/installer/8.0.html

Custom Install 
- https://www.youtube.com/watch?v=u96rVINbAUI





