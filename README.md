# simple bash student's timer
Just a simple cli timer written in bash that I made to help me to control my study time.\
The timer can be paused and resumed anytime, and when you are done with your studies (or whatever you are doing), you can finish the timer and sbst will save the session.\
You can list the sessions, filtering by topic, or see the total acumulated hours for a topic. I made it for studies, but in the end, of course, sbst can be used to track time for any kind of activity.

### Instalation
Just throw the scripts in your $PATH.

### Usage
Refer to the help option:
```
$ sbst --help
        SBST USAGE
        You need to create a topic with sbst -n before starting the timer.
        The <index> is the topic number in the output of sbst -l.

        Options:
         Manage Topics:
         -n, --new              create a new topic
         -l, --list             list created topics

         Timer:
         -S, --start            start the timer
         -s, --show             show timer status
         -p, --pause            pause the timer
         -r, --resume           resume the timer
         -f, --finish           finish the timer and save data

         View data:
         -a, --view-all         view all entries
         -v, --view <index>     view entries for a topic
         -H, --hours <index>    view total acumulated hours for a topic

         -h, --help             print this help message

```

### Know Issues
I forgot to make some input validation, so if you input unexistent topics when trying to view data, it you give you some sed or cat errors instead of a message explaning the mistake.
The date when you print the sessions with -a or -v seems to be off by 2 or 3 hours, perhaps a wrong locale when using date command.
I will fix those later.

