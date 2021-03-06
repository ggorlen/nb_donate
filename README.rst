Donate
======
.. image:: https://travis-ci.org/noisebridge/python-nb-donate.svg?branch=master
   :target: https://travis-ci.com/noisebridge/python-nb-donate.svg?branch=master
A rewrite of Noisebridge's donation site in python using Flask.


Noisebridge Donate
__________________

The donation server handles donations from people to noisebridge as well as to accounts and projects.  All donations flow to Noisebridge accounts, but they can be credited in this system to accounts, including projects.

Installation
____________

See INSTALL.md for instructions on getting the application up and running.

Model Specification
___________________

Financial data is made up of transactions.  A single transaction exchanges and amount of currency.  Transactions occur between two parties: a payer and a receiver.  While the payer and receiver are people or entities, they are modeled as accounts.  The transaction credits one parties account and debits the other simultaneously.  Two accounts are always involved in each transaction.  The collection of transacations builds the structure for double accounting.

Transactions are requested by people and they are approved by others.  In addition to two accounts, each transaction has at least two people associated with it.

Noisebridge is concerned with two top level objects;  Accounts and Projects.

Accounts have some balance of cash which increases with donations and decreases with spending.  An example is the sewing area: People donate money which is then spent on materials.  

Projects have a stated goal.  A project will have at least one account to track donations.  The progress towards the goal is just the sum of the transactions in this account.


.. image:: pics/schema.png
   :width: 60pt
