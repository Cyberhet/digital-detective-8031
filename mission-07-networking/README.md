# Mission 7 — How computers communicate

## 1. Task / objective
Explain basic network types and concepts, observe network lookup and connectivity information, and describe step-by-step what happens when a website opens in a web browser.

## 2. Work completed

### Task 7.1 — Explain network concepts

| Concept | Explain it in your own words | Example |
|---|---|---|
| LAN (Local Area Network) | A network interconnecting devices within a limited physical geographical area. | Home Wi-Fi network connecting laptops, phones, and a wireless printer. |
| MAN (Metropolitan Area Network) | A high-speed network covering an entire town, municipality, or large university campus. | A municipal fiber-optic network connecting city government offices and libraries. |
| WAN (Wide Area Network) | A network spanning vast geographical distances, connecting multiple LANs across states or continents. | The global public Internet connecting servers and users worldwide. |
| DNS (Domain Name System) | The distributed directory service that translates human-readable domain names into machine-routable IP addresses. | Resolving `example.com` to `93.184.215.14` (or IPv6 `2606:2800:21f:cb07:...`). |
| Router | A specialized network device that forwards data packets between different computer networks using IP routing tables. | A home gateway router directing traffic between local home LAN devices and the Internet ISP. |
| Protocol | A standardized set of rules and syntax formatting that communicating entities agree upon to exchange data. | HTTPS for secure web browsing, TCP for reliable packet delivery. |
| Packet switching | A networking method where data streams are broken into discrete small packets, routed independently, and reassembled at destination. | Sending an image over the Internet split into hundreds of TCP/IP packets. |
| Client-server | An architectural model where a client device requests resources or services and a centralized server processes and fulfills the request. | A web browser (client) requesting an HTML webpage from an Apache or Nginx web server. |

---

### Task 7.2 — Observe network information
*(Privacy Note: Personal router IPs, private addresses, and local Wi-Fi names are omitted/redacted).*

- **Connectivity Test (`ping -c 3 example.com`):**
  - Sends ICMP Echo Request packets to test reachability and round-trip latency.
  - *Observation:* 3 packets transmitted, 3 received, 0% packet loss, average round-trip time ~14.2 ms.
- **DNS Lookup (`nslookup example.com`):**
  - Queries local resolver for the domain's A (IPv4) / AAAA (IPv6) records.
  - *Observation:* Resolved `example.com` to public IP address `93.184.215.14`.

#### Conceptual Questions:
- **What a connectivity test helps you check:**
  It verifies whether a target host is active, reachable across the network path, and measures packet latency and packet loss rate.
- **What information a DNS lookup displays:**
  It shows the DNS server used for resolution, the canonical hostname, and the corresponding IP addresses (IPv4 / IPv6 records) mapped to that domain.
- **The role of DNS when entering a website name:**
  Humans remember domain names (e.g. `example.com`), but network routers require IP addresses (e.g. `93.184.215.14`) to forward packets. DNS functions as the internet's phonebook, translating the entered name into the target server's IP address.

---

### Task 7.3 — What happens when you open a website? (7-Step Process)

1. **User Request & URL Parsing:** The user types a URL (e.g. `https://example.com`) into the web browser (**client**). The browser parses the protocol (HTTPS), domain name, and port.
2. **DNS Resolution:** The client checks local DNS cache; if not found, it queries a recursive **DNS** resolver to look up the IP address corresponding to `example.com`.
3. **TCP Handshake & TLS Negotiation:** Once the IP address is obtained, the client establishes a reliable connection with the **server** using the TCP 3-way handshake and negotiates cryptographic encryption via the TLS **protocol**.
4. **Packet Routing Across Network:** The client sends an HTTP GET request packet. Home and ISP **routers** inspect the packet headers and forward them across intermediate networks using **packet switching** to reach the destination server.
5. **Server Processing:** The destination **server** receives and unbundles the packets, processes the HTTP GET request, and locates the requested HTML file and assets.
6. **HTTP Response Transmission:** The server sends back an HTTP response with a status code (e.g., `200 OK`) along with the requested HTML, CSS, and JavaScript payload divided into network packets.
7. **Client Rendering:** The browser (**client**) reassembles the response packets, parses the HTML/CSS/JS, constructs the DOM and render trees, and paints the visible webpage on the user's screen.

## 3. Commands / tools used
- `ping` — Tested round-trip network connectivity and latency.
- `nslookup` / `dig` — Queried Domain Name System records for domain-to-IP resolution.
- `curl -I` — Inspected HTTP response headers and status codes.

## 4. My understanding
I understood that every online interaction relies on layered protocols (IP, TCP, TLS, HTTP) and infrastructure (routers, DNS servers). Networks operate via distributed packet switching, allowing reliable communication between heterogeneous clients and servers across the world.

## 5. Difficulties faced
Distinguishing between domain name resolution (DNS layer) and the actual transport connection (TCP/IP handshake).

## 6. How I resolved them
Traced the sequential life cycle of a web request from DNS lookup through TCP connection establishment to HTTP response rendering.

## 7. Evidence / files
- Privacy-safe ping output, nslookup records, and 7-step website communication explanation in `mission-07-networking/README.md`.

## 8. Commit details
- **Commit message:** `Explain networking concepts and website communication`
- **Pushed to GitHub:** Yes
