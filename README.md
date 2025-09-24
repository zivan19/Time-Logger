# Time Logger

This repository contains a self-contained Windows time tracking tool that runs as a desktop-style application without requiring any additional software to be installed.

## What's included

- **TimeLogger.hta** – The main application. Double-clicking this file on Windows 10/11 opens a full UI for tracking your work sessions.
- **Time Logs/Times Logged** – Folder structure where the app stores the daily log files it generates. A `.gitkeep` file is included so the folders exist when you clone the repository.

## Features

- Start/stop timer that asks for a description of your current work before tracking begins.
- Automatically saves each completed session to a dated text file located at `Time Logs/Times Logged/YYYY-MM-DD.txt`.
- Displays the start and end timestamps (formatted as `DD/MM - HH:mm`) and the total duration in decimal hours (e.g. `1.50`).
- Keeps an on-screen history of the sessions you have logged for the current day.
- Provides a quick link to open today's log file directly from the interface.

## How to run the app

1. Download or clone this repository onto your Windows computer.
2. Navigate to the folder in File Explorer.
3. Double-click `TimeLogger.hta` to launch the application (you may need to allow it to run if Windows shows a security prompt).
4. Enter what you are working on, click **Start**, and then click **Stop** when you are finished. Repeat as needed throughout the day.

All logs are written automatically; no console window or external runtime (such as Python, Node.js, or .NET) is required. The app uses the Windows built-in HTML Application (HTA) host, so it works on a clean installation of Windows 10 or Windows 11.

## Where your logs are stored

- Every time you stop the timer, the entry is appended to the day's log file.
- Logs live at `Time Logs/Times Logged/` alongside the application files.
- Each log entry includes the description, start time, end time, and duration in decimal hours.

## Notes

- Only one timer can run at a time. If you close the app while a timer is active, you will be prompted to confirm.
- To archive or share your logs, simply copy the files from the `Time Logs/Times Logged` folder.
