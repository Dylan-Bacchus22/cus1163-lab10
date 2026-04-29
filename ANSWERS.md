Dylan Bacchus
Lab 10 - Operating Systems
4/29/2026

Security Risk: Why is a world-writable directory (like uploads/) more dangerous than a world-writable file? What could an attacker do?
A world-writable directory is more dangerous than a world-writable file because access to a directory grants the user more permissions. An attacker can gain access to the whole directory and delete files or install all kinds of malware.

Permission Bits: Explain what -perm -002 means versus -perm /111. Why do we use different options for different searches?
-perm -002 allows other users to modify files, while -perm /111 only grants users permissions to files they can execute. We use different options for different searches for added security.

Real-World Impact: If you ran this scanner on a production web server and found 50 world-writable files, what immediate actions should you take?
Find what files should and shouldn’t be world-writable, and then properly handle their permissions once they are analyzed.

Process Substitution: Explain why using find ... | while read doesn't work for counting, but while read ... done < <(find ...) does. What is the difference?
Using find…|while doesn’t work for counting because it creates a subshell, so count won’t persist. You have to use while read … done < <(find…) because it will run count in the current shell and update it. 

Automation: How would you schedule this script to run automatically every day at 2 AM and email the results to a security team?
I would use shell scripting to run the script automatically at 2 AM and then prompt it to send emails to the security team. 
		

