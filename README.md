# series

Keep track of your series without the need to remember where you left off.

## Quick start

Watch your favourite series with just

    cd ~/Videos/Mr.\ Robot
    series .

or

    series ~/Videos/Mr.\ Robot

The script will run your favourite player (set in `~/.seriesrc`) with first
episode found in file tree (recursively and in alphabetical order). Series
entry will be created in `~/.series` to keep track on where you left off. After
you're done watching run the command again to watch another episode. Series
entry will be updated for you again.


## More

If you want to start watching from some other episode you should use set
command with a number or a pattern (used by grep -i).

    series ~/Videos/Mr.\ Robot set s02e05
    series ~/Videos/Mr.\ Robot set -4
    series ~/Videos/Mr.\ Robot set +2
or

    series ~/Videos/Mr.\ Robot set 21


When you're done with series entry will be deleted after watching the final
episode. If you want to delete it before that use del command.

    series ~/Videos/Mr.\ Robot del

And to add series entry manually use add.

    series ~/Videos/Mr.\ Robot add

To show your progress on given series use ls command.

    series ~/Videos/Mr.\ Robot ls 3

You will see 7 episodes with center one as next to watch


## ~/.seriesrc

This file contains variables used by the script.

    # formats - list of file extensions treated like episodes by the script (used by find command)
    formats=(-iname '*.mkv' -o -iname '*.avi' -o -iname '*.mp4')

    # player - your favorite player plus additional parameters
    player=(mpv --fs)

