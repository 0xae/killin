killin - Kill It Now!
=======
killin is a poor man implementation of pkill with some extra features

## Usage

	killin -f [-nhrl] 
             -f string    # mandatory filter (ex: java)
             -n count     # get the first <count> processes
             -r resource  # specify resource (cpu or mem)
             -y           # dont ask for confirmation damn it
             -l           # just list the processes 
             -h           # show this help

## Examples

Kill the top 5 chromium processes that are eating more ram
    
    ./killin -f chromium -n 5 -r mem -y

Kill the top 2 chromium processes that are eating more cpu

    ./killin -f chromium -n 2 -r cpu -y

Just list the top 5 java processes that are eating more cpu

    ./killin -f java -n 5 -r cpu -l

## Warning

This is a very dangerous utility that should be used with lots of care.
We wont take responsability for any damage caused to yo.
So be judicious.

