# Mission Reflection

> This is a starting scaffold (~structure + prompts), not a finished reflection — swap in your own experience and specifics from *your* KillerCoda session before submitting. Target: 250–350 words total.

**1. Which cloud infrastructure component do you think is the most important? Why?**
I think compute is the most important component, because it's the resource that actually does the work — everything else exists to support it. In my KillerCoda environment, lscpu showed a single-core Intel Xeon E312xx CPU running under KVM virtualization, which is a small but real example of how a cloud provider slices physical hardware into sized instances. Without compute, the storage and network I investigated would just be idle disk space and an unused address — compute is what turns infrastructure into a running application.

**2. How does Linux support cloud computing?**

Linux supports cloud computing by being lightweight, scriptable, and free to run at scale, which is why most cloud provider base images — including the Ubuntu 24.04.4 LTS image I found running via cat /etc/os-release — are Linux distributions. Its command-line tools make investigation and automation straightforward: with a handful of commands (lscpu, df -h, hostname) I was able to fully inventory a server's compute, storage, and network identity in minutes, which is exactly the kind of repeatable process cloud engineers rely on for provisioning and auditing real infrastructure.

**3. Why is technical documentation important before deploying infrastructure?**

Documentation matters because infrastructure decisions are invisible once they're running — nobody can look at a live server and instantly know why it was sized a certain way or what's mounted where. Recording findings like mine (a 19G root volume at 30% usage on /dev/vda1, a single-core CPU, hostname ubuntu) gives other engineers a starting reference point, prevents miscommunication about capacity or configuration, and creates a paper trail to troubleshoot from if something breaks later.

**4. What new skills did you learn during this laboratory activity?**

I learned how to pull a full hardware and OS inventory from a Linux server using just the command line — CPU details with lscpu, disk usage with df -h, and OS identity with /etc/os-release. I also learned to connect that raw output to cloud concepts: a single-core KVM-virtualized CPU is conceptually the same "sized instance" idea behind an AWS EC2 or Azure VM tier, just running in a lightweight playground instead of a production data center.

**5. How has your GitHub portfolio improved after completing this mission?**

My portfolio now includes a new, organized lab folder with a full infrastructure inventory, a components breakdown, a provider comparison, an architecture diagram, and documentation — real evidence that I can investigate a server and write it up clearly, not just follow instructions.

---

*Word count target: 250–350 words. Draft each answer above, then combine into flowing paragraphs (or keep numbered) and check the count before submitting.*
