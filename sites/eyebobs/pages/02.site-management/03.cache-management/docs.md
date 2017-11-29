---
title: Cache Management
taxonomy:
    category: docs
---

### General concepts
- It is not recommended flushing cache without special need
- If some cache type(s) is marked as invalidated - flush only that cache type(s)
- If some specific entry was updated (CMS page or product) firstly try flushing cache for this exact entry:
    - Go to System -> Cache Management
    - In the bottom of the page in input "Purge URL in Fastly CDN." enter URL and click "Quick Purge".
    - Note: it should be the full URL, for example, https://www.eyebobs.com/why-eyebobs

### Configuration cache gets invalidated
Message in the top of admin panel regarding invalidated Configuration cache means that some store configuration option was updated.
Flushing Configuration cache should not lead to any issues, so actually you can flush it any time you see the notice.
But looks like Configuration cache gets invalidated in wrong situations, so it's not required to always flush it. If there are doubts if Configuration cache is really invalid - there is a way to check in admin actions log when store configuration was updated:
- `System > Action Log > Report`
- Sort by "Action Group" = "System Configuration"
- Do search
- If there are any recent Saves, this means configuration was updated
If configuration was updated - Configuration cache have to be flushed. There is no need to flush all the caches, it is enough to flush only Configuration. To do this:
- Select the checkbox near this cache type
- Verify Action is "Refresh" (selected by default)
- Click Submit button

### Flushing cache on CMS page changes
If some changes were done to CMS page:
- Firstly try flushing cache for this exact entry, see instructions in General Concepts section
- If it makes no effect - Purge all CMS pages, using special button "Purge all CMS pages" in `System > Cache Management`, bottom of the page
- If it makes no effect - flush Magento cache

### Flushing cache on Product changes
If product changes were done in NetSuite this changes will be pulled to Magento by connector running by cron.
[notice=warning]
Fastly cache for products automatically gets flushed for specific product URL after import from NetSuite
[/notice]
If changes are not visible on front-end, but visible in admin panel on product edit screen:
- wait some time (10 minutes should be enough if there is no big data pull/push from/to NetSuite) - Magento will rebuild index
- flush Fastly cache for specific product page by URL, see instructions in General Concepts section
- If this made no effect - than click button "Flush Magento Cache". Unfortunately Fastly not always works correct