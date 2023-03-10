# Non-Profit Email Alias Strategy

This document describes a strategy for non-profit email address allocation.

## Requirements

Below are requirements
* Each person chooses the email inbox(es) where they ultimately get email
* Each person has an invariant email alias that does not change when positions change (ex: jane.doe@non-profit.org)
* Each position has an email alias that can be updated when the position transitions (ex: events-chair@non-profit.org)
* Each committee has an email alias that can forward to multiple committee members (ex: events@non-profit.org)
* The non-profit email administrators (admins) only need to update each position upon transition

## Detailed Design

Nested groups might look something like below:
* exec-board@non-profit.org
    * president@non-profit.org
        * jane.doe@non-profit.org
            * jane.doe@gmail.com
    * vice-president@non-profit.org
        * john.smith@non-profit.org
            * jsmith@college.edu
    * secretary@non-profit.org
        * david.black@non-profit.org
            * davidb-non-profit@gmail.com
    * treasurer@non-profit.org
        * amy.white@non-profit.org
            * amy.n.white@company.com
    * communications@non-profit.org (for the Communications Committee)
        * communications-committee-chair@non-profit.org
            * peter.parker@non-profit.org
                * pparker@nynex.net
        * secretary@non-profit.org
            * ...
        * technology-committee-chair@non-profit.org
            * ...
    * events@non-profit.org (for the Events Committee)
        * events-chair@non-profit.org (for the Events Chair)
            * brad.blue@non-profit.org
                * brad@blue.com
        * treasurer@non-profit.org (in this example, the Treasurer is on the Events Committee)
            * (see above)
        * clark.kent@non-profit.org (individual on Events Committee)
            * kent@dailyplanet.com

## Optional Features

For some Committees, the organization may want to have one email address for formal announcements and another email address for open discussion.  (ex: exec@non-profit.org for Executive Board announcements and  
