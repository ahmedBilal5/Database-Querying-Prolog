# Database-Querying-Prolog
* This project consists of a knowledge base which is basically a collection of facts and rules. A fact is a statement that is unconditionally true and a rule states information which is conditionally true (only true if the condition contained in the rule is true). In this case, the knowledge base consists of students of a university, their sections, their enlisted courses, course teachers, exam schedule and so forth. An example of facts in the database is:
* 
`/*Student Roll No.s and their respective sections*/
section('18I-0429','A').
section('18I-0641','A').
section('18I-0712','A').
section('18I-0745','A').
section('18I-1582','A').
section('19I-0406','A').
`

* Using the multiple types of facts present the database, we can design queries by setting rules such that multiple facts are conditially linked. The query will return either true or false depending on its truth value. An example is the following query:
*
`/*9)Whether a teacher teaches two sections of the same course*/
teachesTwoSections(X):- instructor(W,X), teaches(W,A), teaches(W,B). (Where the arguments are placeholders for our actual data)
`
* this query can be tested as:
* 
`teachesTwoSections('Hassan Mustafa'). (returns True).
`
