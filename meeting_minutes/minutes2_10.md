Swift Cluster Posse
===================

## 02/10/14 Meeting Minutes

HP called and we discussed our current plan for implementing the Swift metadata
server. Sam and Lincoln have approved of our plan, but have raised some
concerns with our choice of SQL server. We have been told that __SQLite__ is a less
scalable solution than more sophisticated databases such as __MySQL__. We 
agreed that using the existing swift SQL broker library will allow us to make 
our code database-agnostic.

We have also decided that __mob programming__ will be a good way to accelerate our
progress when it comes time to start the implementation workflow. 

