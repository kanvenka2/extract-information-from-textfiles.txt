# extract-information-from-textfiles.txt


1.Extract log.tar.gz
2.Look for unauthorized connection attempts
3.Extract the usernames an attacker tried to use
4.Create a file containing these names (and make it organized)
solution:
1.codebind@DESKTOP-N3JS6V2:~$ tar -xvf log.tar.gz
2.codebind@DESKTOP-N3JS6V2:~$ less auth.log
  codebind@DESKTOP-N3JS6V2:~$ cat auth.log | grep "imput_userauth_request" | awk '{print $9}'
3.codebind@DESKTOP-N3JS6V2:~$ cat auth.log | grep "input userauth request"|awk '{print $9}'
4.codebind@DESKTOP-N3JS6V2:~$ cat auth.log | grep "input userauth request"|awk '{print $9}'|sort -u > users.txt
