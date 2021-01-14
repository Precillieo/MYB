# SCA Cloud School Assessment Process

1. Install Docker for Desktop, Install WSL 2 Backend
2. Create a Dockerfile with a base model, create an HTML file with the display content.
3. Build the Docker Image.
   ```
   docker build -t website-image:v1 .
   ```
4. To run the Dockerfile
   ```
   docker run -d -p 80:80 website-image:v1 .
   ```
5. To ascertain if it has been run and built
   ```
   docker ps -a
   ```
6. When opened in browser using ```locahost:80```, this get displayed

   ![view on browser](https://github.com/Precillieo/SCA-mp-C2-Assignments/blob/master/Cloud%20School.jpg?raw=true)

7. Make Some Changes by editing the HTML file
8. Get the former Docker Container removed
   ```
   docker rm -f container-id
   ```
9. Build the updated Docker image
   ```
   docker build -t website-image:updated .
   ```
10. Run the updated Docker Image
    ```
    docker run -d -p 800:80 website-image:updated .
    ```
11. When opened in browser using ```localhost:800```, the updated one get displayed

    ![view on browser](https://github.com/Precillieo/SCA-mp-C2-Assignments/blob/master/update.jpg?raw=true)
12. Login to Dockerhub from terminal
    ```
    docker login
    ```
13. Tag image again before pushing
    ```
    docker tag website-image:updated precillieo/websiteimage:updated
    ```
14. Push to Dockerhub
    ```
    docker push precillieo/website-image:updated
    ```
15. **Note**: ```precillieo``` is my username on Dockerhub, ```website-image:updated``` are the image name and the tag respectively.

** Click [here](https://hub.docker.com/r/precillieo/website-image) to view the docker hub repository and the two tags made.
