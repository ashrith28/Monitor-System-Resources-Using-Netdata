
# Task 7 - Monitor System Resources with Netdata

## Objective
Install and run Netdata to visualize system and application performance metrics in real time.

## Steps Followed
1. Installed Docker on my system.
2. Pulled the official Netdata image:
   ```
   docker run -d --name=netdata \
     -p 19999:19999 \
     --cap-add SYS_PTRACE \
     --security-opt apparmor=unconfined \
     netdata/netdata
     ```


3. Accessed the dashboard at: ``` http://localhost:19999 ```
4. Explored CPU, memory, disk, and container usage metrics.

# screenshots of the running dashboard

!<Screenshot 2025-10-02 194928-1.png>

!<Screenshot 2025-10-02 195400.png>

5. To stop Netdata:
```
docker stop netdata
docker rm netdata

```
