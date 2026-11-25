# Living Voices — Sprint 1 Contracts

## Project Information

- Project: Living Voices
- Team: Group 2
- Members: Pratik, Ethan, and Nikhil

## Services

| Service | Port | Database | Edge Prefix |
|---|---|---|---|
| edge-service | 9000 | N/A | N/A |
| recording-service | 9001 | recording | /recording |
| transcription-service | 9002 | transcription | /transcription |
| dictionary-service | 9003 | dictionary | /dictionary |

## Platform Configuration

| Component | Port |
|---|---|
| PostgreSQL | 5432 |
| Redis | 6379 |
| RabbitMQ | 5672 |
| RabbitMQ Management | 15672 |
| Keycloak | 8080 |

## Authentication

- Realm: LivingVoices
- Issuer: http://keycloak:8080/realms/LivingVoices
- Edge client: edge-service
- Development test client: living-voices-test

## Proposed Roles

- learner
- committee

## Proposed Main Business Task

Recording registration, consent management, and access control based on user permissions.

## API Contract

To be finalized by the team.

## Event Contract

- Proposed event: RecordingRegistered
- Destination: recording-registered
- Producer: recording-service
- Consumer: transcription-service
- Consumer group: transcription-service
- Each event must contain a unique eventId to prevent duplicate processing.

The exact JSON payload will be finalized by the team.

## Status

Initial draft. All members must review and agree on the contracts before implementation. Future contract changes require a pull request approved by all three members.
