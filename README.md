# Render_starter
#### Basic Render APP - to get it out there

You can test your changes locally by installing Docker and using the following command:
```
docker build -t fastai-v3 . && docker run --rm -it -p 5000:5000 fastai-v3
```

## [Pre-Setup]

#### 1) Upload the trained model file created with learner.export (for example export.pkl)

#####    1.1) Use <a href="https://www.wonderplugin.com/online-tools/google-drive-direct-link-generator/">this link generator</a>

#### 2) Customize the app for your model

#####    2.1) Edit the file <code>server.py</code> inside the app directory and update the <code>export_file_url</code> variable with the URL copied 

#####    2.2) In the same file, update the line <code> classes = ['black', 'grizzly', 'teddys'] </code> with the classes you expect from your model.
    
#### 3) <code> Commit </code> & <code> Push </code>



## [Deploying]


   1)  Create a new Web Service on Render and use the repo you created above. You will need to grant Render permission to access your repo in this step.

   2)  On the deployment screen, pick a name for your service and use Docker for the Environment. The URL will be created using this service name. The service name can be changed if necessary, but the URL initially created can’t be edited.

   3)  Click Save Web Service. That’s it! Your service will begin building and should be live in a few minutes at the URL displayed in your Render dashboard. You can follow its progress in the deploy logs.
   
   
## [Testing]


Your app’s URL will look like <code> https://service-name.onrender.com </code> 

You can also monitor the service logs as you test your app.

### [ local testing ]


To run the app server locally, run this command in your terminal:
<code> python app/server.py serve </code>

If you have Docker installed, you can test your app in the same environment as Render’s by running the following command at the root of your repo:
<code> docker build -t fastai-v3 . && docker run --rm -it -p 5000:5000 fastai-v3 </code>
