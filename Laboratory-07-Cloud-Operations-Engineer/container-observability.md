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
