# Route 53


### Important Concepts
- A Record (Address Record):
Think of an A Record like a street address for your website. It connects your domain name to a specific IP address, telling computers exactly where to find your website's server. <br/>

  - Example: Imagine you have a website called "www.example.com" and your server's IP address is "192.168.1.100". By creating an A Record for "www.example.com" with the value "192.168.1.100", you're basically telling computers, "When someone types 'www.example.com', go to the server at IP address '192.168.1.100'."

- CNAME Record (Canonical Name Record):
Think of a CNAME Record like a shortcut or a signpost that points to another domain. It's used when you want to link one domain to another without revealing the actual destination's IP address. <br/>
  - Example: Let's say you have a blog on a separate server with the address "blog.example.com," but you want it to show the same content as your main website "www.example.com". Instead of duplicating everything, you can create a CNAME Record for "blog.example.com" and set its value to "www.example.com". This means that when someone goes to "blog.example.com", they'll actually end up at "www.example.com" but still see "blog" in the address bar.

- AAA Record (AAAA Record):
Think of an AAAA Record like a modern phone number for the internet. It's used to connect your domain name to an IPv6 address, which is important as IPv6 addresses are replacing the older IPv4 addresses due to the limited availability of the latter. <br/>

  - Example: If your website's server has an IPv6 address like "2001:0db8:85a3:0000:0000:8a2e:0370:7334", you can create an AAAA Record for "www.example.com" with the value "2001:0db8:85a3:0000:0000:8a2e:0370:7334". This tells computers that when someone types "www.example.com", they should use this IPv6 address to reach your website.

- In Amazon Route 53, you can manage these records to control how your domain name connects to different services or servers. Just like your contact list on your phone helps you reach people, these records help the internet find the right places when you use domain names.

#### TTl (Time to live)
- When you update a DNS record, the TTL value determines how long other DNS servers will continue to use the old cached information before querying your authoritative DNS server again for the updated data.
- Imagine you have a big book that holds addresses for different websites. This book is called DNS, and it helps computers find websites when you type in their names.
- Now, sometimes the addresses of websites change, like when a website moves to a new place. When this happens, the book needs to be updated so computers can find the website at its new location.
- But here's the catch: the book is so big that not everyone gets a new copy right away. Instead, they use the old copy they have for a certain time before asking for a new one.
- That "certain time" is what we call Time to Live (TTL). It's like a countdown timer. When you tell the book that a website's address has changed, you also set the timer. Until the timer reaches zero, computers will keep using the old address they remember from the book.
- After the timer is up, they'll ask the book for the new address. This way, changes to website addresses spread gradually across the internet, instead of everyone asking for the new address all at once.
- So, TTL helps control how quickly everyone gets the latest address when a website moves to a new spot. It's like a waiting time for updates to spread out, and it's measured in seconds.
- It's important to note that while short TTLs can help propagate changes quickly, they can also increase the load on DNS servers due to frequent queries.
- Longer TTLs reduce the load but result in slower changes when updates are made to DNS records.






























