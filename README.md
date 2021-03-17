# Acquire Developers Portal

Welcome to Acquire developer document. This document provides a powerful web service API for interacting with Acquire and explains how to use API and Webhooks. API support Email: developer@acquire.io  
  
Acquire Developer Portal enables you to cultivate the facility of Acquire's real-time, historic conversation and communicate within your application. You'll find guides and community support to help you start working as quickly as possible!

## API Reference

​[Acquire](https://acquire.io/) is a headless support API that enables rapid experience-first all business development.

## What do you want to do?

The [Acquire](https://acquire.io/) Developer Portal is unified into four different resources. The Developer Portal can be accustomed to perform a large array of tasks.

| **Resources** | **Description** |
| :--- | :--- |
| [WIDGET](widget/overview.md) | Widget resources empower you to embed into your web page, customizations, etc... |
| SDK |  |
| [WEBHOOKS](webhook-api/introduction.md) |  |
| [REST APIs](rest-apis/introduction.md) |  |

## Errors

Any request that returns an error follows a standard format. Acquire will return an array of `errors` that contains objects containing `status`, `title` and `details`.

You'll most likely receive an error if validation fails, something doesn't exist or something went wrong on our end. We return errors inline with the [JSON API specification](http://jsonapi.org/format/#error-objects).

