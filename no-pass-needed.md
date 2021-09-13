# no-pass-needed

Challenge description: It's all about who you know and I know 'admin'.

# Vulnerability
By the description, we can easily know that this challenge is sql injection challenge. 

# Examining_the_Website
When i put some payloads. i noticed that this website is removing spaces. And also you can see in (/robots.txt). It show us error message that the website is removing spaces.

Robots.txt: TypeError: Cannot read property &#39;search&#39; of undefined

# Solution
I practiced in PortSwigger sql injection labs before. So i know some basics. 

If the website is removing our inject code's spaces, we can add (/**/) in the spaces area. 

So our original payload is (admin'or 1=1 -- -). So in our original payload, we can see there is three spaces. So i add (/**/) in there.

So our final payload will be like this: (admin'or/**/1=1/**/--/**/-).

So i used this payload and it worked. we successfully login to the website. and got flag. Nice challenge.

# Payloads
original_payload = (admin'or 1=1 -- -)
edited_payload = (admin'or/**/1=1/**/--/**/-)

# Flag
flag{wh0_n3ed5_a_p4ssw0rd_anyw4y}

# Sorry
I can't upload or put images here because of my laptop error. Sorry
