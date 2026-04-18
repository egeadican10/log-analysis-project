




-2026-04-18 09:59:58 [INFO] GET /home (ip: 185.23.11.9)
-2026-04-18 10:00:00 [INFO] GET /login (ip: 201.44.12.8)
-2026-04-18 10:00:01 [INFO] GET /admin (ip: 91.21.33.5)
-2026-04-18 10:00:02 [INFO] GET /admin/login (ip: 77.88.12.9)

-2026-04-18 10:00:10 [WARN] Login failed (user: admin, ip: 185.23.11.9)
-2026-04-18 10:00:11 [WARN] Login failed (user: admin, ip: 201.44.12.8)
-2026-04-18 10:00:12 [WARN] Login failed (user: admin, ip: 91.21.33.5)
-2026-04-18 10:00:13 [WARN] Login failed (user: admin, ip: 77.88.12.9)

-2026-04-18 10:00:14 [WARN] Login failed (user: admin, ip: 185.23.11.9)
-2026-04-18 10:00:15 [WARN] Login failed (user: admin, ip: 201.44.12.8)

-2026-04-18 10:00:20 [INFO] Login success (user: admin, ip: 91.21.33.5)

-2026-04-18 10:00:25 [INFO] GET /admin/dashboard (user: admin, ip: 91.21.33.5)
-2026-04-18 10:00:30 [INFO] GET /admin/settings (user: admin, ip: 91.21.33.5)

-2026-04-18 10:00:40 [ERROR] Permission denied /root (user: admin, ip: 91.21.33.5)

-2026-04-18 10:00:45 [WARN] Suspicious privilege escalation attempt (user: admin, ip: 91.21.33.5)
-
-
-
-



#analysis
The logs indicate a distributed brute force attack targeting the admin account.

Multiple IP addresses attempted authentication, suggesting coordinated attack behavior.

Successful login after multiple failures indicates account compromise.

Subsequent privilege escalation attempts were detected via unauthorized root access attempts.



Incident Type: Distributed Brute Force Attack

Target: Admin Account

Indicators:
- Multiple IP login attempts
- Repeated authentication failures
- Successful login after brute force attempts

Attack Chain:
1. Reconnaissance via access logs
2. Distributed brute force attempts
3. Successful authentication (compromise)
4. Privilege escalation attempt

Risk Level: High

Recommendations:
- Implement account lockout policies
- Enable multi-factor authentication
- Monitor login attempts across multiple IPs
- Block suspicious IP ranges
