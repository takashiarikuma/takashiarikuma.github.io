---
layout: post
title: "Create a Struct from a Table"
date: 2023-10-23
last_modified_at: false
tags: DataFlex
image:
  path: /assets/images/dataflex_studio_faded.jpg.1356x526.2.jpg
---

![DataFlex](/assets/images/DataFlex.png){: .left}

Structs in DataFlex can created simple. As example:

{% highlight DataFlex %}

Struct tWebAppServerProps
    String  Key
    Date    CreateDate
    String  CreateTime
    Date    ExpiresDate
    String  ExpiresTime
    Integer Locked
    Date    LockedDate
    String  LockedTime
    Integer Page
    Integer Pages
    String  Data
End_Struct

{% endhighlight %}

It's simple. Right?
But what if you have to create a structure for a table with many columns?
DataFlex incorporate a Query Tester that allows to script SQL queries like in Microsoft SQL Server Management Studio and generates the Struct automatically.

1. First open the Query Tester.
2. Write the SQL query for a requested table.
3. Then press Struct generator that creates the follow:
{% highlight DataFlex %}

Struct tWebAppSession
    { Name="SessionKey" }
    String  sSessionKey
    { Name="CreateDate" }
    Date    dCreateDate
    { Name="CreateTime" }
    String  sCreateTime
    { Name="LastAccessDate" }
    Date    dLastAccessDate
    { Name="LastAccessTime" }
    String  sLastAccessTime
    { Name="UseCount" }
    Integer iUseCount
    { Name="RemoteAddress" }
    String  sRemoteAddress
    { Name="LoginName" }
    String  sLoginName
    { Name="Active" }
    String  sActive
End_Struct

{% endhighlight %}
or disabling Use type prefix:
{% highlight DataFlex %}

Struct tWebAppSession
    String  SessionKey
    Date    CreateDate
    String  CreateTime
    Date    LastAccessDate
    String  LastAccessTime
    Integer UseCount
    String  RemoteAddress
    String  LoginName
    String  Active
End_Struct

{% endhighlight %}
