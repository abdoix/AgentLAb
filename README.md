## Docker Option

1. Build the Docker image

```docker build -t agentlab .```

2. Run the container (Replace API_KEY with your actual API key)

```docker run -it -v $(pwd)/research_dir:/app/research_dir agentlab --research-topic "your research topic" --llm-backend "deepseek-chat" --api-key "API_KEY" ```

Note: The research_dir will be mounted from your local machine, allowing you to access the generated files outside the container

## **Checking Docker Logs**

1. **List Running Containers**: To see which containers are currently running:

   ```docker ps```
   This will show the `CONTAINER ID`, `IMAGE`, and the status of each container. Look for the container associated with your research task.
2. **Check Logs for a Specific Container**: To check the logs of a specific container, use the following command:

   ```docker logs <CONTAINER_ID>```

   Replace `<CONTAINER_ID>` with the actual container ID from the `docker ps` output.
3. **Follow Logs in Real-Time**: If you want to see logs in real-time (live updates), you can add the `-f` flag:

   ```docker logs -f <CONTAINER_ID>```

   This will display the logs as they are generated.
