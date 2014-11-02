absalon-scraper
===============
Scrape information from Absalon courses (the course platform used at
University of Copenhagen). For use with the R-package
dybber/courseviz.

Authors
-------
Original scraping script was made by Sebastian Paaske Tørholm. This is
an extended version made by Martin Dybdal that collects even more
information (e.g. assignment deadlines and student's last visit to the
course page) and saves in CSV instead of JSON (JSON is not nice to
read from R).

Usage
-----
*TODO: command line interface is not done yet. This section will be
written as soon as that is implemented. Current usage involves
customization directly in the script*

Information collected
---------------------
 * List of participants
    - Last visit on course page
    - Exercise class
 * List of assignments
    - Group/Individual
    - Submission deadline
    - Mandatory or not
    - Number of answers
    - Max score
 * List of handins (per assignment)
    - Group
    - Score
    - Status (submitted, resubmit, approved, unapproved, etc.)
    - Submission time
    - Review date

Advanced uses
-------------
 * Create assignments (eventually hidden) that students should not
   submit anything for, e.g. "Is exam qualified?"-assignment with
   scores "Is qualified" and "Is not qualified".

TODO
----
 * Commandline interface (e.g. currently hardcoded output locations etc.)
 * JSON-output
 * Anonymization option
 * Testing on other courses with other evaluation types
 * Testing with Danish Absalon-interface (currently only tested on
   English interface)
 * Standardize date-format (several different formats are used)
 * Support for several types of groups. Currently you can only belong
   to a single exercise class. Sometimes we also have other groups
   e.g. "DIKU students", "Outside DIKU", "Repeater (dansk: omgænger)"
 * Optimizations

Installation
------------
I *think* this all these packages are needed, but it might be too
many. Getting that sorted out is on the TODO-list :-)

```
sudo apt-get install libutf8-all-perl libdatetime-perl \
      libdatetime-format-strptime-perl libwww-mechanize-perl libsyntax-perl \
      libsub-exporter-progressive-perl libsub-exporter-perl libio-all-perl \
      libyaml-syck-perl
```
