# Mission Reflection

**1. Why is object storage better suited for storing millions of photos compared to a traditional block storage hard drive?**

Block storage attaches to one server as raw disk space, so scaling it means provisioning bigger or more volumes and managing a file system on top — that gets unwieldy fast at millions of files. Object storage instead stores each photo as an independent object (data + metadata + a unique ID) in a flat namespace accessed over HTTP, so it scales close to limitlessly without you managing individual disks. It's also cheaper for this kind of write-once, rarely-modified data, and apps can fetch photos directly via API/URL instead of going through a file system path.

**2. How did using Docker make it easier to deploy the MinIO storage server?**

Without Docker, you'd have to manually install MinIO's binaries, handle OS-level dependencies, and configure it for your specific Ubuntu environment. Docker packages MinIO with everything it needs into a single image, so `docker run` with the right flags gets a fully working, isolated server running in seconds, with ports and credentials configured through simple command-line flags instead of editing config files by hand.

**3. What is a "bucket" in the context of cloud storage?**

A bucket is a top-level named container that holds objects in object storage — similar in spirit to a top-level folder, but flatter (objects inside aren't nested in subfolders the way a file system works). Each bucket has its own name, access permissions, and policies, and in this lab `client-photos` is the bucket that holds all the uploaded images.

**4. How do you think large enterprise companies ensure their object storage data is not lost if the physical server crashes?**

They replicate data across multiple physical servers, often in different data centers or geographic regions, so a single hardware failure doesn't mean data loss. Techniques like erasure coding (splitting data into chunks with redundancy, as MinIO itself supports in a multi-node "distributed mode") and automated failover let the system keep serving data even if some nodes go down.

**5. How is your confidence in navigating the Linux command line growing?**

My confidence in the Linux command line is definitely growing. At first the terminal felt intimidating, but going through labs like this one made it a lot more manageable. Having clear commands to reference online helped me understand what each part of a command was actually doing instead of just copying and pasting blindly. I'm starting to recognize patterns in how commands are structured, which makes me feel more comfortable experimenting instead of being afraid of breaking something.
