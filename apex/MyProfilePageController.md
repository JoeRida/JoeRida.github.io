---
hide:
  - path
---

# MyProfilePageController Class

An apex class that updates portal user details. 
Guest users are never able to access this page.

## Class Diagram

```mermaid
graph TD
  MyProfilePageController["MyProfilePageController"]:::mainApexClass
  click MyProfilePageController "/objects/MyProfilePageController/"
  MyProfilePageControllerTest["MyProfilePageControllerTest"]:::apexTestClass
  click MyProfilePageControllerTest "/apex/MyProfilePageControllerTest/"


  MyProfilePageControllerTest --> MyProfilePageController


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex class that updates portal user details.
   Guest users are never able to access this page.
 */
public with sharing class MyProfilePageController {

    private User user;
    private boolean isEdit = false;

    public User getUser() {
        return user;
    }

    public MyProfilePageController() {
        user = [SELECT id, email, username, usertype, communitynickname, timezonesidkey, languagelocalekey, firstname, lastname, phone, title,
                street, city, country, postalcode, state, localesidkey, mobilephone, extension, fax, contact.email
                FROM User
                WHERE id = :UserInfo.getUserId()];
        // guest users should never be able to access this page
        if (user.usertype == 'GUEST') {
            throw new NoAccessException();
        }
    }

    public Boolean getIsEdit() {
        return isEdit;
    }

    public void edit() {
        isEdit=true;
    }

    public void save() {
        try {
            update user;
            isEdit=false;
        } catch(DmlException e) {
            ApexPages.addMessages(e);
        }
    }

    public PageReference changePassword() {
        return Page.ChangePassword;
    }

    public void cancel() {
        isEdit=false;
        user = [SELECT id, email, username, communitynickname, timezonesidkey, languagelocalekey, firstname, lastname, phone, title,
                street, city, country, postalcode, state, localesidkey, mobilephone, extension, fax, contact.email
                FROM User
                WHERE id = :UserInfo.getUserId()];
    }    
}
```

## Fields
### `user`

#### Signature
```apex
private user
```

#### Type
[User](../objects/User.md)

---

### `isEdit`

#### Signature
```apex
private isEdit
```

#### Type
boolean

## Constructors
### `MyProfilePageController()`

#### Signature
```apex
public MyProfilePageController()
```

## Methods
### `getUser()`

#### Signature
```apex
public User getUser()
```

#### Return Type
**[User](../objects/User.md)**

---

### `getIsEdit()`

#### Signature
```apex
public Boolean getIsEdit()
```

#### Return Type
**Boolean**

---

### `edit()`

#### Signature
```apex
public void edit()
```

#### Return Type
**void**

---

### `save()`

#### Signature
```apex
public void save()
```

#### Return Type
**void**

---

### `changePassword()`

#### Signature
```apex
public PageReference changePassword()
```

#### Return Type
**PageReference**

---

### `cancel()`

#### Signature
```apex
public void cancel()
```

#### Return Type
**void**