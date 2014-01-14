About
======
Malware DB is a project created to make the possibility of malware
analysis open and available to the public. Since we have found out
that almost all versions of malware are very hard to come by in a 
way which will allow analysis we have decided to gather all of them
for you in an available and safe way. 


Disclaimer
==========
Malware DB's purpose is to allow the study of malware and enable
people who are interested in malware analysis or maybe even as
a part of their job to have access to live malware, analyse the 
ways they operate and maybe even enable advanced and savvy 
people to block specific malwares within their own environment.


GPL 3
======
Malware DB - the most awesome free malware database on the air
Copyright (C) 2014, Yuval Nativ, Lahad Ludar, 5fingers

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.


Documentation and Notes
========================

# Background:
	The idea behind Malware DB it to allow it to be modular and let
	you enter more malwares of your own. Each malware should have a
	directory of it's own. 
	

# Root Files:
	The main files you see on the root folder are:
		1. index.csv - 	The main index of the malwares you have
						access to and can be searched in your 
						local folders.
		2. malware-db.py - 	The main indexing file. Use it to 
							search for malware in the index.csv
							file on the same folder. 
		3. Rebuild_CSV.sh -	Rebuilds index.csv based on the
							index.log files in all the recursive
							directories. 
							

# Directory Structure:
	Each directory is composed of 5 files:
		1. Malware files in an encrypted ZIP archive. 
		2. SHA256 sum of the 1st file. 
		3. MD5 sum of the 1st file.
		4. Password file for the archive. 
		5. index.log file for the indexer. 
		

# Structure of index.csv
	The main index.csv is the DB which you will look in to find 
	malwares indexed on your drive. We use the , charachter as
	the delimiter to our CSVs. 
	The structure is al follows:
	
	uid,location,type,name,version,author,language,date
	
		UID 	-	Determined base on the indexing process.
					Does not really have any purpose yet. 
		Location - 	The location on the drive of the malware 
					you have searched for. This and the UID
					field are automatically built on run 
					by Rebuild_CSV.sh.
		Type	-	Sorts the different types of malware there are
					So far we sort by:	Virus
										Trojans
										Botnets
										Ransomeware
										Spyware
		Name	-	Just the name of the malware.
		Version	-	Nothing to say here as well.
		Author	-	... I'm not that into documentation...
		Language -	VB/C/ASM/C++/Java or binaries (bin)
		Date	-	See 'Author' section. 
		

# Structure of index.log:
	index.log is about the only file which we cannot built 
	automatically and you will need to write it down for your
	self. 
	The structure is to be:
	
	type,name,version,author,language,date,
	
	Don't worry about the UID and Location section which are 
	not there, they will be built by Rebuild_CSV.sh while it
	collects data on the malwares. 


Bugs and Reports
================
The repository holding all files is currently 
	https://github.com/ytisf/theZoo

Stuff which are in the making:
	1. More precise searching and indexing including 
	   platform and more.
	2. We have about 400 more malwares to map and add
	3. Git update of platform and new malware. 
	4. Fix display of search.

If you have any suggenstions or malware that you have indexed
as in the documentations please send it to us to yuvaln210 [at]
your most popular mail server so we can add it for every 
one's enjoyment. 