# Lab 2: Mermaid Diagrams
## Assignment: Creating a Sequence Diagram for a Network Attack Scenario

```mermaid
sequenceDiagram
    box red bad
    actor attacker
    actor botnets
    end    
    box Green good
    actor users
    end
    box grey target
    participant firewall
    participant server
    end
    users-->>firewall: traffic
    firewall-->>server: approve traffic
    server-->>users: allocate resources
    attacker -->>users: malware to "n" users
    users-->>botnets: "n" users involuntary part of botnet army
    botnets-->>firewall: "n" disguised traffic
    firewall-->>server: approve "n" disguised traffic
    server-->>botnets: overload resources "Server Crash"
    users-->>firewall: traffic
    firewall-->>server: approve traffic
    server-->>users: no access "server down"
```
### Diagram Explanation

**Participants**
* _attacker_ - A hacker who creates and controls a botnet to flood a target with traffic and disrupt its services.
* _botnets_ - A botnet is a network of infected computers or devices controlled by a hacker to carry out cyberattacks without the owners knowing.
* _users_ - day-to-day normal users of the server
* _firewall_ - A firewall is a security system that monitors and controls incoming and outgoing network traffic
* _server_ - A server is a powerful computer or system that stores, processes, and delivers data, services, or applications to other computers (clients) over a network.