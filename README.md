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
4. Upgrade with same values
   1. Unlocked - 04t08000000UJSZAA4
   2. Managed - 04t08000000UJStAAO
5. See result
   1. Unlocked - all reverted back to package version
6. Upgrade with new values
   1. Managed - cannot change metadata record values of previously released version
   2. Unlocked

## Value Set Behaviour
### Test
1. Install first versions
   1.  Unlocked - 04t08000000HiilAAC
   2.  Managed - 04t08000000UJSUAA4
2. Change both valuesets
   1. Deactivate 1 value
   2. Delete 1 value
   3. Create new value
3. Install new version (with same original values)
   1. Unlocked - 04t08000000UJSZAA4 - Versioned Values are re-instated, Manual Values are not touched
   2. Managed - 04t08000000UJStAAO - Versioned Values are not touched even though they don't match anymore, Manual Values are not touched
4. Change both valuesets
   1. Deactivate 1 value
   2. Delete 1 value
   3. Create new value
5. Install new Version (with new and changed values)
   1. 

## Custom Field Moving Between Packages
### Test
1. Install First Version - 04t08000000UJSeAAO (fields created)
2. Install Update to First - 04t08000000UJTDAA4 (removes fields from package, marks deprecated in the org)
3. Install New package - 04t08000000UJT3AAO (assumes the field into the new package)
### Test Alt
1. Install First Version - 04t08000000UJSeAAO (fields created)
3. Install New package (skip step 2 from previous) - 04t08000000UJT3AAO (Fail! Cannot assume a component part of another package)
