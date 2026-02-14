# 🚀 LinkedIn Post Automation Engine

![Build](https://img.shields.io/badge/build-active-success)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![n8n](https://img.shields.io/badge/automation-n8n-orange) ![AI
Powered](https://img.shields.io/badge/AI-powered-purple)

An AI-powered LinkedIn content automation system built with **n8n**,
**Google Sheets**, and **LLM models** to streamline content generation,
approval workflows, and automatic publishing.

This project transforms manual LinkedIn posting into a structured,
scalable, and production-ready automation pipeline.

------------------------------------------------------------------------

## 📌 Overview

The LinkedIn Post Automation Engine enables:

-   Automated LinkedIn post generation using AI\
-   Structured content storage in Google Sheets\
-   Precision-based modification system\
-   Manual approval control\
-   Automatic LinkedIn publishing\
-   Post-status tracking

Designed for creators, developers, startups, and personal brands who
want a repeatable, scalable LinkedIn content workflow.

------------------------------------------------------------------------

## 🏗️ System Architecture

### High-Level Workflow

    Google Sheets Trigger
            ↓
    AI Post Generator (LLM)
            ↓
    Store Initial Output
            ↓
    Modification Engine
            ↓
    Approval Gate (IF Logic)
            ↓
    Publish to LinkedIn
            ↓
    Update Status in Sheet

### Core Components

-   **n8n** -- Workflow automation engine\
-   **Groq LLM / Gemini Model** -- AI content generation\
-   **Google Sheets API** -- Content management\
-   **LinkedIn API** -- Automated publishing\
-   **Conditional Logic & Merge Nodes** -- Workflow orchestration

------------------------------------------------------------------------

## 📊 Google Sheet Schema

  Column                Description
  --------------------- ------------------------------
  PROJECT DESCRIPTION   Base project information
  GITHUB LINKS          Repository reference
  IMAGE LINKS           Media attachment link
  OUTPUT                Initial AI-generated content
  MODIFICATIONS         Requested edits
  MODIFIED OUTPUT       Final approved version
  APPROVAL              APPROVED / PENDING
  LINKEDIN STATUS       POSTED / NOT POSTED

------------------------------------------------------------------------

## ⚙️ Key Features

### 🤖 AI-Driven Content Generation

Generates structured LinkedIn posts including: - Professional hook -
Problem statement - Solution approach - Workflow explanation - Tools &
technologies - Hashtags

### ✏️ Precision Editing Engine

Applies only explicit user-requested modifications without rewriting the
entire post.

### 🛡 Approval Workflow

Manual gate ensures content control before publishing.

### 🚀 Automated Publishing

Posts directly to LinkedIn once approved.

### 📈 Status Tracking

Updates Google Sheet after successful publishing.

------------------------------------------------------------------------

## 🧠 SEO Optimization Strategy

This project is optimized for GitHub discoverability using keywords such
as:

-   LinkedIn automation
-   AI content generation
-   n8n workflow automation
-   LinkedIn API integration
-   Social media automation system
-   LLM-powered content engine

------------------------------------------------------------------------

## 🖼 Workflow Visualization

Add your workflow screenshot:

    assets/workflow.png

------------------------------------------------------------------------

## 🔧 Tech Stack

-   n8n (No-code automation platform)
-   Google Sheets API
-   LinkedIn API
-   Groq Chat Model
-   Google Gemini
-   HTTP & Merge Nodes

------------------------------------------------------------------------

## 🚀 Setup Instructions

### 1. Import Workflow

Import the provided `workflow.json` into n8n.

### 2. Configure Credentials

Connect: - Google Sheets OAuth - LinkedIn OAuth - Groq API / Gemini API

### 3. Prepare Google Sheet

Set up required columns as defined above.

### 4. Run Workflow

-   Add project details
-   Set APPROVAL to APPROVED
-   Execute workflow

The post will be published automatically.

------------------------------------------------------------------------

## 📁 Project Structure

    .
    ├── workflow.json
    ├── README.md
    └── assets/
        └── workflow.png

------------------------------------------------------------------------

## 🔮 Future Roadmap

-   Scheduled auto-posting\
-   Auto-generated image support\
-   Analytics tracking dashboard\
-   Multi-platform publishing (Twitter/X, Instagram)\
-   Hashtag performance optimization

------------------------------------------------------------------------

## 📄 License

This project is licensed under the MIT License.

------------------------------------------------------------------------

## 👨‍💻 Author

Built with precision and automation mindset by\
**Radhesh Reddy Yarram**

------------------------------------------------------------------------

## ⭐ Support

If you find this project useful: - Star the repository - Fork and
improve it - Share it with your network

