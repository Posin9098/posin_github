# HelpBaseify REST API

Here we create a REST api for report a bug or add new bug from third party to Lean Testing site.

For add a new bug you just create an url (explain below) with parameters and hit that url and it return with a json. 

For this we want various parameter (List is below)

1. Project_id (as '**project_id**') : Id of project in which we want to add bug
2. Token (as '**token**'): Authentication toke

Rest of all lean parameters are below.
We need all required parameter and rest of all are optional.

Note: We can pass either **project_version** or **project_version_id** 

Request parameters

Name | type | Description | Required
------------ | ------------- | ------------- | -------------
title | string | Bug title | Required
status_id | integer || Required
status_id | integer || Required
project_version | string |The project version where the bug occurred. e.g. v1.1 or beta | Required
project_version_id | integer | The project version ID where the bug occurred. This parameter has precedence over project_version. | Required
project_section_id | integer || Optional
type_id | integer || Optional
reproducibility_id | integer || Optional
priority_id | integer || Optional
assigned_user_id | integer | The user ID that will be assigned to this bug | Optional
description | string || Optional
expected_results | string || Optional
steps | array | A list with the steps to reproduce the bu | Optional
platform | object | The platform details were the bug occurred (with the options shown below). | Optional
| Show child parameters
device_model | string | e.g. iPhone | Optional
