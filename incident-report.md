# Incident Report — Project 24

## Incident Details
- **Project:** Manual Chaos Test
- **Incident type:** Web service interruption
- **Environment:** Local WSL Ubuntu test environment
- **Service:** Nginx
- **Date:** 26 November 2026

## Objective
Evaluate how a web service behaves when it becomes unavailable and verify that it can be restored successfully.

## Test Results

| Stage | Action | Actual Result |
|---|---|---|
| 1 | Check Nginx status | Active (running) |
| 2 | Request test webpage | HTTP 200 OK |
| 3 | Stop Nginx | Service became inactive |
| 4 | Request test webpage | Connection failed as expected |
| 5 | Restart Nginx | Service became active |
| 6 | Request test webpage | HTTP 200 OK |

## Results
- Initial service status: Successful
- Initial HTTP verification: Successful
- Failure simulation: Successful
- Service recovery: Successful
- Final HTTP verification: Successful

## Recovery Procedure

```bash
sudo systemctl start nginx
sudo systemctl status nginx
curl -I http://localhost
```

## Observations
The Nginx service responded normally before the test. After stopping the service, HTTP requests failed as expected. Restarting Nginx restored the service, and the final HTTP request succeeded.

## Conclusion
The local chaos test was successfully completed. The controlled service interruption and recovery demonstrated that Nginx could be restored after an unexpected service outage.

**Note:** This was a local WSL simulation. No AWS, company-managed, shared, or production infrastructure was affected.