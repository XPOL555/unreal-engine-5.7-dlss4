# DLSS 4 (UE 5.6) → UE 5.7 Experimental Port

## Overview
- This repository tracks the code changes I made to get NVIDIA’s DLSS 4 Unreal Engine plugin (originally for UE 5.6) working on Unreal Engine 5.7.
- The goal is to provide a reference for others attempting a similar migration, along with a working example project that compiles under UE 5.7.0.

## Status and Naming
- All plugins in this repo have their VersionName suffixed with “-EXPERIMENTAL_FORUM”.
  - Example: 1.0-EXPERIMENTAL_FORUM
- This suffix is intentional to signal that these are unofficial, experimental builds not endorsed by NVIDIA or Epic. Expect breaking changes and use at your own risk.

## Project Setup
- I created a blank C++ project using Unreal Engine 5.7.0.
- I then copied/merged the content from NVIDIA’s DLSS 4 sample project for UE 5.6 into this 5.7 project and iterated on the code and plugin descriptors until it built and ran.

## What Changed (High-Level)
- Updated plugin descriptors (.uplugin) and source where needed to target EngineVersion 5.7.0.
- Applied minor code fixes to account for API and build system differences between UE 5.6 and UE 5.7.
- Standardized the experimental suffix on all plugin VersionName fields: -EXPERIMENTAL_FORUM.

## Notes and Disclaimers
- This is an unofficial port provided as-is, without warranty. It is intended for experimentation and learning only.
- DLSS branding and related technologies are property of NVIDIA. Unreal Engine is property of Epic Games.
- If you encounter issues, please compare against upstream NVIDIA plugin releases for UE 5.6 and check UE 5.7 API changes.

## How to Use (at a glance)
1) Open the project with Unreal Engine 5.7.0.
2) Ensure you have a compatible NVIDIA driver and RTX-capable hardware for DLSS features.
3) Enable the included plugins as needed (DLSS, NIS, Streamline, etc.). Remember they’re marked as experimental.

## Acknowledgements
- NVIDIA for the original DLSS 4 plugin and sample project targeting UE 5.6.
- Epic Games for Unreal Engine.
- [Altercode Team](https://altercode.dev/?ref=github_dlss4_ue57), aka me 
