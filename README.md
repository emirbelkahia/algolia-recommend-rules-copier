**Algolia Rules Migration Script**

> **⚠️ Note:** This functionality is now available natively in the Algolia dashboard (just a few clicks). This script remains useful for **programmatic automation** — scheduled tasks, cron jobs, CI/CD pipelines, or any workflow where you need to migrate Recommend rules automatically without manual intervention.

**Overview**
This script facilitates the migration of Algolia Recommend rules from one index/model to another within the same Algolia application. It's designed to retrieve all rules from a source index/model and push them to a target index/model.

**When to use this script:**
- Automating rule migration in CI/CD pipelines
- Scheduled synchronization between environments (staging → production)
- Bulk migrations across multiple indices
- Integration with deployment workflows

**Requirements**
- Python 3.x
- requests library

**Setup**
Install the required Python library:
pip install requests

Configure your API credentials and indices:
APPLICATION_ID = 'YourApplicationID'
API_KEY = 'YourAPIKey'
SOURCE_INDEX_NAME = 'YourSourceIndexName'
SOURCE_MODEL_NAME = 'YourSourceModelName'
TARGET_INDEX_NAME = 'YourTargetIndexName'
TARGET_MODEL_NAME = 'YourTargetModelName'

**Usage**
Execute the script to begin migration:
python migrate_rules.py

**Process**
1. Retrieve Rules: Fetch all rules from the specified source.
2. Clean Rules: Remove unnecessary metadata from the rules.
3. Push Rules: Upload the cleaned rules to the target index/model.

**Debugging**
The script includes extensive print statements to help trace the processing of data:
- Original and Cleaned Rules: Displays before and after states of rules.
- API Responses: Shows detailed responses from the Algolia API for both retrieval and upload operations.

**Note**
Ensure to replace placeholder values in the script with your actual Algolia application details and index/model names.
