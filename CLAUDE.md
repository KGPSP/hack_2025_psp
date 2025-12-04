# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the documentation package for the **HackNation 2025** hackathon challenge "Cyfrowy Nieśmiertelnik PSP" (Digital Dog Tag for Polish State Fire Service).

> **„Ratują innych, ryzykując własne życie. Czas, by technologia pomogła im w tym zadaniu. Stwórz rozwiązanie, które zwiększy bezpieczeństwo strażaków – nawet tam, gdzie nie ma sieci ani sygnału GPS."**

**Pula nagród:** 25 000 PLN

**Wydarzenie:** HackNation 2025, 6-7 grudnia 2025, Bydgoskie Centrum Targowo-Wystawiennicze (ul. Gdańska 187, Bydgoszcz)

**Organizator wyzwania:** Komenda Główna Państwowej Straży Pożarnej

## Repository Contents

This repository contains **documentation only** - no source code:
- `01_KARTA_WYZWANIA_v2.md` - Official challenge specification
- `02_SYMULATOR_API_v2.md` - Simulator API documentation (WebSocket + REST)
- `03_KONCEPCJA_HW_WYTYCZNE.md` - Hardware documentation guidelines
- `04_QUICK_START.md` - Quick start guide for participants
- `05_TECHNOLOGIA_RECCO.md` - RECCO backup localization technology docs
- `EKOSYSTEM_URZADZEN_PELNA_SPECYFIKACJA.md` - Full device ecosystem specification
- `FORMALNO_PRAWNE_HACKNATION.md` - Legal/formal requirements

## External Resources

**Simulator (public server - no installation required):**
- Frontend: https://niesmiertelnik.replit.app
- WebSocket: wss://niesmiertelnik.replit.app/ws
- REST API: https://niesmiertelnik.replit.app/api/v1/

**Documentation portal:** https://niesmiertelnikcyfrowy-admin810.replit.app

## Challenge Architecture

The challenge involves 6 device types:
1. **Tag Nieśmiertelnik** - Wearable device (UWB+IMU+LoRa+LTE+GNSS+BLE+Environmental sensors)
2. **Beacon UWB** - Positional anchor deployed in buildings
3. **Bramka NIB** - Network gateway in vehicles
4. **Pasek HR** - BLE heart rate monitor
5. **Reflektor RECCO** - Passive localization element (backup)
6. **Detektor RECCO** - Search device for RECCO reflectors

## Event Schedule

### Saturday, December 6, 2025
- 10:30 - Opening ceremony
- 11:00 - **Coding starts** (full task details released)

### Sunday, December 7, 2025
- 11:00 - **Coding ends** (judging begins)
- 15:30 - Project pitching
- 17:45 - Closing ceremony and results

## API Quick Reference

```bash
# Health check
curl https://niesmiertelnik.replit.app/api/v1/health

# List firefighters
curl https://niesmiertelnik.replit.app/api/v1/firefighters

# Trigger test alarm
curl -X POST https://niesmiertelnik.replit.app/api/v1/simulation/control \
  -H "Content-Type: application/json" \
  -d '{"action": "trigger_man_down", "params": {"firefighter_id": "FF-003"}}'
```

## Language Note

All documentation is in Polish. Key terminology:
- Strażak = Firefighter
- Nieśmiertelnik = Dog tag (military-style ID)
- Beacon = UWB positioning anchor
- Bramka NIB = Network gateway
- Pasek HR = Heart rate strap
- Pula nagród = Prize pool
