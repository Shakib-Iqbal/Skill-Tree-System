# Skill Tree System

A data-driven skill recommendation system that recommends skills to learn based on a user's target domain/role and current skill set.

## Overview

The Skill Tree System is designed to help users identify relevant skills for a particular career role or domain. It uses aggregated survey data from professionals in different roles, where each skill is assigned a numerical importance score based on its reported relevance.

The project is currently in progress.

## How It Works

The system takes two main inputs:

- **Target Domain/Role** – The career role or domain the user is interested in.
- **Current Skill Set** – The skills the user already has.

Based on these inputs, the system analyzes the available survey data and generates a ranked list of skills recommended for the selected role.

## Current Features

- Role/domain-based skill recommendations
- Aggregated professional survey data
- Numerical importance scores for skills
- Ranked skill recommendations
- Interactive Streamlit interface
- Recommendations based on the user's existing skill level

## Technology Stack

- **Python** – Core development
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Streamlit** – Interactive web interface

## Project Workflow

```text
Select Target Role/Domain
        ↓
Enter Existing Skills
        ↓
Process Survey Data
        ↓
Calculate Skill Importance
        ↓
Rank Recommended Skills
        ↓
Display Recommendations
