# Agent Configs

This repository contains configuration files for various LLM, focusing on agents.
It may include general guidelines, skills, rules, etc.
My plan is to make them service-agnostic, so they can be used with different LLM providers.

## Usage

Each agent configuration is stored in its respective directory.
For general Gemini configuration files, they are located in `~/.gemini/`.
Specifically for Google Antigravity, they are inside `~/.gemini/antigravity/`.
For Claude Code, the configuration files can be found in `~/.claude/`.

## Structure

*   `/skills`: Contains skill definitions for different agent capabilities.
    *   `/editor`: Skills related to text editing and manipulation.
