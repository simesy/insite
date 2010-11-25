Insite, site insight.
---------------------

Copyright Simon Hobbs 2010. Licensed GPL, etc.

** This module is not supported. **
** This module is not recommended for production. **

This Drupal module is a basic inspection tool for your Aegir platform. It
currently allows you to compare variables across the sites managed by Aegir.

Example: "What is the current site_mail for all of the sites I manage?"
 
Perhaps more useful is that the module demonstrates how to implement a
hosting queue so that you can execute arbitrary drush commands as the
'aegir' user.

Basically and currently, this module gathers information about variables and
collates this information into tables Hostmaster's database. They can then be
searched at /insite/variable-search.

To install, install this module in the main Hostmaster platform. Remember to
put it in sites/example.com/modules if you want the module to follow along when
Aegir is updated. If everything is working, the {insite_variable} table should fill
up on subsequent Aegir cron runs. Then the search should work!

CONSIDERATIONS:
-- Doesn't show stored variable values, only after bootstrap. Which is prolly just fine.
-- Assume unscaleable, only trialed on Aegir with ~20 sites.
-- Currently ignoring arrays and object variables.
-- Sites currently are analysed every 24 hours, hardcoded into sql.
-- Not tested on a multiserver environment, so it probably won't work.

