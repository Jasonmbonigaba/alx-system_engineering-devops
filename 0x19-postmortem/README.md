0x19. Postmortem
<img scr="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ-MrcWQYKbB82Ev_b5CJcMM0Xl5jKTeCdUWQ&s">

Postmortem: Internal Wiki Outage (June 12, 2024)
Issue Summary:

The internal wiki was inaccessible for approximately 30 minutes on June 12, 2024, from 10:15 AM to 10:45 AM PST. During this time, employees were unable to access critical documentation and collaboration features.

Timeline:

10:15 AM PST: Multiple reports surfaced from employees about the inability to access the internal wiki.
10:17 AM PST: The IT team was notified and began investigating the issue.
10:20 AM PST: Initial checks ruled out internet connectivity problems or server outages. The focus shifted to the wiki application itself.
10:30 AM PST: Logs revealed a critical disk space issue on the server hosting the wiki application. The application ran out of space, causing it to malfunction.
10:35 AM PST: The IT team initiated a process to free up disk space by removing unnecessary log files and temporary data.
10:40 AM PST: With sufficient space available, the wiki application automatically restarted and normal service resumed.
Root Cause and Resolution:

The outage was caused by the wiki application server running out of disk space. This occurred due to a buildup of log files and temporary data that were not automatically purged. The IT team resolved the issue by freeing up disk space and allowing the wiki application to restart.

Corrective and Preventative Measures:

Implement automatic log rotation: Configure the wiki application to automatically rotate log files, deleting older entries after a set period.
Increase monitoring for disk space: Set up alerts to notify the IT team when disk space on the wiki server falls below a specific threshold.
Review temporary data management: Evaluate the wiki application's temporary data generation and implement a strategy for automatic cleanup or user-initiated purging.
By implementing these measures, we can prevent future disk space issues and ensure the continued availability of the internal wiki for employee use