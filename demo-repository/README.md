# NFDI4Cat Demo Repository

Welcome to NFDI4Cat Demo Repository, a demo platform dedicated to test purposes to facilitating the storage, organization, and sharing of research data from catalysis science.

https://demo-repository.nfdi4cat.org

Below you can find the most important information about this repository.

Do you have some nice idea or we have to make something better? Please create an [issue](https://github.com/nfdi4cat/repo4cat/issues) and let us know!

## Useful links

* See [documentation of the NFDI4Cat Central Data Repository](https://github.com/nfdi4cat/repo4cat/tree/main#useful-links).

## Accounts

**Create a personal account:**

* Use "Sign up for a Dataverse account" button on the [login page](https://demo-repository.nfdi4cat.org/loginpage.xhtml?redirectPage=dataverse.xhtml).
* You are free to use your real "Given Name" and "Family Name" or some other even not-real combinations - the goal of the demo repository is to quickly get usage experience of Dataverse, explore main functions and generally became confident with the repository.
* You can set "Username" as combination of **"GivenName.FamilyName"** all with *small letters without quotes*, e.g. **max.mustermann**. This approach will allow us to find each other and share information with each other on an easy way in Dataverse.
* You can set a real Email address to allow Dataverse to send you notifications. Sometimes it is practical to make some filters in your mailing system to sort emails from Dataverse in a separate folder, because every creation of information will be followed by a mail.
* Please set a strong password, e.g. using some password generator or just "openssl rand -base64 18" command in Linux (you can replace "18" with other number to get different length and symbols).
* You can even create multiple accounts, ideally (but not necessary) with real Email addresses. It alows you to make experiments with Dataverse permissions and access rights - switching between different accounts will show you, how access mechanisms are working in real life. If you use not-real Email address please be sure, that your password is stored on a proper way (ideally in some password manager), because "forget your password" option can not work with not-real Email addresses.  

**Permissions and access rights:**

* See [permissions and access rights of the NFDI4Cat Central Data Repository](https://github.com/nfdi4cat/repo4cat/tree/main#accounts).

## Internal structure: dataverses & datasets

The NFDI4Cat Demo Repository comes with a pre-defined internal structure which is similar to the [structure of the NFDI4Cat Central Data Repository](https://github.com/nfdi4cat/repo4cat/tree/main#internal-structure-dataverses--datasets). It includes a few top-level dataverses which can be further extended by the users with (sub-)dataverses.

The structure is the following:

### [1\. Projects](https://demo-repository.nfdi4cat.org/dataverse/projects)

1. **Scope of work:** area for collaboration in projects that involve multiple institutions.
2. **Creation of the project:** please create a new dataverse "Your Project Name" with the identifier (URL) **".../your-project-name"** (please use some short form if possible) and set one person as a local administrator there (via special group, see "User groups" below ). This person will manage after that the access rights for this specific dataverse - who can access, what will be allowed to do, etc. (via "Edit -> Permissions" buttons).
3. **User groups:** every project must have specific user groups, which are administrated by local administrators of this dataverse (==project). Naming for the user groups - should be created from the prefix **"ug-"** and related role, like **"ug-admin"** and **"ug-curator"** with related permissions. Theses user groups must be created by you via "Edit -> Groups -> Creatre Group" buttons. More detailed information about avaialble roles and permissions you can find above under [useful links](#useful-links). All user groups will be visible within your dataverse and all sub-dataverses (hierarchical principle).
4. **New users:** will be managed by the local administrators of the project (user group **"ug-admin"**) via specific user groups like **"ug-curator"** for curators or user groups with other roles (see "User groups" above).
5. **Access rights:** will be managed by the local administrators of the project (user group **"ug-admin"**) via specific user groups (see "User groups" above).
6. **Sub-dataverses:** please use for the identifier (URL) a combination of the project identifier and the name of your sub-dataverse with minus "-" sign as a separator, e.g. **".../your-project-name-sub-dataverse-name"** (please use some short form if possible). 

Example: ...

### [2\. Organizations](https://demo-repository.nfdi4cat.org/dataverse/organizations)

1. **Scope of work:** area for internal collaboration within one organizations, e.g. some institution.
2. **Creation of the organization:** see [projects](#1-projects) above. Naming of identifier (URL) **".../your-organization-name"** (please use some short form if possible).
3. **User groups:** see [projects](#1-projects) above.
4. **New users:** see [projects](#1-projects) above.
5. **Access rights:** see [projects](#1-projects) above.
6. **Sub-dataverses:** see [projects](#1-projects) above.

Example: ...

### [3\. Personal dataverses](https://demo-repository.nfdi4cat.org/dataverse/personal)

1. **Scope of work:** area to store user's personal dataverses to work alone or in cooperation with colleagues.
2. **Creation of the dataverse:** every user can create own dataverse. Please create your personal dataverse with an **identifier as "name-surname"** (with a minus "-" sign, it will be used in URL). Name of your dataverse can be flexible, e.g. "Name Surname".
3. **User groups:** user who has created a personal dataverse is automatically an administrator of this dataverse and that's why can create custom user groups inside of this dataverse or just invite other users without group creation. Naming of user groups is free, but is better to use some naming system like e.g. in [projects](#1-projects) above.
4. **New users:**  every user account has access to this area, no specific creations are needed.
5. **Access rights:** same access rights for every user with the role **"Dataverse Creator"**.
6. **Sub-dataverses:** see [projects](#1-projects) above.

Example: ...

### [4\. Single publications](https://demo-repository.nfdi4cat.org/dataverse/single-publications)

1. **Scope of work:** area for single publications (datasets), available for every researcher **independent from the project or organization**. **Important:** only datasets can be created here!
2. **Creation of the publication:** every user can create own "dataset" as a separate publication.
3. **User groups:** no user groups needed. Roles are same for every user - possibility to create own "dataset" (publication).
4. **New users:** every user account has access to this area, no specific creations are needed.
5. **Access rights:** same access rights for every user with the role **"Dataset Creator"**.

Example: ...


