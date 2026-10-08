# Mission 6 Reflection

## 1. How does writing a docker-compose.yml file make a cloud engineer's job easier?
Docker Compose made the work easier because I only had to write the configuration
once and run a single command to start all of the containers. Instead of typing a
separate `docker run` command for the database and another for Nextcloud, I
described both in one file and deployed them together. Because the setup lives in
a file, it is also easier to repeat, share, and fix than a list of commands typed
by hand.

## 2. What happens if you make an indentation error in a YAML file?
I did not try this mistake myself, but I understand that YAML depends on spaces to
define its structure and does not allow Tabs for indentation. Using a Tab, or
misaligning a line, can cause Docker Compose to report a parsing or formatting
error, and the stack will not deploy until the file is fixed. This is why I had to
be careful with the spacing while writing the file in nano.

## 3. Why did we use environment variables like MYSQL_PASSWORD?
Environment variables keep configuration, such as the database name, user, and
password, outside the container image. This lets the same MariaDB and Nextcloud
images be reused while only the values change, and it keeps the credentials
consistent between the two containers. It is also better than hard-coding
passwords inside an image, which would be harder to change and less secure.

## 4. How did it feel to deploy Nextcloud in just a few minutes?
I was surprised and satisfied when the Nextcloud page loaded. Seeing the setup
screen showed me that I had successfully set up the containers and that the system
was working properly. It was rewarding to see a real cloud storage application
running after only a few commands.

## 5. How has my understanding of Cloud Computing evolved since Mission 1?
In Mission 1, I thought cloud computing was mainly about storing files and
accessing them online. Now I understand that it is much broader, because it
provides services, applications, storage, and computing resources through the
internet. Deploying a multi-tier application with Compose showed me how cloud
engineers build and manage these services using code.
