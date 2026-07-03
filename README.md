# Flux-UI-Home-Assistant-Dashboard

A modular, reactive Home Assistant dashboard system built on a shared architecture for both Mobile and Tablet interfaces.

This project consolidates home automation control, environmental monitoring, and real-time system awareness into a single cohesive interface inspired by Material Design 3 principles.

It is designed as a **framework-style dashboard**, not a plug-and-play theme - intended to be adapted, extended, and mapped to your own Home Assistant environment.

<img width="1920" height="1080" alt="Mobile_tablet" src="https://github.com/user-attachments/assets/d3a40acd-9f01-45ba-9d35-2a1736824068" />

---

## 🧠 Overview

This dashboard is built around a **priority-driven, context-aware UI system**, where layout and content dynamically adapt based on real-time home state, sensor data, and automation events.

Rather than static pages, the interface continuously evaluates system conditions and presents only the most relevant information at any given moment.

---

## ✨ Features

### 🧠 Dynamic Context-Aware UI

The dashboard reacts dynamically to changes in home state, media activity, and environmental conditions.

- UI elements appear, update, or disappear based on relevance
- Critical information is prioritised over static content
- Layouts adjust automatically depending on system state

---

### 🏠 Live Home Overview Intelligence

The Overview dashboard acts as a real-time representation of the home.

It includes active state tracking such as:

- Open windows and doors across the home
- Active lights and illuminated zones
- Curtain and blind positions
- Running systems (laundry, irrigation, timers)
- Key environmental and automation metrics

This creates a living dashboard that reflects the current state of the home.

---

### 🚨 Contextual Notifications & Live Events

Important events are surfaced directly in context:

- Garage activity triggers live camera overlays with timers
- Motion or security events highlight relevant feeds
- System-critical updates are shown inline rather than as generic alerts

---

### 🎵 Media-Aware Layout Switching (Tablet)

When media is active (e.g. Spotify playback):

- The overview layout dynamically swaps sections to display “Now Playing”
- When playback stops, the original layout is restored automatically

---

### 🌤️ Adaptive Weather Intelligence

Weather components adjust based on real-time conditions:

- High wind speeds prioritise wind alerts
- Normal conditions show standard weather summary
- Environmental data is surfaced only when relevant

---

### 🚨 Status-Driven Mobile Header System

The Mobile dashboard header dynamically changes based on priority:

- Alarm states (armed, triggered, disarmed)
- Weather warnings or alerts
- Critical system notifications

---

### 🏠 Room-Level State Awareness

Each room view reflects live sensor state:

- Open doors and windows are shown when detected
- Indicators automatically disappear when closed
- Only relevant state is displayed to reduce clutter

---

### 📱 Responsive Multi-Device Design

- Shared core system between Mobile and Tablet dashboards (~80%)
- Device-specific layouts for optimal screen usage
- Unified templates, styling, and card system

---

## 📂 Project Structure

dashboard/

├── mobile/

├── tablet/

└── shared/


### Shared Architecture

- Centralised templates, cards, animations, and styling
- Reusable components used across both dashboards
- Single-source updates propagate across layouts

---

## 📸 Screenshots

> Screenshots represent selected views of the system only and do not reflect a full installation.

### 📱 Mobile Dashboard

<img width="4072" height="3072" alt="Mobile Dashboard Examples" src="https://github.com/user-attachments/assets/a0f83ad1-3963-46ad-be22-2146a13a3a2f" />

### 💻 Tablet Dashboard

<img width="4072" height="3072" alt="Tablet Dashboard Examples" src="https://github.com/user-attachments/assets/7e129765-fb71-42bc-be94-aee28b8eb8c0" />

---

## ⚙️ Installation

Flux UI is designed as a modular dashboard framework, not a plug-and-play solution.

It provides the structure, layouts, and reusable components, but you'll need to adapt it to your own Home Assistant installation by mapping your entities, rooms, and devices.

Prerequisites

Before installing Flux UI, ensure that:

Home Assistant is configured to use YAML dashboards.
All required custom cards and integrations are installed. See custom-cards.md for the complete dependency list.
You have access to your Home Assistant configuration files (VS Code, File Editor, or Samba).

**Step 1 - Copy the Dashboard Files**

Download or clone this repository.

Copy the following folders into your Home Assistant configuration directory (/config):

[dashboard/](https://github.com/ElementZoom/Flux-UI-Home-Assistant-Dashboard/tree/main/dashboard)
[www/](https://github.com/ElementZoom/Flux-UI-Home-Assistant-Dashboard/tree/main/www)

Your Home Assistant configuration should look similar to:

/config
├── dashboard
├── www
├── configuration.yaml
└── ...

**Step 2 - Register the Dashboards**

Open configuration.yaml and add the following configuration:

lovelace:
  dashboards:
    mobile-dashboard:
      mode: yaml
      filename: /config/dashboard/mobile/dashboard.yaml
      title: Mobile
      icon: mdi:cellphone
      show_in_sidebar: true

    tablet-dashboard:
      mode: yaml
      filename: /config/dashboard/tablet/dashboard.yaml
      title: Tablet
      icon: mdi:tablet
      show_in_sidebar: true

Restart Home Assistant (or reload the Lovelace configuration if applicable).

**Step 3 - Configure Your Home**

Flux UI uses placeholder entities and example configurations.

To make the dashboard functional, you'll need to:

- Replace entities with your own devices.
- Update room assignments.
- Configure cameras, media players, scenes, and automations.
- Adjust any templates to match your environment.

Think of Flux UI as a blueprint for building your own dashboard rather than a finished configuration.

**Step 4 - Enjoy & Customise**

Once your entities have been mapped, you can begin customising the dashboard to suit your home.

---

## 🧩 Required Dependencies

This dashboard relies on multiple Home Assistant custom integrations and UI components installed via **HACS** and external repositories.

👉 Full list: [`/docs/requirements/custom-cards.md`](https://github.com/ElementZoom/Flux-UI-Home-Assistant-Dashboard/blob/main/custom-cards.md)
---

## 🎨 Design Philosophy

This dashboard is built around:

- Material Design 3 principles
- Consistent spacing and typography
- Shared reusable components
- Context-aware UI rendering
- Minimal visual noise, high information density

---

## 🙏 Credits

This project would not be possible without the incredible Home Assistant ecosystem and its community.

Special thanks to:

- The Home Assistant core developers
- Maintainers of all custom cards and integrations used in this project
- The broader Home Assistant community for inspiration, examples, and shared knowledge

This dashboard builds on top of their work to create a unified, modular interface system.

---

## 💖 Support My Work
If you want to hire me to make your personal dashboard, you can hit me up on one of these social media platforms below, or contact me through my [website](https://elementzoom.co.nz/):

- Email at [reynaldi.sutrisno.rs16@gmail.com](url)
- [Reddit](https://www.reddit.com/user/ElementZoom/)
- [Facebook](https://www.facebook.com/elementzoom)
Or you can support me on [Ko-fi](https://ko-fi.com/elementzoom). Your support helps me keep creating and sharing more awesome open-source tools! Thank you for being part of this journey 🚀
