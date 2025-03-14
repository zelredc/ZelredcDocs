# Multiplayer Health and Health Bar

Need help?: (Join the Discord)[https://discord.gg/khM4XEsGHY]

# Features

- The following all works for multiplayer:

- Built-In Functions:
    - Set health - sets the health to the specified value, additional options for overriding max health if the new health is higher than or lower than the current max.
    - Set max health - sets the max health to the specified value.
    - Damage - Deals the specified amount of damage.
    - Heal - Heals the specified amount of health.
- Blueprint Implementable Functions:
    - OnInitialized - Called when the component initializes.
    - OnHealthChanged - Called via rep notify when health changes.
    - OnMaxHealthChanged - Called via rep notify when max health changes.
    - OnNoHealth - Called on server when health is zero.
    - OnFullHealth - Called on server when health is full.
- Fully Functional Examples:
    - Example calls to all of the built-in functions:
        - Keyboard 1: Set Health (random float).
        - Keyboard 2: Set Max Health (150).
        - Keyboard 3: Damage (10).
        - Keyboard 4: Heal (10).
        - Keyboard 5: A event that uses a timer to call damage on a timer (Damage over time system, can also be easily changed for healing over time).
    - UI Functionality for:
        - Updating the players health bar on UI when their health changes.
        - Updating a health bar above a players health when their health changes and allowing other clients to see this.
        - Updating health bar size based on max health (both on UI for the player who's max health changed and on the health bar above their head, again updating this for all clients to see).
        - Displaying a message on HUD when health is full or empty (player is dead).
    - Damaging Others:
        - Left Mouse Button: A simple line trace based system for damaging other players/actors that have the health component.
        - Event OnAnyDamage used to call the Damage Function.
    - NPCs:
        - A simple dummy NPC that randomly changes its health every 2 seconds and updates their health bar on all clients.
        - Support for and updating the size of NPC health bar on all clients when max health changed.
    - Misc:
        - A simple health pickup, walking over it grants 10 health.

# Getting Started

## Install the plugin

- Current the plugin is only on Fab.
- Open Epic Games Launcher and Install the Plugin to the version you are using.
- Open your project, or create a new one, go to edit>plugins and search for Multiplayer Health and Health Bar.
- Check the box to enable it.
- Restart the project when prompted.

## Accessing the content

- This plugin contains content
- Open the content browsers settings and ensure show plugin content/show engine content are enabled.
- Locate the plugin folder and open the content folder, this contains the blueprint code.
- If you want you can move this into the regular content folder for easier access when editing it.
- Open the demo level and run it to test the functionality.
- Open the blueprints if you need to modify anything, everything is well commented.

## Integrating the system with your project

- If you are integrating this with an existing project, you can start by adding the BP_HealthSystem component to your character.
- Then copy any required code from the demo assets into your version of that asset, or if you want you can keep using the demo assets, depending on use case.
- E.g. copying the code for updating the health bar from the health bar widget to your own health bar widget.
- You may need to change some details inside of the BP_HealthSystem component too, such as getting the HUD widget from the player character.
- Make sure your assets are implementing any interfaces they need and are set to replicated if required.
- Everything is well commented so you should be able to easily see what each function does and then decide if you need it.