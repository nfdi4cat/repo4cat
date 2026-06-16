***Repo4Cat (NFDI4Cat Central Data Repository) changelog***

# 2026-06-14: Dataverse Update, v6.2-v6.10.1

## The most important changes

#### 1. "Private URL" is now "Preview URL"
* https://guides.dataverse.org/en/6.10.1/user/dataset-management.html#preview-url-to-review-unpublished-dataset

#### 2. CVoc (Controlled Vocabulary)
* Allow ORCID and ROR to Be Used Together in Author Field
* Ready for Voc4Cat Integration. Issues: https://github.com/nfdi4cat/repo4cat/issues/8, https://github.com/nfdi4cat/repo4cat/issues/35
* https://github.com/gdcc/dataverse-external-vocab-support/blob/main/docs/readme.md
* https://github.com/gdcc/dataverse-external-vocab-support

#### 3. Licenses added
* MIT
* Apache 2.0
* The following Open Data Commons licenses have been added:
  * Open Database License (ODbL)
  * Open Data Commons Attribution License (ODC-By)
  * Open Data Commons Public Domain Dedication and License (PDDL)
* The following software license has been added:
  * European Union Public License (EUPL)
* See: https://guides.dataverse.org/en/6.10.1/installation/config.html#adding-licenses

#### 4. Citation Metadata block
* New keywordTermURI Metadata Field in the Citation Metadata Block. A new metadata field - keywordTermURI, has been added in the citation metadata block (as a fourth child field under the keyword parent field). This has been done to improve usability and to facilitate the integration of controlled vocabulary services, adding the possibility of saving the "term" and/or its associated URI.   
* New subfield "Relation Type" (IsSupplementTo for the old datasets)
* DataCite v4.5

#### 5. File Retention Period
* Retention periods make file content inaccessible after the retention period end date. This means that file previews and the ability to download files will be blocked.
* see https://guides.dataverse.org/en/6.10.1/user/dataset-management.html#retention-periods

#### 6. Improved Detection of RO-Crate Files
* Detection of mime-types based on a filename with extension and detection of the RO-Crate metadata files.
* RO-Crate metadata export format supported. See list of external exporters: https://guides.dataverse.org/en/6.10.1/installation/advanced.html#inventory-of-external-exporters 

#### 7. Pre-Publish File PID reservation!!!
* Now PID for files will be reserved, when files are created, and not like earlier only during publication!
* The big old issue is closed! - https://github.com/IQSS/dataverse/pull/7334

#### 8. ORCIDs Linked to Accounts
* Dataverse users can now link their Dataverse account with their ORCID profile. Previously, this was only available to users who logged in with ORCID. Once linked, Dataverse will automatically prepopulate their ORCID to their author metadata when they create a dataset.
* This functionality leverages Dataverse's existing support for login via ORCID, but can be turned on independently of it.
* See the User Guide: http://guides.dataverse.org/en/6.10.1/user/account.html#linking-orcid-with-your-account-profile)
* See Installation Guide: http://guides.dataverse.org/en/6.10.1/installation/orcid.html
* Issues: #7284, and #11222.

### 9. ROR (Research Organization Registry) has been added as an Author Identifier Type
* For the case when the author is an organization rather than a person. 
* Like ORCID, ROR will appear in the "Datacite" metadata export format.
* See #11075 and #11118.

#### 10. Croissant Support Is Now Built In, Slim Version Added
* Croissant is a metadata export format for machine learning datasets
* As described in the Discoverability section of the Admin Guide, Croissant is inserted into the "head" of the HTML of dataset landing pages, as requested by the Google Dataset Search team so that their tool can filter by datasets that support Croissant. In previous versions of Dataverse, when Croissant was optional and hadn't been enabled, we used the older "Schema.org JSON-LD" format in the "head". If you'd like to keep this behavior, you can use the feature flag dataverse.legacy.schemaorg-in-html-head.
* https://guides.dataverse.org/en/6.10.1/admin/discoverability.html#id6
* https://datasetsearch.research.google.com/

#### 11. Unlink Dataset Button
* A new "Unlink Dataset" button has been added to the dataset page to allow a user to unlink a dataset from a collection. To unlink a dataset the user must have permission to link the dataset.
* Additionally, the [existing API](https://guides.dataverse.org/en/6.10.1/admin/dataverses-datasets.html#unlink-a-dataset) for unlinking datasets has been updated to no longer require superuser access as the "Publish Dataset" permission is now enough. See also [#10583](https://github.com/IQSS/dataverse/issues/10583) and [#10689](https://github.com/IQSS/dataverse/issues/10689).

#### 12. Move a Dataverse Collection
* In addition to the API Move a Dataverse Collection, it is now possible for a Dataverse administrator to move a collection using the Dataverse dashboard.
* See #10304 and #11150.
* https://guides.dataverse.org/en/6.10.1/admin/dataverses-datasets.html#move-a-dataverse-collection

#### 13. Prevent Publishing of Datasets Without Files
* new "requireFilesToPublishDataset" boolean defined at the collection level.
* This boolean can be set only via API and only by a superuser.
* https://guides.dataverse.org/en/6.10.1/api/native-api.html#change-collection-attributes

#### 14. Dataset Types Can Be Linked to Metadata Blocks
* Metadata blocks, such as (e.g. "CodeMeta") can now be linked to dataset types (e.g. "software") using new superuser APIs.
* https://guides.dataverse.org/en/6.10.1/user/dataset-management.html#dataset-types

#### 15. Linking Drafts
* It is now possible to link draft datasets to other Dataverse collections.
* https://github.com/IQSS/dataverse/issues/10134

#### 16. Version Notes
* Dataverse now supports the option of adding a version note before or during the publication of a dataset.
* Whether this feature is enabled is controlled by the flag "dataverse.feature.enable-version-note"
* Version notes are shown in the user interface (in the dataset page version table), indexed (as versionNote), available via the API, and have been added to the JSON, DDI, DataCite, and OAI-ORE exports.
* The former was listed in some JSON-based API calls and exports as "versionNote" and is now "deaccessionNote", while the latter was referred to as "archiveNote" and is now "deaccessionLink".
* https://guides.dataverse.org/en/6.10.1/user/dataset-management.html#data-provenance
* https://guides.dataverse.org/en/6.10.1/api/native-api.html#dataset-version-notes
* #8431, #11068

#### 17. Curation Status Label Enhancementsq
* Adding tracking of who creates the status label and when
* Keeping a history of past statuses
* https://guides.dataverse.org/en/6.10.1/api/curation-labels.html

#### 18. Signposting Output Now Contains Links to All Dataset Metadata Export Formats
* https://guides.dataverse.org/en/6.10.1/admin/discoverability.html#signposting

#### 19. View Styled Citation ("Cite dataset" button)
* Get citation text in different formats
* https://guides.dataverse.org/en/6.10.1/user/dataset-management.html#dataset-types
* https://guides.dataverse.org/en/6.10.1/api/native-api.html#get-citation-in-other-formats
* Currently it does not provide a proper URL for the Handles. Our issue - https://github.com/IQSS/dataverse/issues/12465

#### 20. Link Permission Split Off from Publish Permission
* Linking or unlinking a dataset or dataverse now requires the new "LinkDataset" or "LinkDataverse" permissions, respectively.
* Previously, this action was covered by the "PublishDataset" or "PublishDataverse" permission
* Splitting linking into its own permission, separate from publishing, allows for more fine-grained access control, if you choose to implement custom roles that differ from the roles that Dataverse ships with.
* https://github.com/IQSS/dataverse/pull/11691

#### 21. Open OnDemand Integration (now possible)
* Open OnDemand, a web frontend to High Performance Computing (HPC) resources, has been integrated with Dataverse, allowing files to be downloaded from Dataverse installations around the world or from a specific dataset landing page if an external tool is enabled. 
* Additionally, after computation is complete, datasets can be created in Dataverse from Open OnDemand and files can be uploaded.
* https://guides.dataverse.org/en/6.10.1/admin/integrations.html#open-ondemand
* https://github.com/IQSS/dataverse/issues/11768
* https://github.com/IQSS/dataverse/pull/11769

#### 22. Globus Async Framework (now possible)
* https://guides.dataverse.org/en/6.10.1/installation/config.html#dataverse-files-globus-monitoring-server
* https://guides.dataverse.org/en/6.10.1/installation/config.html#feature-flags
* New Globus Features in rdm-integration 2.0.1
  * rdm-integration is a Dataverse external tool for synchronizing files from various source repositories into Dataverse, with support for background processing, DDI-CDI metadata generation, and high-performance Globus transfers. You can find it on the Integrations section of the Dataverse Admin Guide.
  * https://github.com/libis/rdm-integration
  * https://guides.dataverse.org/en/6.10.1/admin/integrations.html#integrations-dashboard
  * https://github.com/libis/rdm-integration#readme
  * https://github.com/libis/rdm-integration/blob/main/GLOBUS_INTEGRATION.md

#### 23. Role Assignment History Tracking
* Dataverse can now track the history of role assignments, allowing administrators to see who assigned or revoked roles, when these actions occurred, and which roles were involved.
* https://guides.dataverse.org/en/6.10.1/user/dataverse-management.html#roles-permissions

#### 24. Support for COAR Notify Relationship Announcement
* Dataverse now supports sending and receiving Linked Data Notification messages involved in the COAR Notify Relationship Announcement Workflow.
* https://www.w3.org/TR/ldn/
* https://coar-notify.net/catalogue/workflows/repository-relationship-repository/
* https://guides.dataverse.org/en/6.10.1/developers/workflows.html#coarnotifyrelationshipannouncement

#### 25. Integration with Local Contexts
* Integration with Local Contexts has been updated to support the change in their API regarding how DOIs entered as "Optional Project Information" are represented.
* https://guides.dataverse.org/en/6.10.1/installation/localcontexts.html

#### 26. Optionally Require Acknowledgment of a Disclaimer When Publishing
* When users click "Publish" on a dataset they have always seen a popup displaying various information to read before clicking "Continue"
* Now you can optionally require users to check a box in this popup to acknowledge a disclaimer that you specify through a new setting called :PublishDatasetDisclaimerText
* https://guides.dataverse.org/en/6.10.1/installation/config.html#publishdatasetdisclaimertext

#### 27. Optionally Require Embargo Reason
* It is now possible to configure Dataverse to require an embargo reason when a user creates an embargo on one or more files.
* By default, the embargo reason is optional. dataverse.feature.require-embargo-reason can be set to true to enable this feature.
* https://guides.dataverse.org/en/6.10.1/installation/config.html#dataverse-feature-require-embargo-reason

#### 28. Review Datasets
* Dataverse now supports review datasets, a type of dataset that can be used to review resources such as other datasets in the Dataverse installation itself or various resources in external data repositories. 
* APIs and a new "review" metadata block (with an "Item Reviewed" field) are in place but the UI for this feature will only be available in a future version of the new React-based Dataverse Frontend (see #876). 
* See https://guides.dataverse.org/en/6.10.1/user/dataset-management.html#review-datasets. This feature is experimental.

#### 29. API changes

* New Featured Collections: https://guides.dataverse.org/en/6.10.1/api/native-api.html#list-featured-collections-for-a-dataverse-collection

* Improved JSON Schema Validation for Datasets. See https://guides.dataverse.org/en/6.10.1/api/native-api.html#retrieve-a-dataset-json-schema-for-a-collection
  * looks like it can be used to get a common template for JSON metadata

* Search API: affiliation, parentDataverseName, image_url, etc.

* Search API: publicationStatuses

* Search Facet Information Exposed

* User Permissions on Collections
  * A new endpoint at /api/dataverses/{identifier}/userPermissions for obtaining the user permissions on a collection (dataverse) has been added.

* addDataverse Extended
  * extended to allow adding metadata blocks, input levels and facet IDs at creation time, as the Dataverse page in create mode does in JSF.

* Metadata Blocks and Display on Create

* Feature Flags Can Be Listed

* Update File Metadata API
  * A new API endpoint has been added to allow updating file metadata for one or more files in a dataset.

* Application Terms of Use Available via API
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#get-application-terms-of-use-general-terms-of-use

* Edit Dataset Metadata
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#edit-dataset-metadata
  * Removing Fields
    * The "edit dataset metadata" endpoint now allows removing fields (by sending empty values) as long as they are not required by the dataset.
  * Prevent Inconsistencies
    * A new sourceLastUpdateTime optional query parameter, which prevents inconsistencies by managing updates that may occur from other users while a dataset is being edited. 

* api/roles/userSelectable
  * A new endpoint (api/roles/userSelectable) has been implemented, which returns the appropriate roles that the calling user can use as filters when searching within their data.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#get-user-selectable-roles

* Templates API
  * POST /dataverses/{id}/templates: Creates a template for a given collection id.
  * GET /dataverses/{id}/templates: Lists the templates for a given collection id.

* File Categories API
  * A new API was added that returns a list of categories (both built-in and custom)
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#get-available-dataset-file-categories

* MyData Collection List API
  * To get a list of the collections an authenticated user can create a Dataset in.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#mydata-collection-list

* Search API: datasetCount and show_collections
  * The search index now includes datasetCount for each collection, counting published, linked, and harvested datasets.
  * https://guides.dataverse.org/en/6.10.1/api/search.html

* Listing Collections a Dataset Has Been Linked To
  * https://guides.dataverse.org/en/6.10.1/admin/dataverses-datasets.html#list-collections-that-are-linked-from-a-dataset

* Listing Collections a Collection Has Been Linked To
  * https://guides.dataverse.org/en/6.10.1/admin/dataverses-datasets.html#list-dataverse-collection-links

* Listing Metadata Blocks: isAdvancedSearchFieldType
  * https://github.com/IQSS/dataverse/issues/11614

* Notifications API: unreadCount, markAsRead, inAppNotificationFormat
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#get-all-notifications-by-user

* Edit File Metadata: Empty Values Clear Data
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#updating-file-metadata

* Get Customization File Contents API
  * to get customization file contents: analytics, homepage, header, footer, style, and logo.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#get-customization-file-contents

* Retrieving URLs to Launch External Tools
  * /api/datasets/$DATASET_ID/externalTool/$TOOL_ID/toolUrl: https://guides.dataverse.org/en/6.8/api/native-api.html#get-dataset-external-tool-url
  * /api/files/$FILE_ID/externalTool/$TOOL_ID/toolUrl: https://guides.dataverse.org/en/6.8/api/native-api.html#get-file-external-tool-url

* Storage Quotas on Individual Datasets
  * It is now possible to define storage quotas on individual datasets via API. The practical use case is for datasets in the top-level root collection. 
  * This feature does not address the use case of a user creating multiple datasets.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#storage-quotas-on-individual-datasets

* A new API endpoint has been added for retrieving a list of collections to which a given dataset or collection can be linked.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#list-dataverse-collections-to-which-a-given-dataset-or-dataverse-collection-may-be-linked

* A new API endpoint has been added to manage dataset licenses.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#update-dataset-license

* A new API endpoint has been added to manage dataset terms of access for restricted files.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#update-dataset-terms-of-access

* A new API endpoint has been added for getting and setting the metadata language of a collection.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#list-the-allowed-metadata-languages-of-a-dataverse-collection

* The "File Version Differences" and "Dataset Version Summaries" API endpoints have been improved with pagination support (with limit and offset parameters), performance improvements, and a bug fix.
  * https://guides.dataverse.org/en/6.10.1/api/native-api.html#get-versions-of-a-dataset-with-summary-of-changes

## Full list of changes
* All releases in one place: https://github.com/IQSS/dataverse/releases
* 6.3 - https://github.com/IQSS/dataverse/releases/tag/v6.3
* 6.4 - https://github.com/IQSS/dataverse/releases/tag/v6.4
* 6.5 - https://github.com/IQSS/dataverse/releases/tag/v6.5
* 6.6 - https://github.com/IQSS/dataverse/releases/tag/v6.6
* 6.7 - https://github.com/IQSS/dataverse/releases/tag/v6.7
* 6.8 - https://github.com/IQSS/dataverse/releases/tag/v6.8
* 6.9 - https://github.com/IQSS/dataverse/releases/tag/v6.9
* 6.10 (6.10.1) - https://github.com/IQSS/dataverse/releases/tag/v6.10

## API incompatible changelog
* https://guides.dataverse.org/en/6.10.1/api/changelog.html
