# Unlocked and Managed Package Metadata
## Custom Metadata Behavior
### Setup
2 Packages with a Namespace
- Unlocked
- Managed

3 Custom Metadata types created in each package
- Public
- Namespace Accessible
- Managed

3 Fields For Each Setting
- Locked
- SubscriberControlled
- DeveloperControlled

2 Metadata Records for each
- Protected
- Not Protected
### Test
1. Install first versions
   1.  Unlocked - 04t08000000HiilAAC
   2.  Managed - 04t08000000Hij5AAC
2. Change what can be changed in Subscriber Org
   1. Unlocked Public - can edit all, even delete
   2. Managed Public - can only edit Public Value
   3. Unlocked Namespace - can edit all, even delete
   4. Managed Namespace - can only edit Publi value, even delete
   5. all 4 can create new
   6. Locked Metadata cannot be seen for either package
3. Update / New Version
4. Upgrade
5. See result

## Value Set Behaviour
### Setup
1. Install first versions
   1.  Unlocked - 04t08000000HiilAAC
   2.  Managed - 04t08000000Hij5AAC
2. Change both valuesets
   1. Deactivate 1 value
   2. Delete 1 value
   3. Create new value
3. Install new version (with same original values)
4. Upgrade
5. See result
