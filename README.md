# Gishushu Traffic Lights System

## Overview

This project provides a specification and state diagram for a typical Gishushu Traffic Lights system. The system consists of three primary states: Green Light, Yellow Light, and Red Light. The transitions between these states are timed to ensure the smooth flow of traffic.

## Specification (Narration)

A typical Gishushu Traffic Light system consists of three primary states:

1. **Green Light**:
   - **Description**: Allows traffic to proceed.
   - **Duration**: Typically lasts for a predefined period, e.g., 60 seconds.
   - **Transition**: After the duration, it transitions to the Yellow Light state.

2. **Yellow Light**:
   - **Description**: Warns drivers to prepare to stop.
   - **Duration**: Typically lasts for a shorter period, e.g., 5 seconds.
   - **Transition**: After the duration, it transitions to the Red Light state.

3. **Red Light**:
   - **Description**: Requires traffic to stop.
   - **Duration**: Typically lasts for a predefined period, e.g., 60 seconds.
   - **Transition**: After the duration, it transitions to the Green Light state.

## State Diagram

The state diagram for the Gishushu Traffic Lights system is represented using Mermaid syntax. You can visualize this diagram using any Mermaid-supported environment.

### Explanation of Traffic lights Sytem

- **`[*] --> GreenLight`**: The system starts in the Green Light state.
- **`GreenLight --> YellowLight : after 60s`**: After 60 seconds in the Green Light state, it transitions to the Yellow Light state.
- **`YellowLight --> RedLight : after 5s`**: After 5 seconds in the Yellow Light state, it transitions to the Red Light state.
- **`RedLight --> GreenLight : after 60s`**: After 60 seconds in the Red Light state, it transitions back to the Green Light state.

Each state (GreenLight, YellowLight, RedLight) has a nested state diagram to show the internal state transitions:

- **`GreenLight`**:
  - **`[*] --> GreenOn`**: The Green Light is on.
  - **`GreenOn --> [*] : after 60s`**: After 60 seconds, the Green Light turns off.

- **`YellowLight`**:
  - **`[*] --> YellowOn`**: The Yellow Light is on.
  - **`YellowOn --> [*] : after 5s`**: After 5 seconds, the Yellow Light turns off.

- **`RedLight`**:
  - **`[*] --> RedOn`**: The Red Light is on.
  - **`RedOn --> [*] : after 60s`**: After 60 seconds, the Red Light turns off.

## Contact

For any questions or suggestions, please contact manziosee at oseemanzi3@gmail.com

## Repository

You can find the source code and more details about this project on GitHub:

[Gishushu Traffic Lights System](https://github.com/manziosee/Gishushu_Traffic_Lights_System.git)


