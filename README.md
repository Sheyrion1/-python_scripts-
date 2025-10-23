import os
import time

hosts = ["8.8.8.8", "1.1.1.1"]

while True:
    for host in hosts:
        response = os.system(f"ping -c 1 {host} > /dev/null 2>&1")
        status = "UP" if response == 0 else "DOWN"
        print(f"{host}: {status}")
    time.sleep(10)
