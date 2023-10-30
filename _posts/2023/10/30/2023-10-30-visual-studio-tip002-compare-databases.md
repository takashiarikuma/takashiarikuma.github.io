---
layout: post
title: "Visual Studio Tip #2 - Compare Databases Schemas"
date: 2023-10-30
last_modified_at: false
tags: [Visual Studio]
image:
  path: /assets/images/visual-studio-logo.webp
---

Developing a database backend application and maintaining the schema between environments can be tricky if you have no access to modify it. For example, developers have access to the development environment but can't modify the test environment. There are excellent tools from Devart and Reg-Gate, but they are not free.

Visual Studio contains a SQL Server Schema Comparison tool. Make sure have installed the SQL Server Data Tools. The option is at Tools -> SQL Server -> New Schema Comparison.

You can compare a source schema with a target schema to determine the differences between them. Then you can update the target schema to match the source schema for the database objects you select. Also, you can generate the script for an update script.
