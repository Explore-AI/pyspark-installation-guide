# Installing PySpark using Docker
This readme will help to install and run PySpark using Docker containers.
A read made Dockerfile is provided to make the process easier.
This guide assumes you already have Docker installed on your machine.

## Before your create your Docker Image
The first step is to create a Docker Image using the given Dockerfile.
Before creating your image, the following is required:
- Make sure Docker is running
- Read the Dockfile and ensure it's installing the right versions of Spark, Hadoop, and Java

### Creating the Image
- Open a new terminal and navigate to the folder where your Dockerfile is
- Create or pick a local folder to use for your code and data. We'll call it 'src' in this example. Run `touch src`
- Run `docker build -t pyspark_docker .`

### Create a Container from your new Image
- Get the full path to your 'src' folder as you'll need it for mounting is as a volume
- Run `docker run -it -v C:/path/to/src:/src -p 8888:8888 pyspark_docker`
- Please note that your path to the 'src' folder will be different from 'C:/path/to/src'
- The `-v` flag mounts your local 'src' folder onto the containers 'src' directory
- The `-p` flag forwards your machine's port 8888 to the container's port 8888.
- 8888 is the port used by Jupyter Notebooks

### Access the Docker Container
- You'll see something similar to `root@a123c45b677d:/#` in your terminal once your container is up and running
- You can now launch jupyter from within the container
- Run `jupyter notebook --ip 0.0.0.0 --no-browser --allow-root`
- Click the URL that starts with http://127.0.0.1:8888/tree?token... to launch jupyter in your browser
- You're now ready to use PySpark within a Docker container
- Please note that any files that exist inside of your 'src' folder will show up under the 'src' folder inside of your container.



