ROLE 1: ROS DRIVER (COLLECTOR)



Role intent:

The ROS driver is the only operational user of the mobile application.

The application must support fast, simple and error-resistant data entry.



Main responsibilities:



* Start and complete trips (planned or ad-hoc)
* Register collections per location
* Enter quantities and optional comments
* Confirm unloading at MOG



What the driver can do:

* View own planned trips
* Register collections and submit them
* Receive immediate validation warnings
* Override warnings with a mandatory comment
* View own past submissions



What the driver cannot do:



* Edit submitted collections
* Delete data
* Enter or view EURAL codes, weights or backend calculations
* View data from other drivers



Design principle:

Drivers only enter information they are certain about.

All calculations, codes and validations are handled by the system.



ROLE 2: ECOG ADMINISTRATIVE ASSISTANT



Role intent:

The administrative assistant ensures planning continuity, monitoring

and reporting, but does not correct operational data.



Main responsibilities:



* Maintain weekly planning templates
* Apply last-minute planning changes
* Monitor submitted and flagged collections
* Prepare operational views and MATIS exports
* Follow up anomalies outside the application



What the admin can do:



* View all trips and collections
* Filter and search historical data
* Add administrative comments
* Export data for reporting purposes



What the admin cannot do:



* Edit quantities or registrations submitted by drivers
* Override or "fix" operational data
* Submit collections on behalf of drivers



Design principle:

Submission by the driver is final.

Administrative work focuses on oversight, follow-up and reporting.



ROLE 3: RECYCLING PARK OR SHOP (VIEW-ONLY)



Role intent:

Recycling parks and shops are informed stakeholders, not active system users.



Main responsibilities:



* Be informed that a collection has taken place



What they receive:



* A simple email notification containing:
* Time of collection
* Overview of collected waste



What they cannot do:



* Approve or acknowledge collections
* Comment or dispute within the application
* Modify or influence any data



Design principle:

Disputes or questions are handled outside the application via ECOG.



ROLE 4: POWER PLATFORM SYSTEM (IMPLICIT ROLE)



Role intent:

The system enforces business rules and automation consistently.



Main responsibilities:



* Assign EURAL codes
* Convert quantities to weights
* Perform real-time validation
* Detect and flag unusual quantities
* Log actions and changes
* Send notifications
* Generate exports



Design principle:

Errors are prevented at the moment of entry, not corrected afterwards.



CORE RULES TO ALWAYS KEEP IN MIND



* Drivers enter quantities only
* Validation happens immediately during entry
* Unusual cases are flagged by the system
* Driver submission is final
* Admins monitor and report, they do not correct
* Recycling parks are informed only
* All data must be traceable and auditable
