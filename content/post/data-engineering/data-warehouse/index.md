---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Introduction: Data warehouse"
subtitle: "A central repository of information"
summary: "A data warehouse is constructed by integrating data from heterogeneous sources such as relational databases, flat files, etc."
authors: ["admin"]
tags: ['Data Engineering','Data warehouse']
categories: ["data-engineering"]
date: 2020-06-04T19:29:29+05:30
lastmod: 2020-06-04T19:29:29+05:30
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  placement: 1
  caption: ""
  focal_point: "Center"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
# Data Warehouse 
 A central repository of information that can be analyzed to make informed decisions. Data flows into a data warehouse from transactional systems, relational databases, and other sources.

# The core architecture boils down to some -
## Pre-Processing
 When data collection is from a number of different sources. Consistency in the format is essential before loading into a data warehouse.
 
## Staging 
 A holding area, where you put data after pre-processing (but not always) — and store it transiently until it’s processed further down the line. This is the last point where the data should be found in its raw form. (Amazon s3, Google Cloud Storage, etc are useful cloud products for staging area)

## Master
 The master area is where the incoming data takes some real shape.
 The master schema should contain correctly modeled tables, that are appropriately named. Data Cleaning is mostly done here.

## Reporting 
 Business analysts, data scientists, and decision-makers access the data through business intelligence (BI) tools, SQL clients, and other analytics applications. Businesses use reports, dashboards, and analytics tools to extract insights from their data, monitor business performance, and support decision making. These reports, dashboards, and analytics tools are powered by data warehouses. (To analyze data Amazon Redshift, Google Bigquery, etc are useful big data cloud products)

## Key Points
 Data Warehouse consists of highly curated data that serves as the central version of the truth, the data schema is designed prior DW implementation (schema-on-write). Used for batch reporting, business intelligence, and data visualization by business analyst.
