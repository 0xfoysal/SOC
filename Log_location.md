# Log File Locations

This section provides information on where to find log files for the project. Log files are useful for troubleshooting and monitoring application behavior.

## Common Log File Locations

### 1. Application Logs

- **Local Development Environment**: 
    - Logs are generally stored within the project directory (if configured in your application settings). You may find logs in the following locations:
      - `./logs/app.log`
      - `./logs/error.log`

- **Production Environment**:
    - Logs may be managed by the server or a third-party service (e.g., AWS CloudWatch, Loggly, etc.). Common log locations include:
      - `/var/log/app.log`
      - `/var/log/nginx/access.log`
      - `/var/log/nginx/error.log`

### 2. Web Server Logs

- **Apache**:
    - Access Logs: `/var/log/apache2/access.log`
    - Error Logs: `/var/log/apache2/error.log`
  
- **Nginx**:
    - Access Logs: `/var/log/nginx/access.log`
    - Error Logs: `/var/log/nginx/error.log`

### 3. Database Logs

- **MongoDB**:
    - Log File Location: `/var/log/mongodb/mongod.log`
  
- **MySQL**:
    - Error Log: `/var/log/mysql/error.log`

### 4. System Logs

- **System Logs**: 
    - On Linux-based systems, you can often find system-related logs in:
      - `/var/log/syslog`
      - `/var/log/messages`
      - `/var/log/auth.log`

### 5. Custom Application Logs

- If your application uses a custom logging solution, logs may be written to a specific directory defined by the `LOG_PATH` or a similar environment variable.

## Accessing Logs

- Use the following commands to access logs on Linux-based systems:
  - View logs with `cat` or `tail`:
    ```bash
    tail -f /var/log/nginx/access.log
    ```
  - For error logs:
    ```bash
    tail -f /var/log/nginx/error.log
    ```

## Log Rotation

- Log files should be rotated regularly to prevent them from becoming too large. Many servers use `logrotate` to manage log files. Ensure your system's log rotation settings are configured.
