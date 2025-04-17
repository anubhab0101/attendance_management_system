# Faculty Attendance Management System (Mini Project)

## Overview

This project is a console-based **Faculty Attendance Management System** written in C. It allows faculty members to:
- **Log in securely**
- **Create new attendance records**
- **View past attendance records**
- **Delete existing records**

Each faculty member has a unique ID and password, and their access is limited to their subject(s) only. Records are stored as text files in corresponding directories.

## Features

- 🧑‍🏫 Multiple user login system (faculty-specific access)
- 🗃 File handling for reading, writing, and deleting attendance records
- 📂 Directory browsing using `dirent.h`
- ⏰ Timestamp-based attendance file naming
- 📋 Simple UI with key-based navigation (`getch()`)

## Directory Structure
DSUMini/ │ ├── Stud_Db.txt # Contains student list (one per line) ├── Faculty/ │ ├── Anubhab/ │ │ └── [Attendance Files].txt │ ├── AAM_SIR/ │ ├── PPA_SIR/ │ ├── Prabhu/ │ └── Aman/

## Compilation

Make sure to use a Windows-based C compiler like Turbo C or Dev-C++ since the project uses `<conio.h>` and `getch()` functions.

''bash''
gcc Mini.c -o AttendanceSystem

Note: If compiling on Linux or Mac, you must replace conio.h, getch(), and related functions.

# Usage
Run the compiled program.

Enter your Faculty ID and Password.

Choose from the following options:

q: View attendance records

n: Create a new attendance record

z: Delete existing attendance record

x: Logout

Faculty Credentials (Hardcoded)

Faculty Name	ID	Password	Course Code
Anubhab Mohapatra	25CGUAM	am	CSE101
AAM Sir	25CGUPAA	paa	CSE102
PPA Sir	25CGUPPA	ppa	CSE103
Prabhu Sir	25CGUPP	pp	CSE104
Aman Sir	25CGUAB	ab	CSE105

# Notes
The system works with a pre-existing Stud_Db.txt containing student records.

Each record is timestamped and saved as a .txt file using the format:
DD-MM-YYYY-HH-AM/PM.txt

Temporary files are created in a temp folder during creation and are committed only after confirmation.

# Limitations

No encryption for passwords.

Heavy use of goto, which affects readability and maintainability.

Windows-specific due to conio.h.
