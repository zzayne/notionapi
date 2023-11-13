# notionapi

[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/jomei/notionapi?label=go%20module)](https://github.com/zzayne/notionapi/tags)
[![Go Reference](https://pkg.go.dev/badge/github.com/zzayne/notionapi.svg)](https://pkg.go.dev/github.com/zzayne/notionapi)
[![Test](https://github.com/zzayne/notionapi/actions/workflows/test.yml/badge.svg)](https://github.com/zzayne/notionapi/actions/workflows/test.yml)

This is a Golang implementation of an API client for the [Notion API](https://developers.notion.com/).

## Supported APIs

It supports all APIs of the Notion API version `2022-06-28`.

## Installation

```bash
go getgithub.com/zzayne/notionapi
```

## Usage

First, please follow the [Getting Started Guide](https://developers.notion.com/docs/getting-started) to obtain an integration token.

### Initialization

Import this library and initialize the API client using the obtained integration token.

```go
import "github.com/zzayne/notionapi"

client := notionapi.NewClient("your_integration_token")
```

### Calling the API

You can use the methods of the initialized client to call the Notion API. Here is an example of how to retrieve a page:

```go
page, err := client.Page.Get(context.Background(), "your_page_id")
if err != nil {
    // Handle the error
}
```
