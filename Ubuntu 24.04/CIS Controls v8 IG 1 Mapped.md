# CIS Ubuntu 24.04 LTS Benchmark - Checklist

## 1.1 - Filesystem Configuration

| CIS ID    | Recommendation                                       | YES | NO  | Compensating | Notes |
| --------- | ---------------------------------------------------- | --- | --- | ------------ | ----- |
| 1.1.1.9   | Ensure usb-storage kernel module is not available    |     |     |              |       |
| 1.1.2.1.3 | Ensure nosuid option set on /tmp partition           |     |     |              |       |
| 1.1.2.1.4 | Ensure noexec option set on /tmp partition           |     |     |              |       |
| 1.1.2.2.2 | Ensure nodev option set on /dev/shm partition        |     |     |              |       |
| 1.1.2.2.3 | Ensure nosuid option set on /dev/shm partition       |     |     |              |       |
| 1.1.2.2.4 | Ensure noexec option set on /dev/shm partition       |     |     |              |       |
| 1.1.2.3.1 | Ensure separate partition exists for /home           |     |     |              |       |
| 1.1.2.3.2 | Ensure nodev option set on /home partition           |     |     |              |       |
| 1.1.2.3.3 | Ensure nosuid option set on /home partition          |     |     |              |       |
| 1.1.2.4.1 | Ensure separate partition exists for /var            |     |     |              |       |
| 1.1.2.4.2 | Ensure nodev option set on /var partition            |     |     |              |       |
| 1.1.2.4.3 | Ensure nosuid option set on /var partition           |     |     |              |       |
| 1.1.2.5.1 | Ensure separate partition exists for /var/tmp        |     |     |              |       |
| 1.1.2.5.2 | Ensure nodev option set on /var/tmp partition        |     |     |              |       |
| 1.1.2.5.3 | Ensure nosuid option set on /var/tmp partition       |     |     |              |       |
| 1.1.2.5.4 | Ensure noexec option set on /var/tmp partition       |     |     |              |       |
| 1.1.2.6.1 | Ensure separate partition exists for /var/log        |     |     |              |       |
| 1.1.2.6.2 | Ensure nodev option set on /var/log partition        |     |     |              |       |
| 1.1.2.6.3 | Ensure nosuid option set on /var/log partition       |     |     |              |       |
| 1.1.2.6.4 | Ensure noexec option set on /var/log partition       |     |     |              |       |
| 1.1.2.7.1 | Ensure separate partition exists for /var/log/audit  |     |     |              |       |
| 1.1.2.7.2 | Ensure nodev option set on /var/log/audit partition  |     |     |              |       |
| 1.1.2.7.3 | Ensure nosuid option set on /var/log/audit partition |     |     |              |       |
| 1.1.2.7.4 | Ensure noexec option set on /var/log/audit partition |     |     |              |       |

## 1.2 - Software Updates & Package Management

| CIS ID  | Recommendation                                                          | YES | NO  | Compensating | Notes |
| ------- | ----------------------------------------------------------------------- | --- | --- | ------------ | ----- |
| 1.2.1.1 | Ensure GPG keys are configured                                          |     |     |              |       |
| 1.2.1.2 | Ensure package manager repositories are configured                      |     |     |              |       |
| 1.2.2.1 | Ensure updates, patches, and additional security software are installed |     |     |              |       |

## 1.3 - Mandatory Access Control

| CIS ID  | Recommendation                                               | YES | NO  | Compensating | Notes |
| ------- | ------------------------------------------------------------ | --- | --- | ------------ | ----- |
| 1.3.1.1 | Ensure AppArmor is installed                                 |     |     |              |       |
| 1.3.1.2 | Ensure AppArmor is enabled in the bootloader configuration   |     |     |              |       |
| 1.3.1.3 | Ensure all AppArmor Profiles are in enforce or complain mode |     |     |              |       |
| 1.3.1.4 | Ensure all AppArmor Profiles are enforcing                   |     |     |              |       |

## 1.4 - Bootloader

| CIS ID | Recommendation                                   | YES | NO  | Compensating | Notes |
| ------ | ------------------------------------------------ | --- | --- | ------------ | ----- |
| 1.4.1  | Ensure bootloader password is set                |     |     |              |       |
| 1.4.2  | Ensure access to bootloader config is configured |     |     |              |       |

## 1.6 - Warning Banners & GDM

| CIS ID | Recommendation                                               | YES | NO  | Compensating | Notes |
| ------ | ------------------------------------------------------------ | --- | --- | ------------ | ----- |
| 1.6.4  | Ensure access to /etc/motd is configured                     |     |     |              |       |
| 1.6.5  | Ensure access to /etc/issue is configured                    |     |     |              |       |
| 1.6.6  | Ensure access to /etc/issue.net is configured                |     |     |              |       |
| 1.7.4  | Ensure GDM screen locks when the user is idle                |     |     |              |       |
| 1.7.5  | Ensure GDM screen locks cannot be overridden                 |     |     |              |       |
| 1.7.6  | Ensure GDM automatic mounting of removable media is disabled |     |     |              |       |
| 1.7.8  | Ensure GDM autorun-never is enabled                          |     |     |              |       |
| 1.7.9  | Ensure GDM autorun-never is not overridden                   |     |     |              |       |

## 2.x - Services & Cron

| CIS ID  | Recommendation                                         | YES | NO  | Compensating | Notes |
| ------- | ------------------------------------------------------ | --- | --- | ------------ | ----- |
| 2.1.1   | Ensure autofs services are not in use                  |     |     |              |       |
| 2.4.1.2 | Ensure permissions on /etc/crontab are configured      |     |     |              |       |
| 2.4.1.3 | Ensure permissions on /etc/cron.hourly are configured  |     |     |              |       |
| 2.4.1.4 | Ensure permissions on /etc/cron.daily are configured   |     |     |              |       |
| 2.4.1.5 | Ensure permissions on /etc/cron.weekly are configured  |     |     |              |       |
| 2.4.1.6 | Ensure permissions on /etc/cron.monthly are configured |     |     |              |       |
| 2.4.1.7 | Ensure permissions on /etc/cron.d are configured       |     |     |              |       |
| 2.4.1.8 | Ensure crontab is restricted to authorized users       |     |     |              |       |
| 2.4.2.1 | Ensure at is restricted to authorized users            |     |     |              |       |

## 4.x - Firewall Configuration

| CIS ID  | Recommendation                                                       | YES | NO  | Compensating | Notes |
| ------- | -------------------------------------------------------------------- | --- | --- | ------------ | ----- |
| 4.1.1   | Ensure a single firewall configuration utility is in use             |     |     |              |       |
| 4.2.1   | Ensure ufw is installed                                              |     |     |              |       |
| 4.2.2   | Ensure iptables-persistent is not installed with ufw                 |     |     |              |       |
| 4.2.3   | Ensure ufw service is enabled                                        |     |     |              |       |
| 4.2.4   | Ensure ufw loopback traffic is configured                            |     |     |              |       |
| 4.2.5   | Ensure ufw outbound connections are configured                       |     |     |              |       |
| 4.2.6   | Ensure ufw firewall rules exist for all open ports                   |     |     |              |       |
| 4.2.7   | Ensure ufw default deny firewall policy                              |     |     |              |       |
| 4.3.1   | Ensure nftables is installed                                         |     |     |              |       |
| 4.3.2   | Ensure ufw is uninstalled or disabled with nftables                  |     |     |              |       |
| 4.3.3   | Ensure iptables are flushed with nftables                            |     |     |              |       |
| 4.3.4   | Ensure a nftables table exists                                       |     |     |              |       |
| 4.3.5   | Ensure nftables base chains exist                                    |     |     |              |       |
| 4.3.6   | Ensure nftables loopback traffic is configured                       |     |     |              |       |
| 4.3.7   | Ensure nftables outbound and established connections are configured  |     |     |              |       |
| 4.3.8   | Ensure nftables default deny firewall policy                         |     |     |              |       |
| 4.3.9   | Ensure nftables service is enabled                                   |     |     |              |       |
| 4.3.10  | Ensure nftables rules are permanent                                  |     |     |              |       |
| 4.4.1.1 | Ensure iptables packages are installed                               |     |     |              |       |
| 4.4.1.2 | Ensure nftables is not in use with iptables                          |     |     |              |       |
| 4.4.1.3 | Ensure ufw is not in use with iptables                               |     |     |              |       |
| 4.4.2.1 | Ensure iptables default deny firewall policy                         |     |     |              |       |
| 4.4.2.2 | Ensure iptables loopback traffic is configured                       |     |     |              |       |
| 4.4.2.3 | Ensure iptables outbound and established connections are configured  |     |     |              |       |
| 4.4.2.4 | Ensure iptables firewall rules exist for all open ports              |     |     |              |       |
| 4.4.3.1 | Ensure ip6tables default deny firewall policy                        |     |     |              |       |
| 4.4.3.2 | Ensure ip6tables loopback traffic is configured                      |     |     |              |       |
| 4.4.3.3 | Ensure ip6tables outbound and established connections are configured |     |     |              |       |
| 4.4.3.4 | Ensure ip6tables firewall rules exist for all open ports             |     |     |              |       |


## 5.x - Access, Authentication and Authorization

| CIS ID    | Recommendation                                                             | YES | NO  | Compensating | Notes |
| --------- | -------------------------------------------------------------------------- | --- | --- | ------------ | ----- |
| 5.1.1     | Ensure permissions on /etc/ssh/sshd_config are configured                  |     |     |              |       |
| 5.1.2     | Ensure permissions on SSH private host key files are configured            |     |     |              |       |
| 5.1.3     | Ensure permissions on SSH public host key files are configured             |     |     |              |       |
| 5.1.4     | Ensure sshd access is configured                                           |     |     |              |       |
| 5.1.9     | Ensure sshd GSSAPIAuthentication is disabled                               |     |     |              |       |
| 5.1.11    | Ensure sshd IgnoreRhosts is enabled                                        |     |     |              |       |
| 5.1.14    | Ensure sshd LogLevel is configured                                         |     |     |              |       |
| 5.1.19    | Ensure sshd PermitEmptyPasswords is disabled                               |     |     |              |       |
| 5.1.20    | Ensure sshd PermitRootLogin is disabled                                    |     |     |              |       |
| 5.1.22    | Ensure sshd UsePAM is enabled                                              |     |     |              |       |
| 5.2.1     | Ensure sudo is installed                                                   |     |     |              |       |
| 5.2.2     | Ensure sudo commands use pty                                               |     |     |              |       |
| 5.2.4     | Ensure users must provide password for privilege escalation                |     |     |              |       |
| 5.2.5     | Ensure re-authentication for privilege escalation is not disabled globally |     |     |              |       |
| 5.2.6     | Ensure sudo authentication timeout is configured correctly                 |     |     |              |       |
| 5.2.7     | Ensure access to the su command is restricted                              |     |     |              |       |
| 5.3.2.1   | Ensure `pam_unix` module is enabled                                        |     |     |              |       |
| 5.3.2.2   | Ensure `pam_faillock` module is enabled                                    |     |     |              |       |
| 5.3.2.3   | Ensure `pam_pwquality` module is enabled                                   |     |     |              |       |
| 5.3.2.4   | Ensure `pam_pwhistory` module is enabled                                   |     |     |              |       |
| 5.3.3.1.1 | Ensure password failed attempts lockout is configured                      |     |     |              |       |
| 5.3.3.1.2 | Ensure password unlock time is configured                                  |     |     |              |       |
| 5.3.3.1.3 | Ensure password failed attempts lockout includes root account              |     |     |              |       |
| 5.3.3.2.1 | Ensure password number of changed characters is configured                 |     |     |              |       |
| 5.3.3.2.2 | Ensure minimum password length is configured                               |     |     |              |       |
| 5.3.3.2.3 | Ensure password complexity is configured                                   |     |     |              |       |
| 5.3.3.2.4 | Ensure password same consecutive characters is configured                  |     |     |              |       |
| 5.3.3.2.5 | Ensure password maximum sequential characters is configured                |     |     |              |       |
| 5.3.3.2.6 | Ensure password dictionary check is enabled                                |     |     |              |       |
| 5.3.3.2.7 | Ensure password quality checking is enforced                               |     |     |              |       |
| 5.3.3.2.8 | Ensure password quality is enforced for the root user                      |     |     |              |       |
| 5.3.3.3.1 | Ensure password history remember is configured                             |     |     |              |       |
| 5.3.3.3.2 | Ensure password history is enforced for the root user                      |     |     |              |       |
| 5.3.3.4.1 | Ensure pam_unix does not include nullok                                    |     |     |              |       |
| 5.3.3.4.2 | Ensure pam_unix does not include remember                                  |     |     |              |       |
| 5.4.1.1   | Ensure password expiration is configured                                   |     |     |              |       |
| 5.4.1.2   | Ensure minimum password days is configured                                 |     |     |              |       |
| 5.4.1.3   | Ensure password expiration warning days is configured                      |     |     |              |       |
| 5.4.1.5   | Ensure inactive password lock is configured                                |     |     |              |       |
| 5.4.1.6   | Ensure all users last password change date is in the past                  |     |     |              |       |
| 5.4.2.2   | Ensure root is the only GID 0 account                                      |     |     |              |       |
| 5.4.2.3   | Ensure group root is the only GID 0 group                                  |     |     |              |       |
| 5.4.2.4   | Ensure root account access is controlled                                   |     |     |              |       |
| 5.4.2.6   | Ensure root user umask is configured                                       |     |     |              |       |
| 5.4.2.7   | Ensure system accounts do not have a valid login shell                     |     |     |              |       |
| 5.4.2.8   | Ensure accounts without a valid login shell are locked                     |     |     |              |       |
| 5.4.3.2   | Ensure default user shell timeout is configured                            |     |     |              |       |
| 5.4.3.3   | Ensure default user umask is configured                                    |     |     |              |       |

## 6.x - System Maintenance (Logging and Auditing)

| CIS ID    | Recommendation                                                                       | YES | NO  | Compensating | Notes |
| --------- | ------------------------------------------------------------------------------------ | --- | --- | ------------ | ----- |
| 6.1.1.1   | Ensure journald service is enabled and active                                        |     |     |              |       |
| 6.1.1.2   | Ensure journald log file access is configured                                        |     |     |              |       |
| 6.1.1.3   | Ensure journald log file rotation is configured                                      |     |     |              |       |
| 6.1.2.1.1 | Ensure systemd-journal-remote is installed                                           |     |     |              |       |
| 6.1.2.1.2 | Ensure systemd-journal-upload authentication is configured                           |     |     |              |       |
| 6.1.2.1.3 | Ensure systemd-journal-upload is enabled and active                                  |     |     |              |       |
| 6.1.2.2   | Ensure journald ForwardToSyslog is disabled                                          |     |     |              |       |
| 6.1.2.3   | Ensure journald Compress is configured                                               |     |     |              |       |
| 6.1.2.4   | Ensure journald Storage is configured                                                |     |     |              |       |
| 6.1.3.1   | Ensure rsyslog is installed                                                          |     |     |              |       |
| 6.1.3.2   | Ensure rsyslog service is enabled and active                                         |     |     |              |       |
| 6.1.3.3   | Ensure journald is configured to send logs to rsyslog                                |     |     |              |       |
| 6.1.3.4   | Ensure rsyslog log file creation mode is configured                                  |     |     |              |       |
| 6.1.3.5   | Ensure rsyslog logging is configured                                                 |     |     |              |       |
| 6.1.3.6   | Ensure rsyslog is configured to send logs to a remote log host                       |     |     |              |       |
| 6.1.3.8   | Ensure logrotate is configured                                                       |     |     |              |       |
| 6.1.4.1   | Ensure access to all logfiles has been configured                                    |     |     |              |       |
| 6.2.1.2   | Ensure auditd service is enabled and active                                          |     |     |              |       |
| 6.2.1.3   | Ensure auditing for processes that start prior to auditd is enabled                  |     |     |              |       |
| 6.2.1.4   | Ensure audit_backlog_limit is sufficient                                             |     |     |              |       |
| 6.2.2.1   | Ensure audit log storage size is configured                                          |     |     |              |       |
| 6.2.2.2   | Ensure audit logs are not automatically deleted                                      |     |     |              |       |
| 6.2.2.3   | Ensure system is disabled when audit logs are full                                   |     |     |              |       |
| 6.2.2.4   | Ensure system warns when audit logs are low on space                                 |     |     |              |       |
| 6.2.3.15  | Ensure successful and unsuccessful attempts to use the chcon command are collected   |     |     |              |       |
| 6.2.3.16  | Ensure successful and unsuccessful attempts to use the setfacl command are collected |     |     |              |       |
| 6.2.3.17  | Ensure successful and unsuccessful attempts to use the chacl command are collected   |     |     |              |       |
| 6.2.3.18  | Ensure successful and unsuccessful attempts to use the usermod command are collected |     |     |              |       |
| 6.2.3.20  | Ensure the audit configuration is immutable                                          |     |     |              |       |
| 6.2.4.1   | Ensure audit log files mode is configured                                            |     |     |              |       |
| 6.2.4.2   | Ensure audit log files owner is configured                                           |     |     |              |       |
| 6.2.4.3   | Ensure audit log files group owner is configured                                     |     |     |              |       |
| 6.2.4.4   | Ensure the audit log file directory mode is configured                               |     |     |              |       |
| 6.2.4.5   | Ensure audit configuration files mode is configured                                  |     |     |              |       |
| 6.2.4.6   | Ensure audit configuration files owner is configured                                 |     |     |              |       |
| 6.2.4.7   | Ensure audit configuration files group owner is configured                           |     |     |              |       |
| 6.2.4.8   | Ensure audit tools mode is configured                                                |     |     |              |       |
| 6.2.4.9   | Ensure audit tools owner is configured                                               |     |     |              |       |
| 6.2.4.10  | Ensure audit tools group owner is configured                                         |     |     |              |       |


## 7.x - User Accounts and Environment

| CIS ID | Recommendation                                                    | YES | NO  | Compensating | Notes |
| ------ | ----------------------------------------------------------------- | --- | --- | ------------ | ----- |
| 7.1.1  | Ensure permissions on /etc/passwd are configured                  |     |     |              |       |
| 7.1.2  | Ensure permissions on /etc/passwd- are configured                 |     |     |              |       |
| 7.1.3  | Ensure permissions on /etc/group are configured                   |     |     |              |       |
| 7.1.4  | Ensure permissions on /etc/group- are configured                  |     |     |              |       |
| 7.1.5  | Ensure permissions on /etc/shadow are configured                  |     |     |              |       |
| 7.1.6  | Ensure permissions on /etc/shadow- are configured                 |     |     |              |       |
| 7.1.7  | Ensure permissions on /etc/gshadow are configured                 |     |     |              |       |
| 7.1.8  | Ensure permissions on /etc/gshadow- are configured                |     |     |              |       |
| 7.1.9  | Ensure permissions on /etc/shells are configured                  |     |     |              |       |
| 7.1.10 | Ensure permissions on /etc/security/opasswd are configured        |     |     |              |       |
| 7.1.11 | Ensure world writable files and directories are secured           |     |     |              |       |
| 7.1.12 | Ensure no files or directories without an owner and a group exist |     |     |              |       |
| 7.1.13 | Ensure SUID and SGID files are reviewed                           |     |     |              |       |
| 7.2.2  | Ensure /etc/shadow password fields are not empty                  |     |     |              |       |
| 7.2.3  | Ensure all groups in /etc/passwd exist in /etc/group              |     |     |              |       |
| 7.2.4  | Ensure shadow group is empty                                      |     |     |              |       |
| 7.2.9  | Ensure local interactive user home directories are configured     |     |     |              |       |
| 7.2.10 | Ensure local interactive user dot files access is configured      |     |     |              |       |
