---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>

includes:
  - rest
  - errors

search: true
---

# Introduction

Welcome to LazyRestApi. LazyRestApi is a free tool that allows you to create APIs, create custom data and perform operations using Fire RESTFUL. The goal of LazyRestApi is used as a prototyping / testing / tool for learning.

# Authentication

> To authorize, use this code:


```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "API-Token: meowmeowmeow"
```


> Make sure to replace `meowmeowmeow` with your API key.

To use LazyRestApi does not have to do Authentication, but you can also enable authentication using `API-Token` for each of your projects.

If you enable authentication you must add the `API-Token` header in the form of the project token you can.

`Base-URL: <your_project_url>`

`API-Token: <secret-key>`

<aside class="notice">
You must replace <code>secret-key</code> with your personal API key.
</aside>



