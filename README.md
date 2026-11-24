# Project 24 — Manual Chaos Test

## Objective
Simulate a controlled application service failure, observe the impact, restore the service, and document the recovery process.

## Tools Used
- Linux
- Bash
- systemd
- Nginx
- Git and GitHub

## Test Scenario
1. Set up a test web service using Nginx on an authorized Linux test machine.
2. Verify that the service is running and the test webpage responds.
3. Simulate a service failure by stopping Nginx.
4. Verify that the webpage is no longer responding.
5. Restart Nginx and verify that the webpage responds again.
6. Record the incident, recovery steps, and observations.

## Safety
- Perform the test only on a personal or explicitly approved test machine.
- Never stop services on shared or production infrastructure without written authorization.
- Do not include credentials, private keys, or sensitive server details in this repository.

## Evidence
- Screenshot of the service running before the test.
- Screenshot showing the controlled failure.
- Screenshot showing successful recovery.
- Incident report documenting the test.

## Status
Documentation prepared. Test execution and evidence pending an authorized test environment.