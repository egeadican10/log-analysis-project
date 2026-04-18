
# Log Analysis Project

## Description
This project simulates a distributed brute force attack and analyzes logs to detect suspicious patterns.

## Logs Used
- Access logs
- Authentication logs
- Error logs

## Key Findings
- Multiple IP login attempts detected
- Successful login after repeated failures
- Privilege escalation attempt observed

## Skills
- Log Analysis
- Attack Detection
- Incident Response


#log scenario
2026-04-18 09:59:58 [INFO] GET /home (ip: 185.23.11.9)
2026-04-18 10:00:00 [INFO] GET /login (ip: 201.44.12.8)
2026-04-18 10:00:01 [INFO] GET /admin (ip: 91.21.33.5)
2026-04-18 10:00:02 [INFO] GET /admin/login (ip: 77.88.12.9)

2026-04-18 10:00:10 [WARN] Login failed (user: admin, ip: 185.23.11.9)
2026-04-18 10:00:11 [WARN] Login failed (user: admin, ip: 201.44.12.8)
2026-04-18 10:00:12 [WARN] Login failed (user: admin, ip: 91.21.33.5)
2026-04-18 10:00:13 [WARN] Login failed (user: admin, ip: 77.88.12.9)

2026-04-18 10:00:14 [WARN] Login failed (user: admin, ip: 185.23.11.9)
2026-04-18 10:00:15 [WARN] Login failed (user: admin, ip: 201.44.12.8)

2026-04-18 10:00:20 [INFO] Login success (user: admin, ip: 91.21.33.5)

2026-04-18 10:00:25 [INFO] GET /admin/dashboard (user: admin, ip: 91.21.33.5)
2026-04-18 10:00:30 [INFO] GET /admin/settings (user: admin, ip: 91.21.33.5)

2026-04-18 10:00:40 [ERROR] Permission denied /root (user: admin, ip: 91.21.33.5)
2026-04-18 10:00:45 [WARN] Suspicious privilege escalation attempt (user: admin, ip: 91.21.33.5)



#analysis
The logs indicate a distributed brute force attack targeting the admin account.

Multiple IP addresses attempted authentication, suggesting coordinated attack behavior.

Successful login after multiple failures indicates account compromise.

Subsequent privilege escalation attempts were detected via unauthorized root access attempts.
