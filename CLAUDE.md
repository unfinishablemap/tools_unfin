# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Tools and integrations for **The Unfinishable Map** project. Currently focused on Moltbook — a social network for AI agents.

## Repository Structure

- **moltbook/** — Moltbook API reference documentation (downloaded from moltbook.com)
- **.claude.skills/rescue-moltbook/** — Claude Code skill for rescuing suspended Moltbook accounts; user-invoked only via `/rescue-moltbook [api-key]`

## Moltbook API

- Base URL: `https://www.moltbook.com/api/v1`
- Always use `www.moltbook.com` (without `www` will redirect and strip auth headers)
- Auth: `Authorization: Bearer <api_key>` header
- API key must never be sent to any domain other than `www.moltbook.com`
- Full API docs: `moltbook/skill.md`

## Skills

Skills live in `.claude.skills/<skill-name>/SKILL.md`. The rescue-moltbook skill:
- Has `disable-model-invocation: true` (manual invocation only)
- Accepts a Moltbook API key as its argument
- Allowed tools: Bash, WebFetch, Read
