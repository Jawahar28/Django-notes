# Version Control Systems and Git,Commit, Branch

# VCS (Version Control Systems) : 
    a software tool used in development to track, manage, and record changes to source code over time.

    It acts as a database, enabling teams to collaborate, compare file versions, revert to previous states, and recover from errors without manual backups.

* Key Features and Benefits of a VCS:
    1. Version History: Records who modified what, and when, allowing developers to track changes throughout a project's life.
    2. Collaboration: Enables multiple developers to work simultaneously on a shared codebase, often using branches to work in isolation before merging changes.
    3. Reversion and Safety: Allows restoring individual files or the entire project to a previous state if a mistake is made or a bug is introduced.
    4. Backup and Recovery: Provides a secure, central repository (or distributed repositories) for code, preventing data loss.
    5. Branching and Merging: Facilitates the creation of separate lines of development to work on new features without disrupting the main codebase. 

* There are two types of VCS:
    1. Centralized
    2. Distrubuted 

* Centralized VCS : 
    Use a single, central server to manage all file   versions, which is efficient for handling large, binary files.

    This is not prioritised because of :
        a. Conflict Issues : It allows multiple users to access and modify/ write at same time which results in conflicting entire datbase.

        b. SPOF(Single Point of Failure) : If one users deletes the database unknowingly, the entire database will get erased.

* Majority of users prefer DVCS only.
* Distributed VCS:
    Every developer has a full copy of the project history, offering better speed, offline capability, and flexibility, with Git being the most popular example. 


# GIT and GITHUB :

* GIT : It is a version control system that manages multiple versions.
* GITHUB : It is sort of Cloud storage where we store the files of versions.

* The Core concept of GIT is 
    1. Commit : It is the checkpoint of the source code version.

            a. Commit will have whole codebase.
            cmd : git commit -m "Message"

            b. Commits are immutable(Can't update/ delete).

            c. We can rollback the commits (Just remove the file/ unstage the changes).
            cmd: first unstaging changes : git restore --staged.
                 then git reset (old git), 

            d. We can create a new reverse commit which does exactly opposite to the current commit.(Rollback Technique).