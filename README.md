Part 1

How could you update most of the software on your Ubuntu OS?
```sudo apt update && sudo apt upgrade```


part 2

Screenshot of the Vim File:

![image](https://user-images.githubusercontent.com/93286045/206561208-9c62f846-d553-4eab-8ac5-3a326eb4a809.png)

Keybinding used:

```:[range]s/{pattern}/{string}/[flags] [count]```

for the file:
```:s/1/0/g```

```:s/[F|V|K]/[F|C/K]/g```

```:s|'s/[-[numbs]]*//g'|'s/[-[:digit:]]*//g'|```

part 3

To print logs for the current boot with a priority of warning or more important in pretty JSON format, the following journalctl command can be used:

```journalctl -b -p warning -o json-pretty```

The images for the man pages:




