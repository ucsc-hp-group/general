Swift Metadata Schema
=====================

The metadata broker maintains three schema to hold metadata regarding some 
set of accounts, containers and objects in their respective schema.

There are three crawlers which monitor the three databases for changes. When
such changes occur, the crawlers send a request to update the metadata
corresponding to the updated information detected. 

# account_metadata

* ROWID INTEGER PRIMARY KEY AUTOINCREMENT
* account_uri TEXT UNIQUE
* account_name TEXT
* account_tenant_id TEXT
* account_first_use_time TEXT DEFAULT '0'
* account_last_modified_time TEXT DEFAULT '0'
* account_last_changed_time TEXT DEFAULT '0'
* account_delete_time TEXT DEFAULT '0'
* account_last_activity_time TEXT DEFAULT '0'
* account_container_count INTEGER
* account_object_count INTEGER
* account_bytes_used INTEGER
* account_meta TEXT

# container_metadata

* ROWID INTEGER PRIMARY KEY AUTOINCREMENT
* container_uri TEXT UNIQUE
* container_name TEXT
* container_account_name TEXT
* container_create_time TEXT DEFAULT '0'
* container_last_modified_time TEXT DEFAULT '0'
* container_last_changed_time TEXT DEFAULT '0'
* container_delete_time TEXT DEFAULT '0'
* container_last_activity_time TEXT DEFAULT '0'
* container_read_permissions TEXT
* container_write_permissions TEXT
* container_sync_to TEXT
* container_sync_key TEXT
* container_versions_location TEXT
* container_object_count INTEGER
* container_bytes_used INTEGER
* container_meta TEXT

# object_metadata

* ROWID INTEGER PRIMARY KEY AUTOINCREMENT
* object_uri TEXT UNIQUE
* object_name TEXT
* object_account_name TEXT
* object_container_name TEXT
* object_location TEXT
* object_uri_create_time TEXT DEFAULT '0'
* object_last_modified_time TEXT DEFAULT '0'
* object_last_changed_time TEXT DEFAULT '0'
* object_delete_time TEXT DEFAULT '0'
* object_last_activity_time TEXT DEFAULT '0'
* object_etag_hash TEXT
* object_content_type TEXT
* object_content_length INTEGER
* object_content_encoding TEXT
* object_content_disposition TEXT
* object_content_language TEXT
* object_cache_control TEXT
* object_delete_at TEXT DEFAULT '0'
* object_manifest_type INTEGER
* object_manifest TEXT
* object_access_control_allow_origin TEXT
* object_access_control_allow_credentials TEXT
* object_access_control_expose_headers TEXT
* object_access_control_max_age TEXT
* object_access_control_allow_methods TEXT
* object_access_control_allow_headers TEXT
* object_origin TEXT
* object_access_control_request_method TEXT
* object_access_control_request_headers TEXT
* object_meta TEXT
