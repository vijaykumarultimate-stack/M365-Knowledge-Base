# SharePoint Permission Inheritance

## Overview

Permission inheritance is one of the core security concepts in SharePoint Online.

By default, permissions are inherited from the parent object.

Inheritance follows this hierarchy:

Site Collection
└── Site
    └── Library
        └── Folder
            └── File

Each child object inherits permissions unless inheritance is broken.

---

## Default Behavior

- Sites inherit from the Site Collection.
- Libraries inherit from the Site.
- Folders inherit from the Library.
- Files inherit from the Folder.

---

## Breaking Permission Inheritance

Permission inheritance can be stopped at:

- Site
- Library
- Folder
- File

After inheritance is broken:

- The object receives unique permissions.
- Permissions can be modified independently.

---

## Best Practices

- Keep unique permissions to a minimum.
- Prefer SharePoint Groups instead of assigning permissions directly to users.
- Use inheritance wherever possible.
- Regularly review unique permissions.

---

## Common Issues

### Users cannot access documents

Possible causes:

- Broken inheritance
- Missing group membership
- Incorrect permission level

### Users have unexpected access

Possible causes:

- Member of another SharePoint group
- Permission granted at parent site
- Multiple permission assignments

---

## Troubleshooting Checklist

- Check Site Permissions
- Verify Library Permissions
- Verify Folder Permissions
- Check File Permissions
- Review SharePoint Groups
- Use "Check Permissions" to validate user access

---

## References

- Microsoft Learn – SharePoint permissions
- Microsoft Learn – Permission levels
