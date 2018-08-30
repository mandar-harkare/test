#.git/hooks/commit-msg to add JIRA number from branch name
#!/bin/sh

# Add git branch if relevant
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

# Extact tracker abbreviation and ticket number (e.g. DS-123)
parse_git_tracker_and_ticket() {
  parse_git_branch | grep -e '[A-Z]\+-[0-9]\+' -o
}

MESSAGE="$(cat $1)"
TICKET=`parse_git_tracker_and_ticket`

if [ -n "$TICKET" ]
then
   echo "New commit message: [$TICKET] $MESSAGE"
   echo "[$TICKET] $MESSAGE" > $1
fi

working for merge and Done
# test
dfsfchanging text to check emojis
test
again

belongs to test branch 

checking the git hook

check again

why???

checking the integration


# checking JIRA inegration

test it now

# test the transition now
Cleaning up the stuff


transition using workflow instead from Git
Done??

# check the comments
not working on this anymore


# Merging is creating a difference
lets work on that
working
try removing the In Progress condition
test again with modified condition
that was a mistake

did work

lets try one more time
