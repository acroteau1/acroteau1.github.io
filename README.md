# Professional Self Assessment

## Collaborating in a Team Environment

## Communicating to Stakeholders

## Data Structures and Algorithms

## Software Engineering and Databases

## Security

## Self Assessment

# Code Review
Introduction and Artifact One Review can be found [here](https://youtu.be/MNbDwvWprhM).  
Artifact Two Review can be found [here](https://youtu.be/ed9p4Jq6Fq0).

# Artifact One: Software Design and Engineering

<h4 align="center"><img src="./images/ClientServer.JPG" alt="Client-Server Relationship" height="300" width="400"></h4>

[Original Project Code](https://github.com/acroteau1/IT-365-Operating-Environments)

[Modified Project Code](https://github.com/acroteau1/Operating-Environments)

## Description

For this artifact, I worked on the “Operating Environments” project. This artifact was created during my time in IT-365: Operating Environments in late 2020. This program simulates the communication between a user’s web browser, the server, and the server response using several different classes and methods. Depending on the class, there are programs responsible for simulating a simple web server, returning header output, and mapping configuration parameters, among other functions.

```python
        try:
        # Use the default (non-validating) parser
            parser = xml.sax.make_parser()

        # Parse the Input
            parser.parse(open(configurationFile, "a"), self)
        # Write in contingency instructions for SAX parse exceptions, SAX exception, and I/O exception
        except:
            parser_config_exception = xml.sax.SAXParseException(
                "Parser Configuration Exception",
                None, self._locator)
            self.getErrorHandler().error(parser_config_exception)
            sax_exception = xml.sax.SAXException(
                "SAX Exception")
            self.getErrorHandler().error(sax_exception)
        # True I/O Exception not supported. Closest SAX exception used instead. 
            IO_exception = xml.sax.SAXNotRecognizedException(
                "SAX not recognized")
            self.getErrorHandler().error(IO_exception)
```

## Justification
This artifact is being included in the ePortfolio because it was a project I felt confident working with. I felt that the changes and additions that I made to the base code presented by my instructor when taking the course were well understood, and I was confident in dissecting the code and how it worked. I also felt it would be an appropriate choice because it showcased my skills and abilities in understanding both the original programming language and the one that it would be translated into. The artifact was improved by translating the project from Java to Python, both of which are object-oriented programming languages that would accommodate the functions of the program efficiently. I specifically dissected each file of the original program one at a time to examine what each file was doing in the overall program. From there, I researched similar classes, functions, and packages in Python and worked on re-writing the code in Python so that it would function the same way.

```python
# Create DateFormatter class. Create a variable for current date and time. Modify
# the rightNow variable into the datetime format created in the original files. Declare
# output string and set it to the SimpleDateFormat variable.
class DateFormatter():
    rightNow = datetime.now()
    SimpleDateFormat = rightNow.strftime("%d-%b-%Y %H:%M:%S")
    output = ""

    output = SimpleDateFormat
    # Print the current date and time in the specified format.
    print(output)
```

I met the course objectives that I planned to meet with this enhancement from my original plan. I specifically targeted course outcome CS-499-04, or the use of skills and techniques to apply valuable solutions and to meet the goals of production. I used my knowledge in both java and python to understand the original program, identify what to implement in the new program, and how to write it so it would function without errors. I also demonstrated understanding of the python language by working out syntax and resource errors when the code was originally compiled. Additionally, I was able to complete this work in under a week, demonstrating an ability to meet production goals and follow timelines and deadlines. As far as my outcome-coverage plans, I originally only included plans to re-work the “Configuration” file, but I was able to re-work every file from the original project instead. This will provide a more complete final artifact and a more rounded program that will function as the original project intended. 

## Reflection
In this project, I was able to utilize the Python language to re-create a program from the ground up. I learned quite a bit while I was creating and improving this project. I extensively researched XML exceptions and how they were implemented in a Python program. I also had to determine how to manipulate the “datetime” function to print the date the same way it was printed in the original program. I also had to research how to extend classes in Python, and then determine the equivalent Python class compared to the original Java class that was extended. I faced several challenges during the course of improving this artifact. I had to research several methods that I was not familiar with or had not extensively used, such as the “super()” method, writing exceptions into the code, and the try and catch methods. While these were utilized in the original project in Java, I had limited to no experience with them in Python. I also struggled with the Attributes object type from Java, which did not have a similar object type in Python, leading me to utilize a dictionary object type in its place. Finally, I also struggled to determine the appropriate packages to import in each file, as the packages in Java did not always have identical packages in Python, requiring some creativity to determine what was needed to make the program run correctly. Overall, it was a great learning experience to translate this project from Java to Python, and enhanced my understanding and comfort with both languages. 

```python
# Create test class. Declare a parser, and instruct it to write to
# the configuration XML file. Instruct program to output an error
# message in the event of an exception.
class test():
    parser = configparser.ConfigParser()
    try: 
        with open(r"./config.xml", 'w') as cf:
            parser.write(cf)
    except Exception as ce:
        print(str(ce))
        exit()
```

# Artifact Two: Algorithms and Data Structures

<h4 align="center"><img src="./images/DataStructures.jpg" alt="Data Structures" height="300" width="400"></h4>

[Original Project Code](https://github.com/acroteau1/CS-340)

[Modified Project Code](https://github.com/acroteau1/Search-and-Rescue-Dashboard)

## Description
The artifact for this milestone was the “Rescue Animal Database” project from CS-340: Advanced Programming Concepts. This artifact was created in late 2021. This project incorporated a database of animals and was primarily created for a theoretical company to be able to search through the database more efficiently. Currently, there exist files within a Jupyter Notebook that allow for automated tests to check for the ability to create, read, update, and delete data, as well as the database information. 

```Jupyter Notebook
# Create node class and initialize the node
class Node:
    def __init__(self, data):
        self.item = data
        self.next = None
        self.prev = None
    # Create doubly linked list class
    def __init__(self):
        self.start_node = None
    # Insert Element to Empty list
    def InsertToEmptyList(self, data):
        if self.start_node is None:
            new_node = Node(data)
            self.start_node = new_node
        else:
            print("The linked list is not empty.")
```

## Justification
This item was selected for inclusion within the ePortfolio because it is an item that held a lot of potential for improvement. The original project was relatively basic as far as design, implementation, and work within the database. This left a lot of room to come up with creative solutions to make the project work more fully as it was intended. In particular, this artifact allows me to showcase my skills and abilities in algorithms and data structures through the implementation of a doubly-linked list for search results, and the implementation of the tkinter method for clickable “next” and “previous” buttons. Neither of these methods were implemented in the original project nor were they utilized in any other coursework during my undergraduate studies. This demonstrates an ability to understand and implement data structures that are not familiar to me through independent research and testing. This artifact was improved through the use of the list and clickable buttons by enhancing the user experience. This improvement allows users to scroll through results without needing to return to the entire list of returned results after performing a search or performing a new search after viewing a single result. 

```Jupyter Notebook
    # Create a 'next' function
    def nextNode(self, value):
        # Define current node and create results list
        currentNode = self.head
        results = []
        # Set currentNode to the next node value
        currentNode = currentNode.next
        # Add currentNode to the results list
        while currentNode is not None:
            if currentNode.has_value(value):
                results.append(currentNode)
        # Output next node
        return results
    
    # Create a 'previous' function
    def prevNode(self, value):
        # Define current node and create results list
        currentNode = self.head
        results = []
        # Set currentNode to the prev node value
        currentNode = currentNode.prev
        # Add currentNode to the results list
        while currentNode is not None:
            if currentNode.has_value(value):
                results.append(currentNode)
        # Output prev node
        return results
```

I met the course objectives that I planned to meet with this enhancement in Module One by creating a working code that implemented the changes that were planned earlier on. In particular, I was able to create several classes that encompassed the purpose and execution of a doubly-linked list. I also needed to add a section that would filter results by animal type, and a section to search based on the selected filter. Then, I was able to call those classes at the appropriate part of the code that returned results. Finally, I was able to adjust the code to include the “next” and “previous” buttons, which referenced corresponding nodes in the doubly-linked list classes. As far as the course outcomes, I was able to meet the outcome CS-499-03 which encompasses the creation of solutions for a given problem using principles and practices of algorithms and computer science while managing design choices. Overall, I would say that outcome-coverage plans expanded based on what I had originally planned, as I realized my original files did not have a search function available, and that without that function, I would not be able to implement this data structure. 

## Reflection
During the course of improving this project, I had to learn appropriate ways to create a doubly-linked list. The first challenge I faced was in this lesson, as I realized after writing the original method that I did not have a search function available to implement the data structure within. Then came the next lesson, determining how to implement a simple search function using radio buttons. I was also able to do this successfully, and was able to create a simple search option for either dogs or cats. Next, I had to learn and implement the tkinter method to enable clickable buttons, as well as figure out the dash code that would be required to place the buttons where I wanted them on the results. The end result is a cohesive design that meets the goals of the planned artifact improvement.

```Jupyter Notebook
def dashboard_results(filter_type):
    """Filter rescue dogs based on the rescue type."""
    if filter_type == 'Dog':
        df = pd.DataFrame.from_records(shelter.filtered_rescue_dogs("Dog"))
        # Insert the resulting elements into the linked list
        df.InsertToEnd()
        # Assign node next and previous values to iterations of the results
        df.next = n.next
        df.prev = n.prev
        # Create next and previous buttons
        nextButton = Button(master, text = 'Next', command = Node.nextNode)
        button.pack()
        mainloop()
        prevButton = Button(master, text = 'Previous', command = Node.prevNode)
        button.pack()
        mainloop()
```

# Artifact Three: Databases

<h4 align="center"><img src="./images/Database.JPG" alt="Database" height="300" width="400"></h4>

[Original Project Code](https://github.com/acroteau1/CS-340)

[Modified Project Code](https://github.com/acroteau1/Search-and-Rescue-Dashboard-Enhanced)

## Description
The artifact selected for this portion of the portfolio is CS-340: Advanced Programming Concepts’ “Rescue Animal Database” project. This artifact was created in late 2021, and enhanced as an earlier portion of the ePortfolio. This project utilizes a database of animals to be searched through by a theoretical company for suitable candidates for a search-and-rescue program. So far, it has been improved to create a doubly-linked list of search results, and clickable buttons to move from one result to the next, or previous, result. 

## Justification
This item was selected for inclusion in the ePortfolio because the final version of the project used in the class still left a lot to be desired as far as functionality and potential features within the program. The final project featured a working database and dashboard, but was limited as far as search ability, display, security, and meaningful features. This artifact allows me to showcase my skills and abilities when working with databases through the implementation of triggers when performing certain actions within the database. Triggers have not been utilized previously in my undergraduate studies, demonstrating the ability to research, understand, and properly implement new concepts into my work. This artifact was improved first through the creation of methods to add a new animal to the database, edit an existing animal within the database, and delete an existing animal from the database. To address security problems with these features, I added in a check for the user type when performing these actions. Then, a table was created within the database to record the changes detected by triggers, which would insert a copy of the new animal information or record the old information of the entry. It would also record the type of change made to the entry, when the change occurred, and what user performed the change. This would be useful in creating an audit trail for the database as well as a record of previous information of entries in case a mistake is made and previous information must be restored. 

I met the Module One course objectives I planned to meet with this enhancement and more. I planned to meet CS-499-04, or the ability to utilize skills and concepts to implement solutions. I was able to create and implement functions to make changes to the database, as well as triggers to record when those changes are made and capture what those changes are in a table that can later be accessed and referenced. The code functions as intended and runs without bugs. I am also able to update my outcome-coverage plans by also touching on CS-499-05, which involves developing a security mindset in the work on my final project. I was able to do this by creating a clause that would check the permissions of the user and print an error message if they did not have the appropriate clearance to be making changes to the database. 

## Reflection
The process of enhancing and modifying the artifact taught me several lessons as well as presented several challenges. First, the process of using triggers taught me what they were, how they worked, and how to implement them into my project. I also was able to learn more about utilizing SQL to interact with the database in the process, as I first erroneously thought I would be able to program the triggers into the python code. It seems like there are some methods of doing this, but not in the way I originally planned to execute the enhancement, so I worked through several tutorials with triggers to gain confidence before implementing them into my project. This worked out well, and the SQL queries worked as intended. I was eventually able to navigate recording the user making the changes into the table capturing the change by creating and declaring a username variable, then setting the results of the user() function into that variable, and finally inserting that variable into the table for the user performing the action. Another challenge that was encountered was how to validate which users are allowed to make changes to the database. For the time being, I set a function that only a username of the main user of the database is allowed to make changes to the database. If additional users are added, they will need to either be added to the acceptable username function, or the code will need to be adjusted to specifically reference user access levels. Overall, the final product meets the intended goals of the enhancement, and opens the project up to additional opportunities for improvement and advanced functionality.
