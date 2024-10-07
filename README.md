# NFDI4Cat Central Data Repository (Repo4Cat)

Welcome to NFDI4Cat Central Data Repository, a platform dedicated to facilitating the storage, organization, and sharing of research data from catalysis science.

https://repository.nfdi4cat.org

Below you can find the most important information about this repository.

Do you have some nice idea or we have to make something better? Please create an [issue](https://github.com/nfdi4cat/repo4cat/issues) and let us know!

Do you need a playground for any tests and experiments? Please try our [demo repository](https://github.com/nfdi4cat/repo4cat/tree/main/demo-repository) - a full functionality and already prepared training materials will help you to make the first steps!

***Repo4Cat - Let`s collect our Catalysis data together!***

## Useful links

* Repository is based on [Dataverse software](https://dataverse.org)
* Official [Dataverse documentation](https://guides.dataverse.org/en/latest/), especially:
  * [User Guide](https://guides.dataverse.org/en/latest/user/index.html)
  * [Collection management](https://guides.dataverse.org/en/latest/user/dataverse-management.html) (dataverse/dataset level)
  * [Roles and permissions](https://guides.dataverse.org/en/latest/user/dataverse-management.html#roles-permissions) (dataverse level)
  * [File management](https://guides.dataverse.org/en/latest/user/dataset-management.html) (dataset level)
 


## Accounts

**Create a personal account:**

* Use "Sign up for a Dataverse account" button on the [login page](https://repository.nfdi4cat.org/loginpage.xhtml?redirectPage=dataverse.xhtml).
* Please use your real "Given Name" and "Family Name".
* Please set "Username" as combination of **"GivenName.FamilyName"** all with *small letters without quotes*, e.g. **max.mustermann**. This approach will allow us to find each other and share information with each other on an easy way in Dataverse.
* Set a real Email address to allow Dataverse to send you notifications. Sometimes it is practical to make some filters in your mailing system to sort emails from Dataverse in a separate folder, because every creation of information will be followed by a mail.
* Please set a strong password, e.g. using some password generator or just "openssl rand -base64 18" command in Linux (you can replace "18" with other number to get different length and symbols).

**Permissions and access rights:**

In Dataverse (the repository software) permissions are controlled at the "dataverse collections" level. Note, a "dataverse collection" (often just called a "dataverse") is a folder-like structure that can store one or more datasets (which in turn contain the files to share). A dataverse can also contain other dataverses (for more, see useful links above).

* Based on the Dataverse access control system users can have different access rights (permissions) in different dataverses. Every user can create a personal "dataverse" and then decide, what other users are allowed to do with their dataverse via the "Edit -> Permissions" button.
* Access to some areas in the repository must be explicitly granted by administrators, see information below.

## Internal structure: dataverses & datasets

The NFDI4Cat Central Data Repository comes with a pre-defined internal structure.
It includes a few top-level dataverses which can be further extended by the users with (sub-)dataverses.

The structure is the following:

### [1\. Projects](https://repository.nfdi4cat.org/dataverse/projects)

1. **Scope of work:** area for collaboration in projects that involve multiple institutions.
2. **Creation of the project:** access to this dataverse must be requested from administrators (write a short message with the project name via "Contact" button there: https://repository.nfdi4cat.org/dataverse/projects . Administartors will create a new dataverse "Your Project Name" with the identifier (URL) **".../project-your-project-name"** and will set one person as a local administrator there (via special group, see "User groups" below ). This person will manage after that the access rights for this specific dataverse - who can access, what will be allowed to do, etc. (via "Edit -> Permissions" buttons).
3. **User groups:** every project must have specific user groups, which are administrated by local administrators of this dataverse (==project). Naming for the user groups - must be created from the prefix **"ug-prj-"**, group name and related role, like **"ug-prj-your-project-name-admin"** and **"ug-prj-your-project-name-curator"** with related permissions. The first group "...-admin" will be created by the repository main administrators (Support team) and one person will be added to this group - the person, who has asked about the new project. More detailed information about avaialble roles and permissions you can find above under [useful links](#useful-links).
4. **New users:** will be managed by the local administrators of the project (user group **"ug-prj-your-project-name-admin"**) via specific user groups like **"ug-prj-your-project-name-curator"** for curators or user groups with other roles (see "User groups" above).
5. **Access rights:** will be managed by the local administrators of the project (user group **"ug-prj-your-project-name-admin"**) via specific user groups (see "User groups" above).

Example: ...

### [2\. Organizations](https://repository.nfdi4cat.org/dataverse/organizations)

1. **Scope of work:** area for internal collaboration within one organizations, e.g. some institution.
2. **Creation of the organization:** see [projects](#1-projects) above. Access to this dataverse must be requested from administrators. Naming of identifier (URL) **".../organization-your-organization-name"**.
3. **User groups:** see [projects](#1-projects) above. Naming for the organizational user groups - must be created from the prefix **"ug-org-"**, organization name and related role, like **"ug-org-your-organization-name-admin"** and **"ug-org-your-organization-name-curator"** with related permissions.
4. **New users:** see [projects](#1-projects) above using specific user group prefix for organizations.
5. **Access rights:** see [projects](#1-projects) above using specific user group prefix for organizations.

Example: ...

### [3\. Personal dataverses](https://repository.nfdi4cat.org/dataverse/personal)

1. **Scope of work:** area to store user's personal dataverses to work alone or in cooperation with colleagues.
2. **Creation of the dataverse:** every user can create own dataverse. Please create your personal dataverse with an **identifier as "name-surname"** (with a minus "-" sign, it will be used in URL). Name of your dataverse can be flexible, e.g. "Name Surname".
3. **User groups:** user who has created a personal dataverse is automatically an administrator of this dataverse and that's why can create custom user groups inside of this dataverse or just invite other users without group creation. Naming of user groups is free, but is better to use some naming system like e.g. in [projects](#1-projects) above.
4. **New users:**  every user account has access to this area, no specific creations are needed.
5. **Access rights:** same access rights for every user with the role **"Dataverse Creator"**.

Example: ...

### [4\. Single publications](https://repository.nfdi4cat.org/dataverse/single-publications)

1. **Scope of work:** area for single publications (datasets), available for every researcher **independent from the project or organization**. **Important:** only datasets can be created here!
2. **Creation of the publication:** every user can create own "dataset" as a separate publication.
3. **User groups:** no user groups needed. Roles are same for every user - possibility to create own "dataset" (publication).
4. **New users:** every user account has access to this area, no specific creations are needed.
5. **Access rights:** same access rights for every user with the role **"Dataset Creator"**.

Example: ...
