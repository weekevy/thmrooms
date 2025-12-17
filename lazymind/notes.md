# notes LazyAdmin

## recon
#### Nmap result
![img1](./img/nmap_result.png)
we notice by the following output the server use **ssh** and **ubutu** server
#### Content Discovery
``` ffuf -u http://TARGET_MACHINE/FUZZ -w /path/wordlist ```
- ffuf output after we do directory enumeration we notice that we get output 
![img2](./img/ffuf_output.png)

- let's try visit the web page ```http://TARGET_MACHINE/content```
- we notice that website mention something about **SweetRice** CMS and stuff like that, best thing
  todo is googling what SweetRice cms is
- after check the page source code nothing is suspicious

![img3](./img/content_page.png)

- let's try doing enumeration inside content endpoint
- the wordlist we gonna try the ***raft-meduim-files.txt*** we can find it in seclist repo
``` ffuf -u http://TARGET_MACHINE/content/FUZZ -w /path/wordlist ```


















