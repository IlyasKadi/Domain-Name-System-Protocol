<div id="top"></div>



<!-- PROJECT LOGO -->
<br />
<div align="center">
    <img src="images/logo.png" alt="Logo" width="700" height="400">
  <h2 align="center">Project 2</h2>
  <h3 align="center">Domain Name System Protocol</h3>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  
    <li>
      <a href="#Part-I">Part I : DNS configuration</a>
         <ul>
              <li><a href="#DNS-role-functions">DNS, role & functions</a></li>
              <li><a href="#different-DNS-servers">different DNS servers</a></li>
              <li><a href="#DNS-configuration-steps">DNS server’s configuration steps</a></li>
                  <ul> 
                      <li><a href="#Configure-the-named">Configure the named.conf</a></li>
                      <li><a href="#configure-zone-files">Create and configure zone files</a></li>
                      <li><a href="#Verify-the-configuration">Verify the configuration</a></li>
                  </ul>
              <li><a href="#Configure-the-DNS-Client">Configure the DNS Client</a></li>
              <li><a href="#Configure-primary-and-secondary-DNS-servers">Configure primary and secondary DNS servers</a></li>
                  <ul> 
                     <li><a href="#primary-DNS-server">primary DNS server </a></li>
                     <li><a href="#secondary-DNS-server">secondary DNS server</a></li>
                     <li><a href="#Test-the-configuration">Test the configuration by stopping the master DNS</a></li>
                  </ul>
           </ul>
        </li>
        <li><a href="#Part-II">Part II : DDNS configuration</a>
            <ul> 
              <li><a href="#Configure-the-DDNS-server">Configure the DDNS server</a></li>
                   <ul> 
                     <li><a href="#Install-the-necessary-packages">Install the necessary packages</a></li>
                     <li><a href="#Configure-the-forward-and-reverse-zones">Configure the forward and reverse zones</a></li>                          
                   </ul>
              <li><a href="#Configure-the-client">Configure the client</a></li>
              <li><a href="#Verify-the-configuration">Verify the configuration</a></li>
            </ul>
           </li> 
        <li><a href="#Part-III">Part III : DDNS and DMZ</a></li>
  
</details>



<!-- Part-I -->
# Part-I

<!-- DNS role functions -->
## DNS-role-functions

**What is DNS?**

The Domain Name System (DNS) is the phonebook of the Internet. Humans access information online through domain names, like nytimes.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses. DNS translates domain names to IP addresses so browsers can load Internet resources.

Each device connected to the Internet has a unique IP address which other machines use to find the device. DNS servers eliminate the need for humans to memorize IP addresses such as 192.168.1.1 (in IPv4), or more complex newer alphanumeric IP addresses such as 2400:cb00:2048:1::c629:d7a2 (in IPv6).

**How does DNS work?**

The process of DNS resolution involves converting a hostname (such as www.example.com) into a computer-friendly IP address (such as 192.168.1.1). An IP address is given to each device on the Internet, and that address is necessary to find the appropriate Internet device - like a street address is used to find a particular home. When a user wants to load a webpage, a translation must occur between what a user types into their web browser (example.com) and the machine-friendly address necessary to locate the example.com webpage.

In order to understand the process behind the DNS resolution, it’s important to learn about the different hardware components a DNS query must pass between. For the web browser, the DNS lookup occurs "behind the scenes" and requires no interaction from the user’s computer apart from the initial request.

**There are 4 DNS servers involved in loading a webpage:**

   - **DNS recursor** - The recursor can be thought of as a librarian who is asked to go find a particular book somewhere in a library. The DNS recursor is a server designed to receive queries from client machines through applications such as web browsers. Typically the recursor is then responsible for making additional requests in order to satisfy the client’s DNS query.
   
   - **Root nameserver** - The root server is the first step in translating (resolving) human readable host names into IP addresses. It can be thought of like an index in a library that points to different racks of books - typically it serves as a reference to other more specific locations.
   
   - **TLD nameserver** - The top level domain server (TLD) can be thought of as a specific rack of books in a library. This nameserver is the next step in the search for a specific IP address, and it hosts the last portion of a hostname (In example.com, the TLD server is “com”).
   
   - **Authoritative nameserver** - This final nameserver can be thought of as a dictionary on a rack of books, in which a specific name can be translated into its definition. The authoritative nameserver is the last stop in the nameserver query. If the authoritative name server has access to the requested record, it will return the IP address for the requested hostname back to the DNS Recursor (the librarian) that made the initial request.

**What's the difference between an authoritative DNS server and a recursive DNS resolver?**

Both concepts refer to servers (groups of servers) that are integral to the DNS infrastructure, but each performs a different role and lives in different locations inside the pipeline of a DNS query. One way to think about the difference is the recursive resolver is at the beginning of the DNS query and the authoritative nameserver is at the end.



<p align="right">(<a href="#top">back to top</a>)</p>

<!-- different DNS servers -->
## different-DNS-servers

 

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- DNS configuration steps -->
## DNS-configuration-steps

### Configure-the-named



### configure-zone-files




### Verify-the-configuration


<p align="right">(<a href="#top">back to top</a>)</p>

<!-- Configure the DNS Client -->
## Configure-the-DNS-Client


<p align="right">(<a href="#top">back to top</a>)</p>



<!-- Configure primary and secondary DNS servers -->
## Configure-primary-and-secondary-DNS-servers
### primary-DNS-server


### secondary-DNS-server


### Test-the-configuration

<p align="right">(<a href="#top">back to top</a>)</p>

# Part-II
## Configure-the-DDNS-server

<p align="right">(<a href="#top">back to top</a>)</p>

### Install-the-necessary-packages




### Configure-the-forward-and-reverse-zones




<p align="right">(<a href="#top">back to top</a>)</p>


<!-- Configure the client -->
## Configure-the-client





<p align="right">(<a href="#top">back to top</a>)</p>


<!-- Verify the configuration -->
## Verify-the-configuration


<p align="right">(<a href="#top">back to top</a>)</p>

# Part-III
 **Project description:**
  - The goal is to set up a DNS server on a demilitarized zone, based on the delegation  between  two  DNS  servers  (parent  server  and  child  server).The network diagram is as follows:
  
<p align="center">
     <img src="images/part3.png">
   </p>

<p align="right">(<a href="#top">back to top</a>)</p>

Out Team - [AIT EL KADI Ilyas](https://github.com/IlyasKadi) - [AZIZ Oussama](https://github.com/ATAMAN0)

Project Link: [https://github.com/IlyasKadi/Domain-Name-System-Protocol](https://github.com/IlyasKadi/Domain-Name-System-Protocol)

<p align="right">(<a href="#top">back to top</a>)</p>
