# local deploy
for testing locally, add a ".env" file.
inside the file, add 
```
DATABASE_URL={your_mongo_db_url}
```
you may set up mongodb by just downloading mongodb and running the service
for example, your url may be something like `mongodb://127.0.0.1:27017/subscribers`
the subscribers DB doesnt have to exist as it will be created automatically.
using `mongodb://localhost` didnt work for me, im not sure why

then, run `npm i --dev`

finally, run `npm run dev`
for the dev script, nodemon is used so that once the files update, the server will be immediately reloaded.

# prod deploy
## vercel hosting, netlify hosting, etc etc
for production deployment, make an environment variable called `DATABASE_URL` and add your mongodb url as the data, for example `DATABASE_URL=mongodb://mongodb.com:27017/subscribers` on whatever platform ur hosting this on.
then, run `npm i` and then `npm run start`

## server hosting
if you are hosting this on a server, follow the steps on local deploy.
but for the last command, instead of `npm run dev`, run `npm run start`
