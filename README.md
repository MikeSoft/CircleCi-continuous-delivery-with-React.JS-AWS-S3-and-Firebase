
# Demo of continuous delivery with React , AWS S3 and Firebase Hosting

For a personal project i had to build a continuous delivery feature with AWS S3 for testing and Firebase Hosting for Production. 

Firebase hosting because it's easier to setting up the SSL, instead with AWS S3 you have to use Router 53 and it's more expensive. 

So i did search a lot without find a functional solution and i had to build one that i show you here. 

As you can read in the [config.yml](.circleci/config.yml) the actions depends of the branch. 
 - develop -> Just check the Build 
 - staging -> Deploy to [AWS S3](https://aws.amazon.com/es/s3/)
 - master -> Deploy to [Firebase Hosting](https://firebase.google.com/docs/hosting?hl=es)
