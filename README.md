# ALGROE
AI-powered plant assistant



Algroe is a command-line tool and machine-learning project that helps users identify plant species, detect health conditions, and track care needs through AI-powered image classification and heuristic analysis.


## Project Scope

Algroe aims to:
- Identify plant species from user-uploaded images using a fine-tuned FastAI CNN model.
- Diagnose early signs of disease, dryness, or nutrient deficiency using color and texture heuristics.
- Provide real-time suggestions for watering, fertilizing, or repotting.
- Store plant-care data and reminders in a lightweight SQLite database.


## CLI Command Overview

| Command                               | Function                                                             | Example |
| `plantctl classify <image>`           | Identifies the plant species and estimates its health condition | `plantctl classify fern.jpg` |
| `plantctl diagnose <image>`           | Runs deeper analysis on the image to detect disease, dryness, or nutrient issues | `plantctl    diagnose cactus_leaf.jpg` |
| `plantctl needs-now <plant_name>`     | Suggests what that plant currently needs (watering, sunlight, fertilizer, etc.) | `plantctl needs-now Monstera` |
| `plantctl tell-me-more <plant_name>`  | Displays detailed care info, species traits, growth tips, and common issues for that plant | `plantctl tell-me-more Aloe Vera` |
| `plantctl schedule`                   | Shows upcoming care reminders (watering, fertilizing, etc.) | `plantctl schedule` |
| `plantctl all <image>`                | Combines classify, diagnose, and needs-now into one comprehensive report | `plantctl all snake_plant.jpg` |


## Project Structure
# Algroe
    src - Main source code
        cli.py - CLI entry point
        model.oy - FASTAI image classification model
        db.py - SQLite database management
        utils.py - Image processing & heuristics
        init.py
    data - Dataset
    model - Trained model weights
    docs - Documentation & final report
    assets - CLI screenshots & visuals
    requirements.txt - Dependencies
