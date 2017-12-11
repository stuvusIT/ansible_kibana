# Kibana 6

This role sets up a running kibana instance and configures it.


## Requirements

None


## Role Variables

For variables please see the [kibana documentation](https://www.elastic.co/guide/en/kibana/current/settings.html)

### Mandatory variables
Some variables are only possible to configure together they are also listed below

| Name                                    |         Required         | Default | Description                                                                                                                                                            |    |
|:----------------------------------------|:------------------------:|:--------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---|
| `kibana_elasticsearch_url `             |    :heavy_check_mark:    |         | The URL of the Elasticsearch instance to use for all your queries                                                                                                      |    |
| `kibiana_elasticsearch_password`        | :heavy_multiplication_x: |         | If your Elasticsearch is protected with basic authentication, these settings provide the username and password. Required when `kibiana_elasticsearch_username` is set. |    |
| `kibiana_server_ssl_certificate`        | :heavy_multiplication_x: |         | Required if `kibiana_server_ssl_enabled` is set. SSL certificate for the Kibana server                                                                                 |    |
| `kibiana_server_ssl_key`                | :heavy_multiplication_x: |         | Required if `kibiana_server_ssl_enabled` is set. SSL key for the Kibana server                                                                                         |    |
| `kibiana_elasticsearch_ssl_certificate` | :heavy_multiplication_x: |         | These files validate that your Elasticsearch backend uses the same key files.                                                                                          |    |
| `kibiana_elasticsearch_ssl_key`         | :heavy_multiplication_x: |         | Required if `kibiana_elasticsearch_ssl_certificate` is set. These files validate that your Elasticsearch backend uses the same key files.                              |    |


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
    - hosts: kibana
      roles:
        - stuvusIT.kibana
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).


## Author Information

- [Fritz Otlinghaus (Scriptkidid)](https://github.com/scriptkiddi) _fritz.otlinghaus@stuvus.uni-stuttgart.de_
