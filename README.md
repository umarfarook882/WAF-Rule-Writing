
# Modsecurity WAF rules Writing:
![bannner-WAF](https://cloud.githubusercontent.com/assets/22318677/26273994/8d5414d8-3d5b-11e7-9cd4-b76e4163529c.jpg)
## How to write Custom WAF rule to block new attacks on web application?
   1. At first, try to identify the security issue i.e payload or process which normally  WAF failed to detect. 
   2. Based on that develope regex pattern to match that payload. 
   3. Follow the modsecurity syntax to  write a new rule.
   4. Save the rule as .conf and include in the default rules directory.
   5. Restart the Apache server and start testing the WAF rules. 

## Demo WAF rule Writing

1. Start testing the WAF rule i.e Comodo free WAF rules or OWASP crs rules with vulnerable web application and identifying the security issue in their rules.
2. While testing the Free comodo WAF rules, I  find some loop hole which allow user to bypass sql injection rules.

`Demo Video :Testing free comodo WAF rules`

[![Alt text](https://img.youtube.com/vi/wrDX5ulLB3A/0.jpg)](https://www.youtube.com/watch?v=wrDX5ulLB3A)

3. These are the following payload which free comodo WAF rules failed to detected 

   **' /\*!or\*/1=1# <br />
   ' /\*!order\*/ By 1# <br />
   ' || 1=1# <br />
   ' &&  1=1# <br />
   ' /\*!||\*/ 1=1# <br />
   ' /\*!&&\*/  1=1#**

2. Fixing the identified security issue  by writing custom WAF rule.

`Demo Video :Writing  custom rule to block above mentioned payloads using regex expression`

[![Alt text](https://img.youtube.com/vi/8nDEXZMK2uw/0.jpg)](https://www.youtube.com/watch?v=8nDEXZMK2uw)


## Updates
If you want new rules, create an issue report and label it as enhancement Or start a pull request on our repositories.

## :scroll:Changelog
I will update new rules with  improvements i.e with out any false positive detection . Be sure to check out the [Changelog](https://github.com/umarfarook882/WAF-Rule-Writing/wiki/Change-Log)

## :octocat:Credits:
* Umar Farook: [Security Engineer | Researcher](https://www.linkedin.com/in/umar-farook-a45603101)

## :octocat:How to contribute
All contributions are welcome, from code to documentation, to design suggestions, to bug reports.
Please use GitHub to its fullest. submit pull requests, contribute tutorials or other wiki content, whatever 
you have to offer, we can use it!

## Support !
Email address: umarfarookmech712@gmail.com  for more details.

## Useful links:
 1. [Modsecurity](www.modsecurity.com/)
 2. [Kali](https://www.kali.org/)
 3. [Debuggex](https://www.debuggex.com/)
 3. [OWASP Mutillidae Vulnerable App](https://www.owasp.org/index.php/OWASP_Mutillidae_2_Project)
 
