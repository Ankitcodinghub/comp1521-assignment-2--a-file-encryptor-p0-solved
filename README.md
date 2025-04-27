# comp1521-assignment-2--a-file-encryptor-p0-solved
**TO GET THIS SOLUTION VISIT:** [COMP1521 Assignment 2- a file encryptor P0 Solved](https://www.ankitcodinghub.com/product/comp1521-assignment-2-a-file-encryptor-p0-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124476&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP1521 Assignment 2- a file encryptor P0 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Contents

Aims

Introduction

Getting Started

Reference Implementation

Your Tasks

Subset 0: File and directory commands

Subset 1: XOR encryption

Subset 2: Directory traversal

Subset 3: ECB encryption

Subset 4: Cipher block chaining encryption

Testing

Assumptions and Clarifications

Assessment

Testing

Submission

Assessment Scheme Assignment Project Exam Help

Intermediate Versions of Work

Change Log

Aims

to improve your understanding of filesystem objects to give you experience writing C code to manipulate binary files to further experience practical uses of bitwise operations to give you experience writing a relevant low-level data manipulation program in C

Introduction

Your task in this assignment is to write tide, a terribly insecure single-file encryption/decryption tool. Throughout this assignment, you will explore some basic filesystem operations, as well as implement several rudimentary encryption algorithms.

Encryption is the process of converting information into an obscured format, which can (in theory), only be converted back into useful information by an authorized party who knows the encryption process and key. Encryption is an incredibly useful tool, and is the reason why the internet can function in the way it does, with sensitive information freely transmitted across it.

File encryption is particularly useful to safeguard data in the case that it is stolen. Encrypting your files could prevent someone from being able to access your photos in the event that your laptop gets stolen.

In this assignment, you will implement three different algorithms for file encryption: XOR (eXclusive OR), ECB (Electronic Code Book) and CBC (Cipher Block Chaining). Each of these algorithms function slightly differently, but all work towards the same purpose of obscuring information, that can only be correctly interpreted by an authorised party.

XOR encryption works by employing the bitwise XOR operation on every bit of some given data. A key, which when broken up into it’s constituent bits, expanded to much the length of the data being encrypted. The XOR operation is then employed between these two bitstreams to yield the encrypted data. This encrypted data can be decrypted only by re-running the same XOR operation with the same key. In tide, standalone XOR encryption will only employ the the single-byte key 0xA9 .

ECB encryption works by bit-shifting data by the amount specified by some key (a password). Each character in a ‘block’ of the input data is shifted by the value of the character in the corresponding position within the password. The encrypted data can be decrypted only by shifting it back by the value of the corresponding position within the password. In tide, passwords

Contents

Aims

Introduction Getting Started tide Examples Your Tasks

Subset 0: File and directory commands

Subset 1: XOR encryption

Subset 2: Directory Traversal

Subset 3:

Electronic

Codebook

Subset 4: Cipher

Block Chaining (Challenge!)

Testing

Assumptions and

Clarifications

Assessment

will be a fixed length of 16 characters.

CBC encryption is different from the above two algorithms as each block of the encrypted data contributes to the encryption of the next block. We will combine both XOR encryption and ECB encryption to develop an encryption algorithm where it is significantly harder for an unauthorised party to read our encrypted data by guessing our password.

However, before all of this, tide needs to be able to function as a basic standalone program. As such, we will implement several filesystem manipulation operations. You will also implement two different methods of searching for files, which will make the user’s life easier in finding what they might need to encrypt.

Getting Started

Create a new directory for this assignment called tide , change to this directory, and fetch the provided code by running these commands:

$ mkdir -m 700 tide

$ cd tide

$ 1521 fetch tide

If you’re not working at CSE, you can download the provided files as a zip file or a tar file.

This will get you tide.c , which contains code to start the assignment. As provided, it will compile and run, but lacks any real functionality:

$ make dcc -Wall -Werror main.c tide.c -o tide

$ ./tide

Welcome to tide! To see what commands are available, type help. tide&gt; help help (h) Prints this help message pwd (p) Prints the current directory chdir directory (cd) Changes the current directory

list (ls) Lists the contents of the current directoryAssignment Project Exam Help test-encryptable filename (t) Tests if a file can be encrypted xor-contents filename (x) Encrypts a file with simple XOR encrypt-ecb filename (ee) Encrypts a file with ECB

from a file encrypt-cbc filename (ec) Encrypts a file with CBC decrypt-cbc filename (dc) Decrypts a file with CBC quit (q) Quits the program tide&gt; q

Thanks for using tide. Have a nice day!

However, tide.c also contains some provided functions to make your task easier. For example, the sort_strings function will sort an array of strings into alphabetical order in-place. You should read through the provided code in this file before you begin work on this assignment.

Reference implementation

A reference implementation is a common, efficient, and effective method to provide or define an operational specification; and it’s something you will likely work with after you leave UNSW.

We’ve provided a reference implementation, 1521 tide , which you can use to find the correct outputs and behaviours for any input:

tide also has a colored mode, to make it a bit nicer to use.

$ 1521 tide –colors Welcome to tide!

To see what commands are available, type help. tide&gt; q

Thanks for using tide. Have a nice day!

(as tends to be the convention in computing, we use the Americanised spelling of colour here.)

Every concrete example shown below is runnable using the reference implementation. Your goal is to make your program run just as the reference implementation does, with identical output and behaviour.

Where any aspect of this assignment is unAssignment Project Exam Helpdefined in this specification, you should match the behaviour exhibited by the reference implementation. Discovering and matching the reference implementation’s behaviour is deliberately a part of this assignment.

$ 1521 tide

Welcome to tide! To see what commands are available, type help. tide&gt; help help (h) Prints this help message pwd (p) Prints the current directory chdir directory (cd) Changes the current directory list (ls) Lists the contents of the current directory test-encryptable filename (t) Tests if a file can be encrypted xor-contents filename (x) Encrypts a file with simple XOR encrypt-ecb filename (ee) Encrypts a file with ECB decrypt-ecb filename (de) Decrypts a file with ECB search-name search-term (sn) Searches for a file by filename search-content search-size (sc) Searches for a file by its content for the provided bytes search-from-file source-file (sf) Searches for a file by its content for the provided bytes, supplied from a file encrypt-cbc filename (ec) Encrypts a file with CBC decrypt-cbc filename (dc) Decrypts a file with CBC quit (q) Quits the program tide&gt; q

Thanks for using tide. Have a nice day!

tide Examples

Additionally provided for your use is a command 1521 tide-examples .

When executed, it will create an examples directory in the current directory, and will create a number of files intended for testing, in this directory. An example of its usage follows:

$ ls commands.h escape.h main.c tide.c tide.h Makefile

$ 1521 tide-examples

$ ls commands.h escape.h main.c tide.c tide.h Makefile

$ ls examples a empty.txt forbidden lorem lorem.txt ro_dir tide_sols.txt

The autotests make heavy use of these examples, so it is recommended to run this command before manually replicating any autotest output you intend to debug.

Your Tasks

This assignment consists of five subsets. Each subset builds on the work of the previous one, and each subset is more complex than the previous one.

Assignment Project Exam Help

Listing the current directory

list_current_directory should print every file and folder in tide’s working directory, along with its permissions. The output of

this function should be sorted.

$ 1521 tide-examples

$ cd examples

$ 1521 tide

Welcome to tide! To see what commands are available, type help.

tide&gt; cd a Moving to a tide&gt; p

The current directory is: /home/z5555555/tide/examples/a tide&gt; cd .. Moving to ..

tide&gt; p

The current directory is: /home/z5555555/tide/examples tide&gt; cd this_doesnt_exist Could not change directory. tide&gt; q

Thanks for using tide. Have a nice day!

Once you have this function working correctly, your tide implementation should match the following behaviour:

$ 1521 tide-examples

$ cd examples

$ 1521 tide

Welcome to tide! To see what commands are available, type help. tide&gt; ls drwxr-xr-x . drwxr-xr-x .. drwxr-xr-x a

-rw-r–r– empty.txt drwxr-xr-x forbidden drwxr-xr-x lorem -rw-r–r– lorem.txt drwxr-xr-x ro_dir -rw-r–r– tide_sols.txt tide&gt; q

Thanks for using tide. Have a nice day!

Testing

You are expected to do your own testing. SAssignment Project Exam Helpome autotests are available to help you get started:

$ 1521 autotest tide

$ 1521 autotest tide [other .c or .h files]

Assumptions and Clarifications

Like all good programmers, you should make as few assumptions as possible.

You should avoid leaking memory wherever possible.

All supplied error messages should be printed to stdout .

You can call functions from the C standard library available by default on CSE Linux systems: including, e.g., stdio.h , stdlib.h , string.h , assert.h .

tide only has to handle ordinary files and directories. tide does not have to handle symbolic links, devices or other special files. tide will not be given directories containing symbolic links, devices or other special files. tide does not have to handle hard links.

If you need clarification on what you can and cannot use or do for this assignment, please ask in the course forum.

You are required to submit intermediate versions of your assignment. See below for details.

Your program must not require extra compile options. It must compile with dcc *.c -o tide , and it will be run with dcc when marking. Run-time errors from illegal C will cause your code to fail automarking.

If your program writes out debugging output, it will fail automarking tests. Make sure you disable debugging output before submission.

Assessment

Testing

When you think your program is working, you can use autotest to run some simple automated tests:

$ 1521 autotest tide [optionally: any extra .c or .h files]

You can also run autotests for a specific subset. For example, to run all tests from subset 0:

$ 1521 autotest tide subset0 [optionally: any extra .c or .h files]

Some tests are more complex than others. If you are failing more than one test, you are encouraged to focus on solving the first of those failing tests. To do so, you can run a specific test by giving its name to the autotest command:

$ 1521 autotest tide subset0_test1 [optionally: any extra .c or .h files]

1521 autotest will not test everything. Always do your own testing.

Whilst we can detect errors have occurred, it is often substantially harder to automatically explain what that error was. As you continue into later subsets. the errors from 1521 autotest will become less and less clear or useful. You will need to do your own debugging and analysis.

Submission

When you are finished working on the assignment, you must submit your work by running give :

$ give cs1521 ass2_tide tide.c [optionally: any extra .c or .h files]

Assignment Project Exam Help

Only your last submission will be marked.

You can check your latest submission on CSE servers with:

$ 1521 classrun check ass2_tide

You can check the files you have submitted here.

The UNSW standard late penalty for assessment is 5% per day for 5 days – this is implemented hourly for this assignment.

For example, if an assignment worth 60% was submitted half an hour late, it would be awarded 59.8%, whereas if it was submitted past 10 hours late, it would be awarded 57.8%.

Assessment Scheme

100% for performance implements all behaviour perfectly, following the spec exactly.

90% for performance completely working subsets[0-3].

80% for performance completely working subsets[0-2].

65% for performance completely working subsets[0-1].

50% for performance completely working subset0.

30-40% for performance good progress, but not passing subset0 autotests.

0% knowingly providing your work to anyone and it is subsequently submitted (by anyone).

0 FL for

COMP1521 submitting any other person’s work; this includes joint work.

academic submitting another person’s work without their consent; misconduct paying another person to do work for you.

100% for style perfect style

90% for style great style, almost all style characteristics perfect.

80% for style good style, one or two style characteristics not well done.

70% for style good style, a few style characteristics not well done.

60% for style ok style, an attempt at most style characteristics.

≤ 50% for style an attempt at style.

Assignment Project Exam Help

An indicative style rubric follows:

Whitespace (e.g. 1 + 2 instead of 1+2 )

Indentation (consistent, tabs or spaces are okay)

Line breaks (using vertical whitespace to improve readability) Documentation (8/20):

Header comment (with name and zID)

Function comments (above each function with a description)

Descriptive variable names (e.g. char *home_directory instead of char *h )

Descriptive function names (e.g. get_home_directory instead of get_hd )

Sensible commenting throughout the code (don’t comment every single line; leave comments when necessary) Elegance (5/20):

Does this code avoid redundancy? (e.g. Don’t repeat yourself!)

Are helper functions used to reduce complexity? (functions should be small and simple where possible) Are constants appropriately created and used? (magic numbers should be avoided) Portability (1/20):

Would this code be able to compile and behave as expected on other POSIX-compliant machines? (using standard libraries without platform-specific code)

Does this code make any assumptions about the endianness of the machine it is running on?

0 for asst2 knowingly providing your work to anyone and it is subsequently submitted (by anyone).

0 FL for

COMP1521 submitting any other person’s work; this includes joint work.

academic submitting another person’s work without their consent; misconduct paying another person to do work for you.

Intermediate Versions of Work

You are required to submit intermediate versions of your assignment.

Every time you work on the assignment and make some progress you should copy your work to your CSE account and submit it using the give command below. It is fine if intermediate versions do not compile or otherwise fail submission tests. Only the final submitted version of your assignment will be marked.

Assignment Conditions

Joint work is not permitted on this assignment.

Do not request help from anyone other than the teaching staff of COMP1521 — for example, in the course forum, or in help sessions.

Do not post your assignment code to the course forum. The teaching staff can view code you have recently submitted with give, or recently autotested.

Assignment submissions are routinely examined both automatically and manually for work written by others.

Rationale: this assignment is designed to develop the individual skills needed to produce an entire working program. Using code written by, or taken from, other people will stop you learning these skills. Other CSE courses focus on skills needed for working in a team.

The use of generative tools such as Github Copilot, ChatGPT, Google Bard is not permitted on this assignment.

Rationale: this assignment is designed to develop your understanding of basic concepts. Using synthesis tools will stop you learning these fundamental concepts, which will significantly impact your ability to complete future courses.

Sharing, publishing, or distributing your assignment work is not permitted.

Do not provide or show your assignment work to any other person, other than the teaching staff of COMP1521. For example, do not message your work to friends.

Do not publish your assignment code via the Internet. For example, do not place your assignment in a public GitHub repository.

For example, do not place your assignment in a public GitHub repository after this offering of COMP1521 is over.

For all enquiries, please email the class account at cs1521@cse.unsw.edu.au

CRICOS Provider 00098G
