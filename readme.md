# Angular projects with TensorFlow JS
- An exercise in TFJS and Angular

# todo
- [ ] deploy using gh-pages
- [ ] add acknowledgement to orginal author in app

# Notes
- TFJS use json as model (converted from h5)
- to convert the model from h5 to json (converted model attached):
    1. install the python tfjs lib
    2. make sure your `tensorflowjs_converter` is not `not found`
        - I'm on macOS, your solution may vary
        - mine wasn't at first, after installing tfjs, because of some log like:
        ```  
        WARNING: The script tensorboard is installed in '/Users/myuser/Library/Python/3.8/bin' which is not on PATH.
        ```
        - `echo $PATH` to show your current paths
        - `PATH='/Users/myuser/Library/Python/3.8/bin'` to set temporary path
    3. go to your model dir, and run the command:
    `$ tensorflowjs_converter --input_format=keras model.h5 ./`

    
# Dependencies
0. node/angular cli
1. install TFJS and jQeury for angular project
```
npm install @tensorflow/tfjs --save
npm install jquery --save
```
2. instal TFJS to convert model `.h5` to `.json`  
`pip install tensorflowjs`  
make sure not to run in VS Code (mine crashed, yours might differ)
3. Optionally install Bootstrap  
`npm install bootstrap --save`

# References
https://towardsdatascience.com/how-to-use-angular-to-deploy-tensorflow-web-apps-5675b5a042cc

https://github.com/jamescalam/meditations_ai
