---
layout: page
title: User Guide
---

TutorsPet is a **desktop app designed for private tutors in Singapore to manage students’ information, optimised for use via a Command Line Interface** (CLI) while still having the benefits of a Graphical User Interface (GUI). TutorsPet helps improve the efficiency and effectiveness of student management by categorising relevant contact information and keeping track of both lesson schedules and important dates.

## How to Navigate User Guide
* To get an overview of this user guide, head to [1. About](#1-about).
* To start your journey with TutorsPet, head to [2. Quick Start](#2-quick-start).
* To learn about all our features, head to [3. Features](#3-features).
* To see some exciting features in our future version, head to [4. Coming soon](#4-coming-soon).
* To see our answers to some frequently asked questions by users, head to [5. FAQ](#5-faq).
* To learn about the field formats of a student contact, head to [6.1 Field Format Summary](#61-field-format-summary).
* To get an overview of all our commands, head to [6.2 Command summary](#62-command-summary).
* To understand some terms we use, head to [7. Glossary](#7-glossary).

Feel free to check out our [Table of Contents](#table-of-contents), to get familiar with TutorsPet step by step.

You can return to Table of Contents by clicking this button <a href="#table-of-contents"> <button>Back to Table of Contents </button></a> below each section.

<div style="page-break-after: always;"></div>

## Table of Contents
* Table of Contents 
{:toc}

<div style="page-break-after: always;"></div>

--------------------------------------------------------------------------------------------------------------------
## 1. About
This document can be thought of as a manual, and a reference guide for TutorsPet. It will guide you on how to use TutorsPet and will provide complete information on each available command.
Furthermore, the guide gives information on the User Interface (UI), and the other useful features of TutorsPet. Each section of the guide can be read independently.
You can view the full list of content using the Table of Contents above. You can also use your document viewer’s Find function to quickly navigate to the content you want to know more about.

It is generally advised for new users to at least read through the [Quick Start](#2-quick-start) section to familiarise themselves with TutorsPet.

Note the following symbols and formatting used in this document:

* Mark-up: `list` <br>
  Text with this formatting indicates that it can be **typed** into the command line and executed by the application or it
  can be the **results** of the command.
* Bolded: **important** <br>
  Text with this formatting indicates that it is important information, and should be taken note of.

<div markdown="block" class="alert alert-info">

:information_source: **Notes:**<br>

* This block is used for detailing information about formatting, handling exceptional cases or special keywords used in the corresponding section.
</div>

<div markdown="block" class="alert alert-primary">
:bulb: **Tips:**

* This block is used to provide you extra details about the feature that will enable you to use it more effectively.
</div>

<div markdown="span" class="alert alert-warning">
:exclamation: **Caution:** This block is used to point out any dangerous actions that may result in the loss of data or the app crashing.
</div>

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

--------------------------------------------------------------------------------------------------------------------

## 2. Quick start

1. Ensure you have Java **11** or above installed in your Computer. If you have not installed Java before, 
   you can download it from [here](https://www.oracle.com/sg/java/technologies/javase-jdk11-downloads.html).
   
1. Download the latest **tutorspet.jar** from [here](https://github.com/AY2021S2-CS2103T-T11-3/tp/releases).

1. Copy the file to the folder you want to use as the **home folder** for your TutorsPet.

1. Double-click the file to start the app. If that does not work, open command prompt and type in
   `java -jar /path/to/jar/file`, replacing the path with the absolute or relative file paths.
   The GUI similar to the below should appear in a few seconds. Note how the app contains some sample data.<br>
   ![TutorsPet Interface](images/TutorsPetDiagram1.png)

1. Type the command in the command box and press Enter to execute it. e.g. typing **`help`** and pressing Enter will open the help window.<br>
   Some example commands you can try:

    * **`list`** : Lists all contacts.

    * **`schedule`** : Opens a window that shows the weekly schedule.

    * **`add`**`n/Alice Tan p/98765432 s/Abc Secondary School e/alicet@example.com a/John street, block 123, #01-01
      gn/Mary Tan gp/23456789` : Adds a student's contact named `Alice Tan` to TutorsPet.

    * **`delete`**`3` : Deletes the 3rd contact shown in the current list.

    * **`clear`** : Deletes all contacts and important dates.

    * **`exit`** : Exits the app.

1. Refer to the [Features](#3-features) below for details of each command.

1. All sample data in TutorsPet can be cleared at once using the `clear` command.

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

--------------------------------------------------------------------------------------------------------------------

## 3. Features

<div markdown="block" class="alert alert-info">

**:information_source: Notes about the command format:**<br>

* Words in **UPPER_CASE** are the parameters to be supplied by the user.<br>
  e.g. in `add n/NAME`, `NAME` is a parameter which can be used as `add n/John Doe`.

* Items in square brackets are optional.<br>
  e.g `n/NAME [t/SUBJECT]` can be used as `n/John Doe t/econ` or as `n/John Doe`.

* Items with `…` after them can be used multiple times including **zero times**.<br>
  e.g. `[t/SUBJECT]…​` can be used as ` ` (i.e. 0 times), `t/chem`, `t/phys t/math` etc.

* Parameters can be in any order.<br>
  e.g. if the command specifies `n/NAME p/PHONE_NUMBER`, `p/PHONE_NUMBER n/NAME` is also acceptable.

* If a parameter is expected only once in the command but you specified it multiple times, only the **last occurrence** of the parameter will be taken.<br>
  e.g. if you specify `p/12341234 p/56785678`, only `p/56785678` will be taken.

* **Extra keywords** input for commands that do not require parameters (such as `help`, `list`, `exit` and `clear`) will be **ignored**.<br>
  e.g. if the command specifies `help 123`, it will be interpreted as `help`.
</div>

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

### 3.1 General

#### 3.1.1 Clearing all entries : `clear`

Clears all entries from TutorsPet.

Format: `clear`

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

#### 3.1.2 Exiting the program : `exit`

Exits the program.

Format: `exit`

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

#### 3.1.3 Viewing help : `help`

Shows a message explaining how to access the user guide and a list of commands.

![help message](images/helpMessage.png)

Format: `help`

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

### 3.2 Student Management

#### 3.2.1 Adding a contact : `add`

Adds a student’s contact to TutorsPet.

Format: `add n/NAME p/PHONE [s/SCHOOL] [e/EMAIL] [a/ADDRESS] [gn/GUARDIAN_NAME] [gp/GUARDIAN_PHONE] [lv/LEVEL] [t/SUBJECT]…​ [le/LESSON]…​`

* `n/NAME p/PHONE` are compulsory fields that must be provided. **Phone can uniquely identify a student.** i.e. Students cannot share the same phone number, while duplicate names are allowed.
  Note that names are **case-insensitive** in TutorsPet,  e.g. `john`, `JOHN`, `John` are read as the same name.

* `[s/SCHOOL] [e/EMAIL] [a/ADDRESS] [gn/GUARDIAN_NAME] [gp/GUARDIAN_PHONE] [lv/LEVEL] [t/SUBJECT]…​ [le/LESSON]…​` are optional which can be added now with `add` command or later with `edit` command.

* Lessons should only consist of the lesson day and time e.g. `monday 1300`

* Lesson day must take on one of the values: **monday, tuesday, wednesday, thursday, friday, saturday, sunday**.

* Lesson time must be in **HHmm** format e.g. **1300**

* If the student **name** or **lesson** to be added already exists in TutorsPet, a warning prompting user's input will be shown.
  If `y` is entered, the contact will be added.
  If `n` is entered, the contact would not be added.

* Student's phone number is allowed to be the same as the guardian's number.

<div markdown="block" class="alert alert-primary">

:bulb:**Tips:** <br>
* Education levels are represented abbreviated names. Valid education levels are `pri1`, `pri2`, `pri3`, `pri4`, `pri5`, `pri6`,
    `sec1`, `sec2`, `sec3`, `sec4`, `sec5`, `jc1`, `jc2`, `grad`. Levels are case-insensitive, e.g. `jc1`, `JC1`, `Jc1` are equivalent.
    For more details, see the [Field Format Summary](#61-field-format-summary) below.

* Subjects are represented by abbreviated names. Valid names are `bio`, `chem`, `cn`, `econ`, `eng`, `geo`, `hist`, `lit`, `mal`, `math`, `phys`, `sci`, `tam`,
  which are case-insensitive, e.g. `bio`, `BIO`, `Bio` are equivalent.
  For more details, see the [Field Format Summary](#61-field-format-summary) below.
  
* Education levels and subjects available cover the usual students who are more likely to need private tuition. More options
will be explored in [Coming Soon](#4-coming-soon).
</div>

<div markdown="span" class="alert alert-warning">:exclamation: **Caution:**
TutorsPet does not corroborate the school, education level, subject and lesson fields of the student contacts
input in the app. Users will have to ensure the information they enter for these fields match up accordingly,
e.g. A student contact in ABC Primary School will probably not be in sec3, or take subjects
like chem and bio.

</div>

<div style="page-break-after: always;"></div>

Example:

`add n/John Doe p/98612341`

* After the command is entered, the new student named John Doe is added to TutorsPet.

![AfterAdd](images/DemoAfterAddCommand.png)

Other examples:

Command     | Result
----------- |---------------------------------------------------
`add n/Alice Tan p/98765432 s/Abc Secondary School e/alicet@example.com a/John street, block 123, #01-01 gn/Mary Tan gp/23456789`|adds a new student Alice Tan's details in TutorsPet
`add n/Bob Lee p/87654321 s/Def Secondary School e/bobl@example.com a/Bob street, block 321, #01-02 gn/John Lee gp/12345678 t/math le/monday 1300`| adds a new student Bob Lee's details in TutorsPet

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

#### 3.2.2 Editing a contact : `edit`

Edits an existing student in TutorsPet.

Format: `edit INDEX [n/NAME] [p/PHONE] [s/SCHOOL] [e/EMAIL] [a/ADDRESS] [gn/GUARDIAN_NAME] [gp/GUARDIAN_PHONE] [lv/LEVEL] [t/SUBJECT]…​ [le/LESSON]…​`

* Edits the student at the specified `INDEX`.

* `INDEX` refers to the index number shown in the list panel.

* At least one of the optional fields must be provided.

* When editing subjects or lessons, the existing subjects or lessons of the student will be removed, i.e. adding of subjects or lessons are not cumulative.

* You can remove all the student’s subjects and lessons by typing `t/` and `le/` respectively without specifying any subject or lesson details.

* If the student **name** or **lesson** to be edited already exists in TutorsPet, a warning prompting user's input will be shown.
  If `y` is entered, the contact will be edited.
  If `n` is entered, the contact would not be edited.
  
<div markdown="block" class="alert alert-primary">

:bulb:**Tips:** <br>
* Valid education levels are `pri1`, `pri2`, `pri3`, `pri4`, `pri5`, `pri6`,
  `sec1`, `sec2`, `sec3`, `sec4`, `sec5`, `jc1`, `jc2`, `grad`. Levels are case-insensitive, e.g. `jc1`, `JC1`, `Jc1` are equivalent.
  For more details, see the [Field Format Summary](#61-field-format-summary) below.

* Valid subject names are `bio`, `chem`, `cn`, `econ`, `eng`, `geo`, `hist`, `lit`, `mal`, `math`, `phys`, `sci`, `tam`,
  which are case-insensitive, e.g. `bio`, `BIO`, `Bio` are equivalent.
  For more details, see the [Field Format Summary](#61-field-format-summary) below.
</div>

<div style="page-break-after: always;"></div>

Example:

`edit 1 p/91234567 e/johndoe@example.com`

* After [`detail 1`](#323-viewing-a-contact-details--detail) is successfully executed, all details of Alex Yeoh are displayed.

![BeforeEdit](images/DemoBeforeEditCommand.png)

<div style="page-break-after: always;"></div>

* Then `edit` command is entered. Changes are displayed immediately.

![AfterEdit](images/DemoAfterEditCommand.png)

Other examples:

Command     | Result
----------- |---------------------------------------------------
`edit 2 n/Betsy Crower t/` | edits the name of the 2nd student to be `Betsy Crower` and clears all existing subjects.
`edit 1 le/monday 1300 le/tuesday 1400` | edits the 1st student's lesson details to `monday 1300` and `tuesday 1400`.

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

#### 3.2.3 Viewing a contact details : `detail`

Views the full details of the specified student's contact from TutorsPet.
The student's name, phone number, school, email, address, guardian name, guardian's phone number,
education level and lessons will be displayed.

Format: `detail INDEX`

* Student details of a searched list can be displayed on the details panel using this command.
* The details panel contains a lesson panel on the right to view your schedule with the specified student.

<div markdown="block" class="alert alert-primary">
:bulb:**Tips:** <br>

If student details are cut off, the windows can be resized to view more. Furthermore, the student's complete details
will be in the results display.
</div>

Example: <br>

`detail 1`

* During start up, the details panel could be empty.

![BeforeDetail](images/DemoBeforeDetailCommand.png)

* After the `detail 1` command is entered, the details of the 1st student in the list panel are displayed.

![AfterDetail](images/DemoAfterDetailCommand.png)

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

#### 3.2.4 Deleting a contact : `delete`

Permanently deletes the specified student's contact from TutorsPet.

Format: `delete INDEX`

<div markdown="block" class="alert alert-primary">

:bulb:**Tips:** <br>

* Deletes the contact at the specified `INDEX`.

* `INDEX` refers to the index number shown in the list panel.

</div>
Example: <br>

`delete 7`

* `list` followed by `delete 7` deletes the 7th student in the list.

![AfterDelete](images/DemoAfterDeleteCommand.png)

<div style="page-break-after: always;"></div>

Other examples: <br>

Command     | Result
----------- |---------------------------------------------------
`search n/Betsy` followed by `delete 1`| deletes the 1st student in the results of the `search` command

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

#### 3.2.5 Searching for a contact : `search`

Searches for a student’s contact whose details contain any of the given keywords.

Format: `search [n/KEYWORDS] [s/KEYWORDS] [t/KEYWORDS]`

Prefix | Searching Criteria
------ | -----------------
`n/`   | Name
`s/`   | School
`t/`   | Subject

* **At least one** prefix must be used.

* All 3 types of prefixes can be used **concurrently**.

* The search is case-insensitive.

* The order of the keywords does not matter. E.g. `n/Tan Alice` will match `Alice Tan`.

* Only full words will be matched. E.g. `Ta` will not match `Tan`.

* Contacts matching at least one keyword will be returned.


<div markdown="block" class="alert alert-primary">

:bulb:**Tips:** <br>

* Available subject names are `bio`, `chem`, `cn`, `econ`, `eng`, `geo`, `hist`, `math`, `phys`, `sci`, which are case-insensitive, e.g. `bio`, `BIO`, `Bio` are equivalent.

  For more details, see the [Field Format Summary](#61-field-format-summary) below.

</div>

<div style="page-break-after: always;"></div>

Example:

`search n/yeoh alex s/xyz t/cn` 

* After the `search` command is entered, a list of students whose name, school or subject contains the specified keywords
  will be displayed.

![AfterSearch](images/DemoAfterSearchCommand.png)

Other examples:

Command     | Result
----------- |---------------------------------------------------
`search n/eliza s/woodlands t/math`| displays a list of students whose name is `Eliza`, students who are studying in `woodlands primary school`, and students taking the subject `math` 
`search n/patrick lim` | displays a list of students whose names are `Patrick Lim` and `Lim Zi Ying`
`search s/woodlands` | displays a list of students studying in `woodlands primary school` and `woodlands secondary school`
`search s/raffles hwa` | displays a list of students studying in `Raffles Institution` and `Hwa chong institution`
`search t/chem` | displays a list of students taking the subject `chem`
`search t/chem math` | displays a list of students taking the subjects `chem` or `math` or both.

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

#### 3.2.6 Sorting contacts : `sort`
Sorts the student contacts by name, school, subjects or lessons.

Format: `sort PREFIX`

Prefix | Sorting Criteria | Details
------ | -----------------|--------
`n/`   | Name             |Alphabetical order
`s/`   | School           |Alphabetical order
`t/`   | Subject          |Alphabetical order of the first subjects in their lists
`le/`  | Lesson           |Chronological order of the first lessons in their lists

* There are four sorting criteria available, represented by the prefixes `n/`, `s/`, `t/`, and
  `le/`. They represent sorting by name, school, subjects or lessons respectively.

* If multiple sorting prefixes are listed out, the list will be sorted by the **last** prefix listed.

* Any extra words typed will be ignored.

Example:

`sort t/` 

* After the `sort` command is entered, the list of students displayed on the list panel will be sorted based on the 
  alphabetical order of their first subject.

![Sort Command](images/DemoSortCommand.png)

Other examples:

Command     | Result
----------- |---------------------------------------------------
`sort le/`  | sorts students based on the chronological order of their respective earliest lesson of the week
`sort n/ s/`| sorts students by the alphabetical orders of their schools, ignoring the name prefix

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

#### 3.2.7 Listing all contacts : `list`

Shows a list of all student contacts in TutorsPet. Each student's name, phone number, subjects and lessons are displayed on the list panel.

Format: `list`

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

#### 3.2.8 Increasing level of all students : `levelup`

Advances the education level of all the student contacts by one grade by default, unless the student is excluded.
This feature can perform a mass update on all the students' levels at the start of the school year.

If only some students' levels need to be changed, [edit](#322-editing-a-contact--edit) can be used instead.

Format: `levelup [ex/INDEX]`

* Students who are `sec4` will automatically advance to `sec5` when `levelup` is applied. If students
  are part of the express course, `levelup` can be applied again to advance them to `jc1`.

* Students who are `jc2` will advance to `grad` when `levelup` is applied. Students will not
  advance any further if they are `grad`.

* If the `ex/` prefix is not used, all students will advance by one education level (unless they have `grad`).
  Once `ex/` prefix is used, the index field cannot be left blank.

* `INDEX` refers to the index number shown in the list panel. Indexes are used to
  indicate students who are to be excluded from the advancement.

* Multiple indexes can be taken in. Indexes must be separated by spaces.

Example:

`levelup ex/1`

* Before the command, the 1st student is `pri5`.

![BeforeLevelUp1](images/DemoBeforeLevelUpCommand1.png)

* While the 2nd student is `sec3`.

![BeforeLevelUp2](images/DemoBeforeLevelUpCommand2.png)

* After entering the command, all students are advanced by one level, excluding the 1st student in the list (and the `grad` students).
  Entering `detail 1` will show that the level did not change for the 1st student. 

![AfterLevelUp1](images/DemoAfterLevelUpCommand1.png)

* Entering `detail 2` will show that the 2nd student is advanced to `sec4`.

![AfterLevelUp2](images/DemoAfterLevelUpCommand2.png)

<div style="page-break-after: always;"></div>

Other examples:

Command     | Result
----------- |---------------------------------------------------
`levelup`   | advances all students (except `grad` students) by one level
`levelup ex/3 4`| advances all students by one level, excluding the 3rd and 4th student in the list (and `grad` students)

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

#### 3.2.9 Decreasing level of all students : `leveldown`

Demotes the education level of all the student contacts by one grade by default, unless the student is excluded.
This feature can perform a mass undo of `levelup` or can be applied if any of the students retain a level.

If only some students' levels need to be changed, [edit](#322-editing-a-contact--edit) can be used instead.

Format: `leveldown [ex/INDEX]...`

* Students who are `jc1` will be automatically demoted to `sec5` when `leveldown` is applied. If students
  are part of the express course, `leveldown` can be applied again to demote them to `sec4`.

* Students who are `pri1` will not be demoted any further.

* If the `ex/` prefix is not used, all students will be demoted by one education level (unless they have `grad`).
  Once `ex/` prefix is used, the index field cannot be left blank.

* `INDEX` refers to the index number shown in the list panel. Indexes are used to
  indicate students who are to be excluded from the demotion.

* Multiple indexes can be taken in. Indexes must be separated by spaces.

Example:

`leveldown ex/1`

* Before the command, entering `detail 1` will show that the 1st student is `sec4`.

![BeforeLevelUp1](images/DemoBeforeLevelDownCommand1.png)

* Entering `detail 6` will show that the 6th student is `sec5`.

![BeforeLevelUp2](images/DemoBeforeLevelDownCommand2.png)

* After entering the command, all students are demoted by one level, excluding the 1st student in the list
(and `grad` students).
  Entering `detail 1` will show that the 1st student is not demoted and remains at `sec4`.
  
![AfterLevelUp1](images/DemoAfterLevelDownCommand1.png)
  
* Entering `detail 6` will show that the 6th student is demoted to `sec4`.

![AfterLevelUp2](images/DemoAfterLevelDownCommand2.png)

<div style="page-break-after: always;"></div>

Other examples:

Command     | Result
----------- |---------------------------------------------------
`leveldown`   | demotes all students (except `pri1` students) by one level
`leveldown ex/1 2`| demotes all students by one level, excluding the 1st and 2nd student in the list (and `pri1` students)

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

### 3.3 Important Date Management

#### 3.3.1 Listing all important dates : `list-date`

Shows a list of all important dates in TutorsPet.

Format: `list-date`

* After `list-date` is entered, a window containing a list of your important dates will be opened.

![list-date](images/DemoListDateCommand.png)


<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

#### 3.3.2 Adding an important date : `add-date`

Adds an important date to TutorsPet.

Format: `add-date d/DESCRIPTION dt/DETAILS`

* `DETAILS` must be in the **yyyy-mm-dd HHmm format** e.g. `2021-11-03 0800`
* Dates with the **exact same description** will be considered a duplicate and will not be added into TutorsPet.
* All dates would be accepted, including past dates. e.g. `2019-01-20`

Example: <br>

`add-date d/math exam dt/2021-11-03 0800`

* Entering the above command will add an important date with description `math exam` 
and details `2021-11-03 0800`. Then, entering the `list-date` command will display the list of updated important dates.

![add-date](images/DemoAddDateCommand.png)

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

#### 3.3.3 Deleting an important date : `delete-date`

Permanently deletes the specified important date from TutorsPet.

Format: `delete-date INDEX`

* Deletes the important date at the specified `INDEX`.

* `INDEX` refers to the index number shown in the displayed important dates list.

Example: <br>

`delete-date 2`

* Entering the above command will delete the 2nd important date in TutorsPet.
  Then, entering the `list-date` command will display the list of updated important dates.
  
![delete-date](images/DemoDeleteDateCommand.png)

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

### 3.4 Lesson Planning

#### 3.4.1 Viewing schedule : `schedule`

Shows a weekly schedule that displays lessons for the week.

Format: `schedule`

* Entering `schedule` will open up a window that displays all your lessons in this week.

![schedule popup](images/scheduleWindow.png)

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

### 3.5 Data Management

#### 3.5.1 Saving the data 

TutorsPet data is saved in the hard disk automatically after any command that changes the data. There is no need to save manually.

#### 3.5.2 Editing the data files

TutorsPet data is saved into three different JSON files: <br>
1. **\[JAR file location]/data/addressbook.json** for storing contact details.
2. **\[JAR file location]/data/datesbook.json** for storing important dates.
3. **\[JAR file location]/data/lessonbook.json** for storing lesson details.


<div markdown="block" class="alert alert-warning">
:exclamation: **Caution:**

* You are strongly discouraged from editing the files due to syncing of information between the three files.

* If your changes to the data file make its format invalid, TutorsPet will discard all data and start with an empty data file at the next run.

</div>

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

## 4. Coming soon

### 4.1 Add a subject to teach **[coming in v2.0]**

Format: `add-subject SUBJECT_NAME` <br> Currently, there is a fixed list of subjects that is available in TutorsPet,
while in v2.0, more personalised subjects can be added in.

<div style="page-break-after: always;"></div>

### 4.2 Add profile picture for each contact **[coming in v2.0]**
Format: `add-profile INDEX FILE_PATH` <br> Add a profile picture to the contact of the specified index 
by providing the file path to the picture.

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

--------------------------------------------------------------------------------------------------------------------

## 5. FAQ

**Q**: How do I transfer my data to another Computer?<br>
**A**: Install the app in the other computer, and there will be three empty data files named `addressbook.json`, `datesbook.json`, `lessonbook.json`.
Replace these three files with the corresponding files of the same names from your previous TutorsPet home folder.

**Q**: Do I have to connect to the internet to use this application? <br>
**A**: No, TutorsPet is an offline application. No internet connection is needed.

**Q**: What are the optimal display settings for this application? <br>
**A**: The default settings of almost all desktops support our application perfectly.
However, if you want to personalise your window size, the optimal display resolution is 1920 * 1080 and scaled to 150%.

**Q**: What is the maximum length for a student's name? <br>
**A**: TutorsPet allows names of up to 60 characters. See [6.1 Field Format Summary](#61-field-format-summary) for more details on the specifications of the other fields.

**Q**: Why is there such a length limit for the fields of a student, i.e. name has a character limit of 60, address has a character limit of 254, and so on? <br>
**A**: Limits are set so that users can view each student detail more effectively and have a better user experience with TutorsPet.

**Q**: Why has all my data been cleared? <br>
**A**: You could have edited the data files accidentally and corrupted the data.

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

--------------------------------------------------------------------------------------------------------------------

## 6. Summary

### 6.1 Field Format Summary

Student Contact Field   | Prefix | Optional?|Format                                          | Character Limit
------------------------| -------|--------- |------------------------------------------------|----------------
Name                    | `n/`   | N        | Contains alphanumeric characters and spaces only | 60
Phone number            | `p/`   | N        | Contains numbers only; at least 3 digits long | 15
Email                   | `e/`   | Y        | Should be in the format of **local-part@domain** e.g. `alexyeoh@gmail.com` | 254
Address                 | `a/`   | Y        | Any format | 254
Guardian's name         | `gn/`  | Y        | Contains alphanumeric characters and spaces only | 60
Guardian's phone number | `gp/`  | Y        | Contains numbers only; at least 3 digits long | 15
Education level         | `lv/`  | Y        | Fixed format: <br>Primary School: `pri1`, `pri2`, `pri3`, `pri4`, `pri5`, `pri6` <br>Secondary School: `sec1`, `sec2`, `sec3`, `sec4`, `sec5`<br>Junior College: `jc1`, `jc2`<br>Post-Junior College: `grad` | N.A.
Subject                 | `t/`   | Y        | Can have any number of inputs (including 0)<br><br>Fixed format: <br> Languages: `cn`, `eng`, `mal`, `tam`<br>Mathematics & Sciences: `bio`, `chem`, `math`, `phys`, `sci`<br>Humanities: `econ`, `geo`, `hist`, `lit`<br><br>Represents subjects Chinese, English, Malay, Tamil, Biology, Chemistry, Mathematics, Physics, Science, Economics, Geography, History, Literature in order of the above listing.| N.A.
Lesson                  | `le/`  | Y        | Can have any number of inputs (including 0)<br><br>Consist of lesson day and lesson time:<br>Lesson day: `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`, `sunday`<br>Lesson time: In **HHmm** format e.g. `1300`| N.A.

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

<div style="page-break-after: always;"></div>

### 6.2 Command summary

Action | Format, Examples
--------|------------------
**[Clear](#311-clearing-all-entries--clear)** | `clear`
**[Exit](#312-exiting-the-program--exit)** | `exit`
**[Help](#313-viewing-help--help)** | `help`
**[Add](#321-adding-a-contact--add)** | `add n/NAME p/PHONE [s/SCHOOL] [e/EMAIL] [a/ADDRESS] [gn/GUARDIAN_NAME] [gp/GUARDIAN_PHONE] [lv/LEVEL] [t/SUBJECT]…​ [le/LESSON]…​` <br> e.g., `add n/Bob Lee p/87654321 s/Def Secondary School a/Bob street, block 321, #01-02 gn/John Lee gp/12345678 t/geo`
**[Edit](#322-editing-a-contact--edit)** | `edit INDEX [n/NAME] [s/SCHOOL] [p/PHONE] [e/EMAIL] [a/ADDRESS] [gn/GUARDIAN_NAME] [gp/GUARDIAN_PHONE] [lv/LEVEL] [t/SUBJECT]…​ [le/LESSON]…​`<br> e.g.,`edit 2 n/James Lee e/jameslee@example.com`
**[Detail](#323-viewing-a-contact-details--detail)** | `detail INDEX` <br> e.g., `detail 1`
**[Delete](#324-deleting-a-contact--delete)** | `delete INDEX`<br> e.g., `delete 3`
**[Search](#325-searching-for-a-contact--search)** | `search [n/KEYWORDS] [s/KEYWORDS] [t/KEYWORDS]`<br> e.g., `search n/James Jake s/woodlands t/eng`
**[Sort](#326-sorting-contacts--sort)** | `sort PREFIX` <br> e.g., `sort [n/]`, `sort [s/]`
**[List](#327-listing-all-contacts--list)** | `list`
**[Level Up](#328-increasing-level-of-all-students--levelup)** | `levelup [ex/INDEX]` <br> e.g., `levelup`, `levelup ex/3 4`
**[Level Down](#329-decreasing-level-of-all-students--leveldown)** | `leveldown [ex/INDEX]` <br> e.g., `leveldown`, `leveldown ex/1 2`
**[List dates](#331-listing-all-important-dates--list-date)** | `list-date`
**[Add dates](#332-adding-an-important-date--add-date)** | `add-date d/DESCRIPTION dt/DETAILS`<br> e.g, `add-date d/math exam dt/2021-11-05 1300`
**[Delete dates](#333-deleting-an-important-date--delete-date)** | `delete-date INDEX`<br> e.g., `delete-date 3`
**[Schedule](#341-viewing-schedule--schedule)** | `schedule`

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>

## 7. Glossary

**Parameters:** Inputs keyed in after the command word that specify the behaviour of the command.

**Prefix**: Expressions that signal inputs of a certain field e.g. `n/` signals name field, `gp/` signals guardian's phone.

**Case-sensitivity**: Case-sensitive means that character inputs in upper case or lower case will be treated differently.
Case-insensitive means the opposite.

**Character limit**: The maximum length of characters a field of a student can take in.

<a href="#table-of-contents"> <button>Back to Table of Contents </button></a>
