# Incident Report — Project 24

## Incident Details

- **Project:** Manual Chaos Test
- **Incident type:** Web service interruption
- **Environment:** Authorized test environment
- **Service:** Nginx
- **Date:** To be recorded during execution

## Objective
Evaluate how a web service behaves when it becomes unavailable and verify that it can be restored successfully.

## Test Procedure

| Stage | Action | Expected result |
|---|---|---|
| 1 | Check Nginx status | Service is active |
| 2 | Request test webpage | HTTP response succeeds |
| 3 | Stop Nginx | Service becomes inactive |
| 4 | Request test webpage | Request fails |
| 5 | Restart Nginx | Service becomes active |
| 6 | Request test webpage | HTTP response succeeds |

## Results

- Initial service status: Pending
- Failure simulation: Pending
- Recovery status: Pending
- Final HTTP verification: Pending

## Recovery Procedure

```bash
sudo systemctl start nginx
sudo systemctl status nginx
curl -I http://localhost
```

## Observations
To be completed after the authorized test.

## Conclusion
To be completed after successful execution and verification.