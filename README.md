Download Link: https://assignmentchef.com/product/solved-cmsc204-project-4-a-concordance
<br>
<h2>Project 4</h2>

A <strong>concordance</strong> is an alphabetical list of the principal words used in a book or body of work, listing every instance of each word with its immediate context. Only works of special importance have had concordances prepared for them, such as the Bible, Qur’an, the works of Shakespeare, or classical Latin and Greek authors, because of the time, difficulty, and expense involved in creating a concordance in the pre-computer era.

The first Bible concordance was compiled for the Vulgate Bible by Hugh of St Cher (d.1262), who employed 500 monks to assist him.

The reconstruction of the text of some of the Dead Sea Scrolls involved a concordance.

<strong>Assignment</strong>

Write a program that creates a concordance from some text. It will list all the words in alphabetic order followed by a list of line numbers where the word can be found in the text.

<strong>Academic Honesty Policy Reminder</strong> | <strong>Do your own work</strong> – each submitted project will be compared against other submissions from current and previous semesters.

<strong>Specifications</strong>

<strong>Data Element – </strong>ConcordanceDataElement

ConcordanceDataElement implements Comparable&lt;ConcordanceDataElement&gt; and consists of a String (the word) and a reference to a LinkedList&lt;Integer&gt; (list of line numbers where word occurs).  See provided Javadoc.

<strong>Data Structure – </strong>ConcordanceDataStructure

Implement the data structure as specified (ConcordanceDataStructureInterface).

You will be implementing a hash table with buckets.  It will be an array of linked list of ConcordanceDataElements.  The add method will take a word and a line number to be added to the data structure. If the word already exists, the line number will be added to the linked list for this word.  If the line number for the word already exists, don’t add it again to the linked list. (i.e., if Sarah was on line 5 twice, the first line 5 would be added to the linked list for Sarah, the second one would not). If the word doesn’t exist, create a ConcordanceDataElement and add it to the HashTable. Two constructors will be required, one that takes in an integer that is the estimated number of words in the text, the other is used for testing purposes.

<strong>Data Manager – </strong>ConcordanceDataManager

Implements the data manager  as specified (ConcordanceDataManagerInterface).

The data manager allows the user to create a concordance file or a concordance list (ArrayList of strings). The input is read (from a file or string) and is added to the data structure through the add method.  The add method requires a word and a line number. The line number is incremented every time a newline appears in the file or the string.  Change all words to lowercase so that Now and now are considered the same word.

<strong>Exception Classes</strong>

IOException – created and thrown when user selects an input file that cannot be read (check out the methods of File).

<strong>GUI (provided)</strong>

<ul>

 <li>User will only create a concordance file once they have entered an input file and an output file</li>

 <li>Show the text area only when the option to create from text is chosen</li>

 <li>Use a FileChooser to select the input and output files. Use a filter so that user can only select .txt files</li>

 <li>Inform the user if there is an error with the input file or the output file</li>

 <li>Use exception handling for the validity of the files</li>

 <li>If creating a concordance from text, make sure the user has entered some text in the text area. Inform user if text area is empty</li>

 <li>Display the concordance from the text in the text area</li>

 <li>Provide a way for the user to “clear” the text area</li>

</ul>

<strong>Testing</strong>

<ul>

 <li>Create a JUnit Test – ConcordanceDataManager_STUDENT_Test</li>

</ul>

<strong>Additional Details</strong>

There are two ways to create a concordance.  The first requires a document to be read from an input file, and the concordance data is written to an output file.  The second reads the input from a string and returns an ArrayList of strings that represent the concordance of the string.

<strong>Don’t include the words “the” or “and” </strong>in your concordance since they are so common. Also, <strong>do not include words that have length less than 3</strong>.  <strong>Strip out all punctuation, except apostrophes that occur in the middle of a word (i.e., let’s, we’d, etc.)</strong>

<strong>Programming Concepts</strong>

This project utilizes the following concepts:

<ul>

 <li>Hash Table</li>

 <li>Link List</li>

 <li>Hash code, buckets/chaining</li>

 <li>Exception handling</li>

 <li>File Chooser</li>

</ul>