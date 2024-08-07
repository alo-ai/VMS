# ALO Milestone Integration Guide

## Introduction

This document provides instructions for integrating Milestone with ALO. It covers retrieving bookmarks from Milestone and sending them to the ALO.

## Installation

### Prerequisites

- **API key**: You need to contact ALO to obtain the API key, which will be configured by ALO to send the bookmarks to a specific team and channel.

### Installation Steps

1. During installation, you will be prompted for the API key and asked to choose whether to enable or disable automatic action creation at ALO.
2. You can modify these settings later by editing `appsettings.json` located at the installation location, for example:

`C:\Program Files\Milestone\XProtect Smart Client\MIPPlugins\AloAi.Milestone.Plugin\appsettings.json`

### The options are:

- **MinimumLevel**: The log level. Logs are grouped by date and stored at the installation location, in the logs folder, for example:

`C:\Program Files\Milestone\XProtect Smart Client\logs`


- **LookbackPeriod**: Search period for bookmarks (in minutes).

- **AutoActionCreation**: Auto creation of actions (true/false).

## How It Works?

The plugin exports bookmarks to: 

`C:\projects\alo-ai\plugin\AloAi.GenetecIntegration\AloAi.Milestone.Plugin`

Subsequently, it uploads them to ALO and deletes them from the disk.

## Upgrading

To upgrade:

1. Uninstall the current version.
2. Install the new version.

## Troubleshooting
1. Check the Milestone logs and make sure the ALO plugin is loaded.
   - **A. Make sure the logging is enabled:**
     - Go to Settings (gear icon in the upper right corner of the window).
     - Go to the Advanced tab.
     - Switch Logging (for technical support) to Enabled.

   - **B. Check the logs at this path:** `C:\ProgramData\Milestone\XProtect Smart Client\MIPLog`


2. The Milestone Smart Client requires a restart to load the ALO plugin. To verify that the plugin is loaded properly:

   - **A.** Open the options menu as shown in Screenshot 1.
   - **B.** Click on 'About'.
   - **C.** Ensure the plugin is listed as shown in Screenshot 2.

   <img src="Images/screenshot1.png" alt="Screenshot 1" width="200" height="150" style="margin: 10px;" />
   <img src="Images/screenshot2.png" alt="Screenshot 2" width="200" height="150" style="margin: 10px;" />

## Support

For assistance, contact:

success@alo.ai