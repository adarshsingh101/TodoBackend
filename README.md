To-Do List App - Bakend

this is the bakend for my to-do list aplication. it uses Node.js, Express, and mongodB to handle all the data and stuff.

How make it runing

first you have to clone the project
git clone https://github.com/adarshsingh101/TodoBackend.git

then go into the folder
cd todo-backend

install all the things it needs
npm install

you need to make a .env file in the main folder. its very important. and add this stuff:

MONGO_URI=mongodb+srv://adarshfinalchannel_db_user:T6SMVr3B1LZylmYA@cluster0.3ldmqar.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
PORT=5000


then just run the server
node server.js

the server should start up on port 5000.

API Endpoints

GET /api/todos: gets all the tasks

POST /api/todos: makes a new task

PUT /api/todos/:id: updates a task

DELETE /api/todos/:id: deletes a task

Challenges i faced

at first the frontend couldnt talk to the bakend. i got this CORS error. had to install the cors package to fix it, was a bit tricky to figure out.

also had a problem where the MONGO_URI was undefined on Render. i didnt realize that the .env file is only for local and you have to add the variables directly on the render website. that took me a while to debug.

the delete function was crashing the server. turns out .remove() is old and i had to change it to .deleteOne(). mongoose updates are confusing sometimes.
