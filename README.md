Part 1.

How could you update most of the software on your Ubuntu OS?
```sudo apt update && sudo apt upgrade```


part 2.

Screenshot of the Vim File:

![image](https://user-images.githubusercontent.com/93286045/206561208-9c62f846-d553-4eab-8ac5-3a326eb4a809.png)

Keybinding used:

```:[range]s/{pattern}/{string}/[flags] [count]```

for the file:
```:s/1/0/g```

```:s/[F|V|K]/[F|C/K]/g```

```:s|'s/[-[numbs]]*//g'|'s/[-[:digit:]]*//g'|```

part 3.

To print logs for the current boot with a priority of warning or more important in pretty JSON format, the following journalctl command can be used:

```journalctl -b -p warning -o json-pretty```

![image](https://user-images.githubusercontent.com/93286045/206566255-27d7ea61-ada3-4cd2-b381-e1fcfae6aa37.png)


The images for the man pages:

Information about these options can be found in the "SYNOPSIS" section of the journalctl man page, as well as in the "OPTIONS" section. 

Make it look pretty

![image](https://user-images.githubusercontent.com/93286045/206565508-f4996cbb-a37b-4f52-a528-bce362416706.png)


The -b, -p, and -o options are all described in detail in the "OPTIONS" section.

the -o
![image](https://user-images.githubusercontent.com/93286045/206564711-7c990252-ec3b-46fb-9f8d-1a55f7710f03.png)

the -b
![image](https://user-images.githubusercontent.com/93286045/206564904-e2a65a2f-169d-49e7-91e1-5233267d7f4c.png)

the -p
![image](https://user-images.githubusercontent.com/93286045/206564980-e0027888-af22-4b55-a7e2-b5bba70877f0.png)


part 4.

Scipt without the motd file changes:

```
#!/bin/bash

file="/etc/passwd"

users=$(grep -E "^.+:x:[1-5][0-0][0-0][0-9]:" $file)

results=$(awk -F ":" '{ print $1 ": " $3 }' <<< "$users")

echo "Regular users with a UID from 1000 to 5000:"
echo "$results"
```

Script after changes:

```
#!/bin/bash

file="/etc/passwd"

users=$(grep -E "^.+:x:[1-5][0-0][0-0][0-9]:" $file)

results=$(awk -F ":" '{ print $1 ": " $3 }' <<< "$users")

echo "$results" > /etc/motd
```

image of code working:
![image](https://user-images.githubusercontent.com/93286045/206568225-8c90fdf0-5627-42d8-b91c-a64d6c052cd9.png)

the `W` Command:
![image](https://user-images.githubusercontent.com/93286045/206568528-931bc4ac-1261-45f2-ac9c-2e0d0fd60c0d.png)

Part 5.




