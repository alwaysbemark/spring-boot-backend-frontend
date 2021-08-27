# Spring Boot integrated frontend application
This application bundles two Gradle subprojects: `frontend` and `backend`. The frontend application uses the Gradle frontend
plugin to build the artifact in the `assembleFrontend` task which records its artifacts. The backend application then puts
the frontend resources in the `/resources/static/main` folder which means that Spring Boot picks those up to serve as a homepage
(e.g. when visiting localhost:8080 while it's running).  

  
This allows for monorepo'ing the backend and frontend applications which are written using two compeltely different tech stacks.