### Metabase Docker Setup with Auto-Restart

This repository contains the necessary files to run Metabase using Docker with auto-restart.

### Prerequisites

- Docker installed on your system.

### Getting Started

1. Install Docker on your machine if you haven't already. Refer to the official Docker documentation for installation instructions: [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)

2. Run Metabase using Docker with auto-restart:

```bash
docker run -d -p 3000:3000 --name metabase --restart unless-stopped metabase/metabase
```

Explanation:
- `-d`: Run the container in the background (detached mode).
- `-p 3000:3000`: Map port 3000 from the container to port 3000 on the host.
- `--name metabase`: Assign a custom name "metabase" to the container for easy management.
- `--restart unless-stopped`: This option will automatically restart the Metabase container unless it is explicitly stopped by the user or in case of system reboots.
- `metabase/metabase`: The Docker image for Metabase from Docker Hub.

3. Access Metabase through your web browser:

   ```
   http://localhost:3000
   ```

   Follow the on-screen instructions to set up your admin account and database connections.

4. To stop the Metabase container, run:

```bash
docker stop metabase
```

### Further Customizations

You can further customize the Metabase configuration by passing environment variables to the `docker run` command. Refer to the [Metabase Official Documentation](https://www.metabase.com/docs/latest/operations-guide/running-metabase-on-docker.html) for more information.

---

That's it! You now have an updated README file with the auto-restart option included in the Docker run command. This will ensure that Metabase automatically restarts unless explicitly stopped, providing better reliability and availability. Feel free to add more details or elaborate further based on your specific requirements.
