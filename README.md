
### Apache Pig and Hadoop Docker Setup

# Apache Pig and Hadoop Docker Environment

This repository contains a Docker Compose setup for Apache Pig integrated with Hadoop, providing a straightforward way to test and develop big data scripts with Pig on a local machine.

## Prerequisites

Before you begin, ensure you have Docker and Docker Compose installed on your machine. These are essential for creating and managing the containers defined in the `docker-compose.yml` file.

## Quick Start

Follow these steps to get your Docker environment up and running:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/pig-hadoop-docker.git
   cd pig-hadoop-docker
   ```

2. **Start the Docker containers:**

   ```bash
   docker-compose up -d
   ```

   This command will pull the required Docker images, create the necessary Docker volumes, and start the services defined in `docker-compose.yml`.

3. **Access the Pig CLI:**

   Use the following command to access the Pig command line interface:

   ```bash
   docker exec -it pig bash
   ```

   From here, you can run Pig scripts or perform interactive analysis.

4. **Interact with Hadoop:**

   The Hadoop NameNode and DataNode web interfaces are available at:

   - NameNode: [http://localhost:9870](http://localhost:9870)
   - DataNode: [http://localhost:9864](http://localhost:9864)

## Environment Configuration

- `hadoop.env`: Defines environment variables for Hadoop services.
- `data/`: Directory mounted into the Pig container. Place your Pig scripts and data files here.

## Stopping the Services

To stop and remove the containers, networks, and volumes associated with the environment, run:

```bash
docker-compose down -v
```

## Additional Notes

- The Docker images used are `bde2020/hadoop-namenode` and `bde2020/hadoop-datanode` for Hadoop, and `sequenceiq/pig` for Apache Pig.
- Modify `hadoop.env` and Docker volumes as needed to fit your specific requirements or to expand this setup.

## Contributing

Contributions are welcome! Feel free to submit pull requests or open issues to improve the Docker setup or documentation.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
