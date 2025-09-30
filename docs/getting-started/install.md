# Installation


---

!!! tip

    If you don't have prior experience with Python, we recommend reading
    [Using Python's pip to Manage Your Projects' Dependencies], which is a
    really good introduction on the mechanics of Python package management and
    helps you troubleshoot if you run into errors.

  [Python package]: https://pypi.org/project/mkdocs-material/
  [virtual environment]: https://realpython.com/what-is-pip/#using-pip-in-a-python-virtual-environment
  [semantic versioning]: https://semver.org/
  [upgrade to the next major version]: upgrade.md
  [Markdown]: https://python-markdown.github.io/
  [Pygments]: https://pygments.org/
  [Python Markdown Extensions]: https://facelessuser.github.io/pymdown-extensions/
  [Using Python's pip to Manage Your Projects' Dependencies]: https://realpython.com/what-is-pip/

### with docker <small>recommended</small> { #with-docker data-toc-label="with docker" }

The official [Docker image] is a great way to get up and running in a few
minutes, as it comes with all dependencies pre-installed. Open up a terminal
and pull the image with:

=== "Latest"

    ```
    docker pull apache/ranger
    docker pull apache/ranger-db
    docker pull apache/ranger-solr
    docker pull apache/ranger-zk
    ```

=== "2.7"

    ```
    docker pull apache/ranger:2.7.0
    docker pull apache/ranger-db:2.7.0
    docker pull apache/ranger-solr:2.7.0
    docker pull apache/ranger-zk:2.7.0
    ```

???+ warning

    The Docker container is intended for local previewing purposes only and
    is not suitable for deployment. This is because the web server used by
    MkDocs for live previews is not designed for production use and may have
    security vulnerabilities.

    [Docker Image]: https://hub.docker.com/r/apache/ranger
