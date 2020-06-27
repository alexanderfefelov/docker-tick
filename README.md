# docker-tick

Run

    docker-compose up --build

and point your browser to <http://localhost:8888>.

## Log collection

- Linux and Rsyslog

    `/etc/rsyslog.d/10-rsyslog.conf`:

    ```
    $ActionQueueFileName queue
    $ActionQueueMaxDiskSpace 500M
    $ActionQueueSaveOnShutdown on
    $ActionQueueType LinkedList
    $ActionResumeRetryCount -1

    $WorkDirectory /var/spool/rsyslog

    @(o)localhost:5514;RSYSLOG_SyslogProtocol23Format
    ```
