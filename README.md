LogicPull
======================================

LogicPull gives you the tools to quickly create advanced question and answer interviews for end-users. The answers are then combined with templates to produce all the documents you need. Take the [tour](https://logicpull.com/tour) to find out more about what LogicPull.

Features
--------

[LogicPull](https://www.logicpull.com/) was initially developed to save time and money creating the many legal documents needed for a court preceding. It has since expanded to handle the assembly of PDF, DocX, RTF and XML documents for any project. It is a cloud based automated document assembly service. We give you the tools to quickly create an advanced question and answer interview to be completed by an end user, which in turn creates an answer set to be combined with a template to produce documents.

* Multiple Document Formats Supported
* Create Complex Branching Logic
* Keep your Data and Documents in the Cloud
* Save Progress on Client Interviews
* Attach Custom Templates to Guided Interviews
* Preview your Work Before it Goes Live
* Send Processed Documents Automatically

Demo
----

1. Basic
   * [**Viewer**](http://demo.logicpull.com/interviews/active/3): The Résumé Builder is just one of the endless guided interviews which can be built.
   * [**Editor**](https://logicpull.com/demo/editor/2): This is the tool used to create the Resume Builder.
2. Advanced
   * [**Viewer**](http://demo.logicpull.com/interviews/active/2): Shows more of the features that LogicPull offers.
      - Nested Looping
      - Field Validation
      - Saving and resuming interviews
      - Advanced Functions
      - Popovers and embedded Youtube videos
   * [**Editor**](https://logicpull.com/demo/editor/2): The tool used to create the advanced demo.

Docs
----

* [Help](http://help.logicpull.com)

FAQ
---
* What exactly can I do with LogicPull?
  > You can collect answers to dynamic questions through a form built with our editor, then combine those answers with a template to produce PDF, RTF, XML or DocX documents.

* What are templates?
  > LogicPull uses [EJS](http://embeddedjs.com/) to combine with answer sets to produce the documents you need. Please see this [article](http://help.logicpull.com/portal/articles/working-with-templates) for more information on how to work with templates.

* Do I need a technical background to use LogicPull?
  > LogicPull tries to make it as easy as possible to create, edit, and manage guided interviews. Writing templates does require a basic understanding of how conditional logic works.

* What browsers does LogicPull support?
  >  * Google Chrome
  >  * Safari
  >  * Firefox
  >  * Opera 9.5+
  >  * Microsoft Internet Explorer 8.0+

Installation
------------

A full installation tutorial on a Ubuntu 12.04.3 64 bit server is available [here](http://help.logicpull.com/portal/articles/installation-server). To build LogicPull locally, please see this [article](http://help.logicpull.com/portal/articles/installation-local).

System Requirements 
-------------------

The minimum memory requirement for LogicPull, and all its components is 256 MiB of memory. With only the minimum amount of memory available, the interviews will take longer to process than normal, but will complete successfully. This minimum requirement is dependent on the number of users connected to the server, and the complexity of the tasks being performed.

Software Requirements
------------

[LogicPull](https://www.logicpull.com/) uses the software packages listed below in our server side tech stack. For detailed instruction on how to install LogicPull on a server, please see [here](http://help.logicpull.com/portal/articles/installation-server).

| Package | Description | License |
| --- | --- | --- |
| [MongoDB](http://www.mongodb.org/) | Database used to store all interviews, and answer sets. | AGPL |
| [nodeJS](http://nodejs.org/) | Server side JavaScript platform. | MIT |
| [stunnel](https://www.stunnel.org/index.html) | Decryption for SSL traffic. | GPL |
| [nginx](http://nginx.org/) | Server for static resources. | BSD |
| [varnish](https://www.varnish-cache.org/) | Used to cache resources. | BSD |
| [graphviz](http://www.graphviz.org/) | Open source graph visualization software, used in editor. | EPL |
| [Apache FOP](http://xmlgraphics.apache.org/fop/) | Document assembler. | Apache |

TODO
----

__Editor__ 

* Complete Validations. The following validations are not yet implemented.
  * min_date
  * max_date  
    To perform validation for these properties, use 'after logic' and check the date using dateDifference().
* Add descending order into number dropwdown in the editor
* Add drop down list of months as a default in the date field
* Create undo function
* Add a variable lookup/finder in the editor
* Select multiple nodes from graph and move
* Disallow duplicate variable field names

__Viewer__

* Allow users to change a past variable without having to go back to that question and start from there

Known Issues
------------

* The Settings button in the editor view does not work when the debug preview is running.
* Once a date is entered into the viewer, it cannot be cleared, only changed. 
* When adding question text in the editor, the 'Toggle HTML' button does not reset when the question is closed. To prevent any issues, make sure the default compiled view is visible when exiting the question. 
* Adding format in the editor may interfere with the parsers ability to recognize templates. For example, when bolding text, the editor may insert `<%<bold> someVar %></bold>`. This would prevent the parser to recognize the variable `someVar` since the `<bold>` tag was inserted in between the template tags `<% %>`. To prevent this, you can switch to 'HTML View' and move the bold tag to outside the template tag. This is a rare bug that seems to come up only when re-bolding text.

Possible Improvements
---------------------
* Replace ejs templating engine with more robust solution 
* Replace apache FOP with [XMLMind](http://www.xmlmind.com/foconverter/) 
* Use mardown instead of wysihtml5 in the editor

License
-------

The platform code for LogicPull is released under the Affero General Public License. This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Affero General Public License for more details. You should have received a copy of the GNU Affero General Public License along with this program.  If not, see <http://www.gnu.org/licenses/>.

Author
------

[@ChrisZieba](http://chriszieba.com)

Copyright
---------

Copyright 2015 Chris Zieba
