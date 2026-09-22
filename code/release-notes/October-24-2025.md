---
title: Syncfusion Code Studio Release Notes - October 24, 2025
Description: Bug fixes for AI Assistant parsing, GPT-5 parameter handling, and improvements to Credit Token Usage API in Code Studio.
platform: syncfusion-code-studio
---


# Release Updates - October 24, 2025

## Breaking Changes
 
### Credit Token Usage API Update
- We have refined the Credit Token Usage API to prevent excessive or looping API calls that previously caused unexpected server load.
 
## Bug Fixes
 
### “Failed to Parse Assistant” Issue Resolved
- Fixed the issue where users encountered parsing errors while interacting with the AI Assistant. This update ensures smooth message processing and reliable responses.

### GPT-5 ‘reasoning’ Parameter Error (Status Code 400)
- Fixed the issue where GPT-5 model requests returned 400 Unknown parameter: 'reasoning'.