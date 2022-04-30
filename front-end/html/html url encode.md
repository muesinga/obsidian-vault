//** HTML URL Encode **//

A URL is another word for a web address.

A URl can be composed of words (e.g. w3schools.com), or an Internet Protocol (IP) address.

Most people enter the name when surfing, because names are easier to remember than numbers.

-- URL - Uniform Resource Locator --

Web browsers request pages from web servers by using a URL.

A web address follows syntax rules:

`scheme://prefix.domain:port/path/filename`

Explanation:

• scheme - defines the tyoe of Internet service (most common is http or https)
• prefix - defines a domain prefix (default for http is www)
• domain - defines the Internet domain name (like w3schools.com)
• port - defines the port number at the host (default for http is 8-)
• path - defines a path at the server (if omitted: the root directory of the site)
• filename - defines the name of a document or resource

-- URL Encoding --

URLs can only be sent over the Internet using the ASCII character-set. If a URL contains characters outside of the ASCII set, the URL has to be converted.

URL ncoding converts non-ASCII characters into a format that can be transmitted over the internet.

URL encoding replaces non-ASCII characters with a "%" followed by hexadecimal digits.

URLs cannot contain spaces. URL encoding normally replaces a space with a plus (+) sign, or %20