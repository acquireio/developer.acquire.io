---
description: >-
  Welcome to Acquire developer document. This document provides a powerful web
  service API for interacting with Acquire and explains how to use API and
  Webhooks. API support Email: developer@acquire.io
---

# Acquire Developers Portal

## Welcome to Acquire Developers Hub

Welcome to the Acquire Documentation, where you'll find guides and community support to help you start working as quickly as possible!

## API Reference

​[Acquire](https://acquire.io/) is a headless support API that enables rapid experience-first all business development.

## Requirement

Acquire is built and tested to work in various web browsers. It may work in other browsers but these are not officially supported. We’ll explain the system requirements of Acquire covering requirements on the client side, agent side \(Control Panel and Agent Console\), and [requirements]() for Audio & Video Chat.

## JS API

Loading the Acquire JavaScript library provides an Acquire JavaScript object that responds to a few methods. Use our powerful, fully-documented API for client side and [agent side]() to automate some of your Acquire activities and create custom integrations with your own systems. These [JS APIs]() allow you to update users without a page refresh and interact with the widget UI. 

## IOS

Acquire for iOS, for integrating Acquire into your iOS application. Get started on integrating the [AcquireIO iOS SDK](sdk/ios/sdk-setup-guide/getting-started.md) into your native iOS app using all functionality like live chat, video/audio call, cobrowse SDK, push notification, UI setting and many customization. 

## Android

Bring real customer service to your mobile apps with ready-to-use chat widgets. In this documentation will cover embedding a mobile chat window in an Android application using [android native SDK](https://developer.acquire.io/android/getting-started).

## Webhook API

This [Webhooks API]() allows you to subscribe to changes happening in the accounts of any Acquire user that installs your integration. Webhooks are a powerful API resource that you can use to automate much of your use cases and improve your productivity.

Unlike the API resources, which represent static data that you can create, update and retrieve as needed, webhooks represent dynamic resources. You can configure them to automatically notify you when a customer has taken a particular action, such as making a purchase or replying to a conversation.

## REST API

An [Acquire RESTful API](rest-apis/oauth/authorization.md) is an application program interface \(API\) that uses HTTP requests to GET, PUT, POST and DELETE data. You can use it to retrieve and update information from your own Acquire account, or to integrate Acquire into your own product. It's completely up to you and your custom use case.

## Errors

Any request that returns an error follows a standard format. Acquire will return an array of `errors` that contains objects containing `status`, `title` and `details`.

You'll most likely receive an error if validation fails, something doesn't exist or something went wrong on our end. We return errors inline with the [JSON API specification](http://jsonapi.org/format/#error-objects).

