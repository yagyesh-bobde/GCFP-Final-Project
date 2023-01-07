# PENAUTO-React Site 
This is the final project created for the completion of Google Cloud Facilitator's Program. 
PENAUTO is a react site which is mobile responsive. It also has form validation. I have deployed it using app engine on Google cloud platform.

# What is GCP? 
GCP stands for Google Cloud Platform, it is a suite of cloud computing services that runs on the same infrastructure that Google uses internally for its end-user products, such as Google Search, Gmail, Google Drive and YouTube.

# What is App Engine? 
App Engine is <b>a fully managed, serverless platform for developing and hosting web applications at scale</b>.

<br>
### Why app engine?
GAE is fully managed, so users can write code without considering IT operations and back-end infrastructure. The built-in APIs enable users to build different types of applications. Access to application logs also facilitates debugging and monitoring in production.
<br>

## How to deploy react app using app engine? 

1. Open a GCP. 
2. Create and initialize an app engine.
   1. Select a region
   2. <b>Language</b>-Nodejs
   3. <b>Environment</b>-Standard
   4. Click the "I'll do this later" link and your app should be created.
3. Activate Cloud shell
4. Clone your project inside our cloud working directory
   - Use the git clone <project-repository-url> to clone your project in the cloud environment.
5. cd into your <project-directory>  
6. Install all dependencies
   ```
   $ npm install
   ```
7. Run the build command
 ```
   $ npm run build
   ```
8. Now remove every other files and folders in the directory except the build folder using the <b>rm and rm -r</b> commands respectively.
9. Create an app.yaml file and paste the following script inside it. ( You can edit the app.yaml file using the vim editor or the cloud editor environment)
   ```
      runtime: nodejs14
      handlers: 
      - url: /(.*\..+)$
        static_files: build/\1
        upload: build/(.*\..+)4
      - url; /.*
        static_files: build/index.html
        upload: build/index.html 
   ```
Before we move ahead just make sure that your project directory has is the build folder and app.yaml file. 

10. Run the following command
   ```
      $ gcloud app deploy
   ```
   press y (yes) for any such prompts.
<b>IF YOU FACE ANY ERRORS</b><U>Make sure that you have enabled the Cloud Build API before running the deploy command or enable and run it again after.</U>

Voila! You have deployed you app successfully 🎉. You can get the url where the app is deployed by running the command: 
   ```
      $ gcloud app browse
   ```    
You can check your deployed applicaiton on the link that is shown.


## How to run the project locally?
1. Fork the repository/download the files and extract the files in your local machine
2. Open a terminal in the project repository
3. Initialize & install the project and necessary packages by running: 
   ```
    $ npm init 
   ```
4. The final step is to run the following command: 
   ```
    $ npm run start
   ```

### Project Gallery

#### Desktop View

<div style="display:flex; flex-direction:column; justify-content:center;align-items:center; gap: 15px;">
<img src="/1.png" width="640" height="375"  alt="" >
<img src="/2.png" width="640" height="375"  alt="" >
</div>

#### MOBILE View
<div style="display:flex; justify-content: space-evenly; gap: 5px; flex-wrap:wrap;">
<img src="/3.png" height="450" width="350"  alt="" >
<img src="/4.png" height="450" width="350"  alt="" >
<img src="/5.png" height="450" width="350"  alt="" >
</div>

## External Packages 
- Bootstrap
- FontAwesome
- Concurrently ( developer dependency )

## Tech Stack Used: 
1. React js
2. HTML
3. CSS 
4. Javascript / JSX
5. Bootstrap
6. Google Cloud Platform

## More Links: 
1. Backend Link : <a href="https://github.com/yagyesh-bobde/Vocally-Assignment-Backend" target="_blank" >https://github.com/yagyesh-bobde/Vocally-Assignment-Backend</a>


### Created By<br>
Yagyesh Bobde 
Connect : 
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yagyesh-bobde-177523220/) [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/yagyesh-bobde)

