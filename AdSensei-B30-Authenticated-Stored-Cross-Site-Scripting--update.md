# Exploit Title: AdSensei B30 <= 1.9.9.9 - Authenticated Stored Cross-Site Scripting (XSS)
# DownloadLink: https://downloads.wordpress.org/plugin/adsensei-b30.zip
# Affects Version:1.9.9.9
# Original Researcher:websafe2021
# Description:
The WordPress plugin AdSensei B30 <= 1.9.9.9 does not escape its 'adsenseib30_settings[adName10]'  From 'Ad10 Edit name' settings
allowing high privilege users such as admin to perform Cross-Site Scripting attacks even when the unfiltered_html capability is disallowed

# Proof of Concept:
```
adsenseib30_settings[adName10]="><script>alert(123)</script>
```
  
 
![B30-xss](https://user-images.githubusercontent.com/100707395/156787197-118f5abe-58ca-46b5-9907-4b6a4b385452.gif)

