# Container Observability

## Application Logs 

Log line showing the 404 error:

```
172.17.0.1 - - [06/Oct/2026:06:21:08 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

## Why Application Logs Are Vital for Troubleshooting
Application logs record every request and error that happens in the
container, including what was requested, when it happened, and what the
result was. This helps engineers find the exact cause of a problem quickly,
like the 404 above, which shows that someone tried to visit a page that does
not exist.

## Real-Time Container Metrics

Output of `docker stats`:

```
CONTAINER ID   NAME             CPU %     MEM USAGE / LIMIT     MEM %     NET I/O           BLOCK I/O     PIDS
c45c241f9ee5   client-website   0.00%     2.734MiB / 1.859GiB   0.14%     3.85kB / 5.37kB   0B / 12.3kB   2
```

- **Memory Usage:** 2.734MiB
- **CPU Percentage:** 0.00%

The `client-website` container was using very little memory and almost no CPU
at the time of the screenshot, which shows that it was idle and had plenty of
room to handle more traffic.
