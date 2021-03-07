# Areia_Message_Gagger
Add, remove, enable, and disable gags easily

# General Overview
This plugin is intended to simplify the process of handling simple gag triggers. Say you're headed on an epic run. You don't really want to see messages about experience gained or gold shared. Say you're pupping/leveling in a well-known zone and don't want to see all the damage messages the mobs spam you with.
With this plugin, you can easily create groups of related messages and turn them on or off without having to open and search through your triggers menu.
By default, you enter regular expressions that match the lines you want to gag. However, there is also an option to simplify that portion, allowing you to enter plain text with simple * wildcards if you're not comfortable using regex.

# Commands
# amg restoredefault [confirm]
Restores the plugin to its default state. ***Note: this will permanently delete
all messages you have added and revert all changes you have made. Be certain
this is what you want before adding the 'confirm' argument.

# amg count
Displays a brief count of the number of enabled messages and groups.

# amg show [<group name> [<message name>]]
Displays info on the requested group or message. 'Amg show' on its own gives a
list of all groups along with an indication of whether each group is enabled or
disabled currently. 'Amg show <group>' will display all messages within that
group, along with an indication of its enabled status and a peek at its match
string. To see a message's full regex, enter 'amg show <group> <message>'.

# amg <enable|disable> [<group name> [<message name>]]
Enables or disables the given group or message. 'amg <en|dis>able' on its own
will enable/disable all groups. To enable/disable a single group, use
'amg <en|dis>able <group>', and to enable/disable only a single particular
message, enter 'amg <en|dis>able <group> <message>'.

# amg add <group name> <message name> <match string>
Adds a new message to be gagged. All arguments are required. The message will
be given the name <message name>, added to the group called <group name> (which
will be created if it does not exist), and will gag the line described by
<match string>. The match string should be a regular expression. Group and
message names may contain only letters, numbers, and underscores.

# amg edit <group name> <message name> <name|group|match> <value>
Changes the given field of the nominated message. <Value> is the value you wish
to assign to the field. For example, to change the name of the sanc message in
the spellup group to 'sanctuary', enter 'amg edit spellup sanc name sanctuary'.
Assigning a group name that does not already exist will create a new group;
likewise, if a group is left empty by this operation, it will be removed.

# amg remove <group name> [<message name>] [confirm]
Removes the given group or message. If only a group name is given, all messages
in that group will be deleted. Note that this cannot be reversed, so be certain
you have the correct group and message names before adding the 'confirm'
argument.

# amg regex [on|off]
Choose the method in which the plugin will receive and display match strings.
Default is on, which means you should enter and will see regular expressions.
That method is more powerful but also more complicated. Turning regex off will
allow you to enter simple strings for your gag triggers. You may use '*' as a
wildcard, and '\\*' to match a literal '*' (e.g., '* waves at you.' would gag
any line where Jo, or Bob, or anyone else waves at you).

# amg update
Check for and install updates to the plugin.
