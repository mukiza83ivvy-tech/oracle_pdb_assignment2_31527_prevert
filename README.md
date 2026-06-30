

Oracle PDB Assignment II – Mukiza Prevert

Student Name: Mukiza Prevert
Student ID: 31527/2025
Course: DPR400210 – Database Programming
Assignment: Oracle Pluggable Database (PDB) Management
Submission Date: June 30, 2026

⸻

Assignment Overview

This assignment demonstrates the creation and management of Oracle Pluggable Databases (PDBs) using Oracle Database 21c Express Edition. The tasks included creating a personal PDB, creating a user inside the PDB, granting privileges, creating and deleting a temporary PDB, and verifying the configuration through Oracle Enterprise Manager (OEM).

⸻

Oracle Environment

* Oracle Database 21c Express Edition (XE)
* SQL*Plus
* Oracle Enterprise Manager (OEM)
* Windows 11

⸻

Personal PDB Information

PDB Name

mukiza_pdb_31527_2025

Username

mukiza_prevert_31527_2025

Password

YourPassword123

⸻

PDB Creation Process

The following tasks were completed:

1. Connected to Oracle as SYSDBA.
2. Created the pluggable database:

CREATE PLUGGABLE DATABASE mukiza_pdb_31527_2025
ADMIN USER admin_mukiza IDENTIFIED BY YourPassword123;

3. Opened the PDB.

ALTER PLUGGABLE DATABASE mukiza_pdb_31527_2025 OPEN;

4. Verified the PDB using:

SHOW PDBS;

5. Changed the session container to the created PDB.

ALTER SESSION SET CONTAINER = mukiza_pdb_31527_2025;

⸻

User Creation Process

A dedicated user was created within the PDB.

CREATE USER mukiza_prevert_31527_2025
IDENTIFIED BY YourPassword123;

Privileges were granted:

GRANT CREATE SESSION, CREATE TABLE, RESOURCE
TO mukiza_prevert_31527_2025;

⸻

Temporary PDB Creation and Deletion

A temporary pluggable database was created for testing purposes.

Creation

CREATE PLUGGABLE DATABASE mukiza_temp_pdb_31527_2025;

Opening

ALTER PLUGGABLE DATABASE mukiza_temp_pdb_31527_2025 OPEN;

Closing

ALTER PLUGGABLE DATABASE mukiza_temp_pdb_31527_2025 CLOSE IMMEDIATE;

Deletion

DROP PLUGGABLE DATABASE mukiza_temp_pdb_31527_2025 INCLUDING DATAFILES;

⸻

Oracle Enterprise Manager (OEM)

Oracle Enterprise Manager was used to monitor:

* Database Status
* PDB Availability
* Storage Usage
* Performance Metrics
* Database Resources

Screenshots of the OEM dashboard are included in the repository.

⸻

Challenges Encountered

Challenge 1

Error:

ORA-65012: Pluggable database already exists

Solution: Verified existing PDBs using SHOW PDBS before creating another PDB.

Challenge 2

Error:

ORA-12154: TNS could not resolve connect identifier specified

Solution: Reconnected through SQL*Plus and verified the container configuration.

Challenge 3

Error:

ORA-65019: Pluggable database already open

Solution: Confirmed the PDB status using SHOW PDBS.

⸻

Lessons Learned

Through this assignment, I learned:

* How Oracle Multitenant Architecture works.
* How to create and manage Pluggable Databases.
* How to create database users and assign privileges.
* How to use Oracle Enterprise Manager.
* How to document database administration activities using GitHub.

⸻

Repository Structure

oracle_pdb_assignment2_31527_2025_mukiza
│── README.md
│
└── screenshots
    │── pdb_creation.png
    │── pdb_open.png
    │── user_creation.png
    │── privileges.png
    │── user_login.png
    │── temporary_pdb_creation.png
    │── temporary_pdb_deletion.png
    │── oem_dashboard.png

⸻

Integrity Statement

I hereby declare that this assignment is my original work. All commands, screenshots, and documentation were produced by me as part of the Oracle Pluggable Database Assignment.

Student Name: Mukiza Prevert
Student ID: 31527/2025
Date: June 30, 2026

⸻

