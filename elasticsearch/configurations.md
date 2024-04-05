# Elasticsearch configurations

## Allow insecure connections

To allow insecure connections, you need to disable the SSL verification in the Elasticsearch configuration file. This is useful when you are using CURL to interact with the Elasticsearch database (error 52)

1. Open the `elasticsearch.yml` file

    ```bash
    vi /etc/elasticsearch/elasticsearch.yml
    ```

2. Add or edit the following line in the file

    ```bash
    xpack.security.http.ssl.enabled: false
    ```

3. Save the file and restart the Elasticsearch service

    ```bash
    # With systemd
    sudo systemctl restart elasticsearch

    # With Docker compose
    docker compose restart elasticsearch
    ```
