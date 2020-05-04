# Render_starter
Basic Render APP - to get it out there

You can test your changes locally by installing Docker and using the following command:
```
docker build -t fastai-v3 . && docker run --rm -it -p 5000:5000 fastai-v3
```


1) Upload the trained model file created with learner.export (for example export.pkl)

    1.1) Use <a href="https://www.wonderplugin.com/online-tools/google-drive-direct-link-generator/">this link generator</a>

2) Customize the app for your model

    2.1) Edit the file <code>server.py</code> inside the app directory and update the <code>export_file_url</code> variable with the URL copied 

    2.2) In the same file, update the line <code> classes = ['black', 'grizzly', 'teddys'] </code> with the classes you expect from your model.
    
3) <code> Commit </code> & <code> Push </code>
