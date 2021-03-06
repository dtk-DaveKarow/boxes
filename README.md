# boxes demo
#
# david.martin@split.io

WHAT IT BE
==========

The Split boxes demo is a 10 x 10 grid
with two characters identifying each cell:
a single letter for row, and a digit for 
column.  Each grid cell can represent any
traffic type: users, tenants, accounts,
etc. The goal is to use a Split of your
choice to manipulate the "on" and "off"
state of the boxes with Split rules like
whitelisting, targeting, traffic allocation,
segments, etc.

HOW DO I INSTALL?
================

 - Download or checkout split-boxes-demo.html 
 - Create a split (in any traffic type).
 - Find the first FIXME and replace with a
browser key from the Split created in the 
previous step (you can use the Syntax button)
 - Find the second FIXME and replace with
the name of the split you created.

Don't accidentally delete the single quotes
around the key and the split name.

Don't do your editing in TextEdit, since this
Mac app will sometimes use incorrect quotes.

TRY IT, YOU MUST?
================

 - Open your split in the Split console.
 - Open your split-boxes-demo.html in 
another window.

It works best if you put the windows 
side-by-side.

 - Turn on Google Development Tools in the
split-boxes-demo.html window.

Go to the Network tab and make sure 
"Disable Cache" is checked. This step is
easy to forget, but you must remember
or the boxes won't update instantly
(browser-side cache issue).

 - Return to the Split console and
start rolling out to your boxes!

TIPS AND TRICKS
===============

- Create a segment with a block of cells
arranged together ahead of time.  Use
the segment in the whitelisting and 
targeting rules

 - Play "whitelist bingo" with the 
customer by having them throw out squares
they'd like to see turn on.

 - Don't use less than about 10% traffic
allocation or the customers will count
cells.  For the same reason, be especially
careful about showing 50/50 allocation
for less than 20% of the boxes. 

 - The boxes demo knows about 'row' and
'col' attributes.  In the targeting rules,
you can ask if 'row' is letter a through j 
is in a String list.  You can do the same for
a number between 0 and 9 of a 'col' attribute.
Don't get caught accidentally ANDing
something you expect to be an OR.

 - By planning ahead, you can illustrate
dependencies too.  Make a second split 
that whitelists only select cells.  From
the main boxes grid, declare a dependency
on the this split being on.  Flip boxes
all on, and note that only select boxes
turn on.  Why?  Now go show which boxes
are whitelisted in the dependent split... 

KNOWN PROBLEMS
==============

 - If you forget to use Google Development
Tools...

It will take ~30s for boxes to update.

 - If you have no network conection...

The boxes HTML page will be blank.

 - If you kill from another window or 
with the REST API, the original Split
window will be out-of-sync.

Refresh the Split console to sync up.

 - Something else?

Open the Javascript console and see
if there are any messages to send me.

Cheers!

David B. Martin





