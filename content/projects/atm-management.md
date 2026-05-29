---
layout: project
title: "ATM Management System"
description: "Python ATM simulator with facial recognition as a biometric authentication layer, built with Tkinter, OpenCV, and MySQL."
category: "Software & ML"
tags: [Python, OpenCV, Tkinter, MySQL, Computer Vision, Biometrics]
link: "https://github.com/devesh-b/ATM-Management"
---

## Overview

A desktop ATM simulation application that replaces the standard PIN with **facial recognition** as the primary authentication factor. Built in Python using Tkinter for the GUI, OpenCV for face detection and recognition, and MySQL for account data persistence.

## System Design

**Authentication flow**: At login, the webcam captures a live frame. OpenCV's face detection pipeline (Haar cascade or LBP detector) locates the face region, which is then matched against the enrolled face embedding stored per account in MySQL. A match threshold governs acceptance — tunable to balance false accept rate against false reject rate.

**ATM operations**: Standard banking transactions — balance inquiry, cash withdrawal, deposit, mini-statement — are implemented with proper transaction logging. Each operation validates session state to prevent unauthorised access after the biometric step.

**Data layer**: MySQL stores account records, transaction history, and facial feature data. Parameterised queries were used throughout to guard against SQL injection.

## Context

Built as an exploration of computer vision applied to security systems, combining GUI design, database integration, and real-time image processing in a single end-to-end project.
