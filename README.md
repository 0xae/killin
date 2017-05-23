killin - Kill It Now!
=======
killin is a poor man implementation of pkill with some extra features

## Usage

	killin -f [-nhrl] 
             -f string    # mandatory filter (ex: java)
             -n count     # get the first <count> processes default: 1
             -r resource  # specify resource (cpu or mem) default: mem
             -y           # dont ask for confirmation damn it
             -l           # just list the processes 
             -h           # show this help

## Motivation

Sometimes i want to kill processes based on the 
resource that is being "abused" (cpu or mem) and i need
a safe way to make sure i am not messing with other important processes (thus the mandatory filter)

## Examples

Kill the top 5 chromium processes that are eating more ram
    
    ./killin -f chromium -n 5 -r mem 
    -------
    kill  chromium pid= 28083 $resource= 2419292
    kill  chromium pid= 28125 $resource= 1968152
    kill  chromium pid= 29285 $resource= 1116864
    kill  chromium pid= 13672 $resource= 1098564
    -------
    are you certain? (y/n) y


Kill the top 2 chromium processes that are eating more cpu
and dont ask for confirmation

    ./killin -f chromium -n 2 -r cpu -y

Just list the top 5 java processes that are eating more cpu

    ./killin -f java -n 5 -r cpu -l

## Tip
If you wish to kill all processes that matches a certain criteria use `pkill` instead

    pkill chromium

## Warning

This is a very dangerous utility that should be used with lots of care.
We wont take responsability for any damage caused to yo.
So be judicious.

### Enjoy
