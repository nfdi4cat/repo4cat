# NFDI4Cat Central Data Repository (Repo4Cat)

Welcome to NFDI4Cat Central Data Repository, a platform dedicated to facilitating the storage, organization, and sharing of research data from catalysis science.

https://repository.nfdi4cat.org

Below you can find the most important information about this repository.

Do you have some nice idea or we have to make something better - please create an <a href="https://github.com/nfdi4cat/repo4cat/issues" target="_blank">issue</a>.

***Repo4Cat - we create repository togehter!***

# Useful links

* Repository is based on [Dataverse software](https://dataverse.org)
* Official Dataverse documentation: <a href="https://guides.dataverse.org/en/latest/" target="_blank">here</a>
  * User Guide: <a href="https://guides.dataverse.org/en/latest/user/index.html" target="_blank">here</a>
  * Collection management (dataverse/dataset level): <a href="https://guides.dataverse.org/en/latest/user/dataverse-management.html" target="_blank">here</a>
  * Roles and permissions (dataverse level): <a href="https://guides.dataverse.org/en/latest/user/dataverse-management.html#roles-permissions" target="_blank">here</a>
  * File management (dataset level): <a href="https://guides.dataverse.org/en/latest/user/dataset-management.html" target="_blank">here</a>

# Accounts

**Create a personal account:**

* use "Sign up for a Dataverse account" button on the [login page](https://repository.nfdi4cat.org/loginpage.xhtml?redirectPage=dataverse.xhtml).
* please use your real "Given Name" and "Family Name".
* please set "Username" as combination of **"GivenName.FamilyName"** all with *small letters without quotes*, e.g. **max.mustermann**. This approach will allow us to find each other and share information with each other on an easy way in Dataverse.
* set a real Email address to allow Dataverse to send you notifications. Sometimes it is practical to make some filters in your mailing system to sort emails from Dataverse in a separate folder, because every creation of information will be followed by a mail.
* please set a strong password, e.g. using some password generator or just "openssl rand -base64 18" command in Linux (you can replace "18" with other number to get different length and symbols).

**Permissions and access rights:**

* Basing on the Dataverse access control system users can have different access rights (permissions) in different "dataverses" (here "dataverse" == folder, or similar to folder structure, see useful links above). Every user can create a personal "dataverse" and then decide, what other users can do with this dataverse via the "Edit -> Permissions" button.
* Access to some areas of the repository must be explicitly granted by administrators, see information below.

# Internal structure - Dataverses/Datasets

NFDI4Cat Central Data Repository provides a concept of the internal structure. It includes some top-level dataverses which can be extended by the users.

The structure is following:

#### [1\. Projects](https://repository.nfdi4cat.org/dataverse/projects)

1. **Scope of work:** area for project-related collaboration.
2. **Creation of the project:** access to this dataverse must be asked by administrators (write a short message with the project name via "Contact" button there: https://repository.nfdi4cat.org/dataverse/projects . Administartors will create a new dataverse "Your Project Name" with the identifier (URL) **".../project-your-project-name"** and set 1 person as a local administrator there (via special group, see "User groups" below ). This person will manage after that the access rights for this specific dataverse - who can access, what will be allowed to do, etc. (via "Edit -> Permissions" buttons).
3. **User groups:** every project must have specific user groups, which is administrated via local administrators of this dataverse (==project). Naming for the user groups - must be created from the prefix **"ug-prj-"**, group name and related role, like **"ug-prj-your-project-name-admins"** and **"ug-prj-your-project-name-curators"** with related permissions. The first group "...-admins" will be created by the repository main administrators (Support team) and 1 person will be added to this group - the person, who has asked about the new project.
4. **New users:** will be managed by the local administrators of the project (user group **"ug-prj-your-project-name-admins"**) via specific user groups like **"ug-prj-your-project-name-curators"** for curators or user groups with other roles (see "User groups" above).
5. **Access rights:** will be managed by the local administrators of the project (user group **"ug-prj-your-project-name-admins"**) via specific user groups (see "User groups" above).

Example: ...

#### [2\. Organizations](https://repository.nfdi4cat.org/dataverse/organizations)

1.  **Scope of work:** area for internal collaboration within one organizations, e.g. some institution.
2.  **Creation of the organizations:** see [projects](#1-projects) above. Access to this dataverse must be asked by administrators. Naming of identifier (URL) **".../organization-your-organization-name"**.
3.  **User groups:** see [projects](#1-projects) above. Naming for the organizational user groups - must be created from the prefix **"ug-org-"**, organization name and related role, like **"ug-org-your-organization-name-admins"** and **"ug-org-your-organization-name-curators"** with related permissions.
4.  **New users:** see [projects](#1-projects) above using specific user group prefix for organizations.
5.  **Access rights:** see [projects](#1-projects) above using specific user group prefix for organizations.

Example: ...

#### [3\. Single publications](https://repository.nfdi4cat.org/dataverse/single-publications)

1.  **Scope of work:** area for single publications (datasets), available for every researcher **independent from the project or organization**. **Important:** only datasets can be created!
2.  **Creation of the publication:** Every user can create own "dataset" as a separate publication.
3.  **User groups:** no user groups needed. Roles are same for every user - possibility to create own "dataset" (publication).
4.  **New users:** every user account has access to this area, no specific creations are needed.
5.  **Access rights:** same access rights for every user with the role **"Dataset Creator"**.

Example: ...

