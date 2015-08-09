# Introduction #

This project was born out of necessity because of the need to manage groups and users from a non-Windows computer (though you can use Windows if you want).  py-ad-ldap allows you to make most common operations on Active Directory objects.  It uses the python-ldap module and OpenSSL libraries, but is otherwise pure Python.

# Details #

The basic workflow for using this module is:
  1. import ad\_ldap from ad\_ldap
  1. Create an **ad\_ldap.Domain** object
  1. **Connect()** to a domain controller
  1. **Search()** using ldap filters or one of the convenience methods.  This will return **ad\_ldap.ADObject** objects, a generic class for Active Directory objects, or you can use the **object** argument to return a **User**, **Computer**, **Group**, or **Container** object which inherits from ADObject and adds more methods
  1. Read properties from the **properties** dict
  1. If you modify properties, use the **SetProperties()** method to write them back to Active Directory

Keep an eye on this page for more examples and documentation as they become available.