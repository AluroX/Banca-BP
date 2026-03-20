# Banca-BP
Sistema Bancario por Internet BP

Solución de banca por internet diseñada para la entidad BP, que permite a los clientes consultar movimientos, realizar transferencias, pagos y completar onboarding con verificación biométrica. La arquitectura sigue el modelo C4 y está desplegada en Microsoft Azure con alta disponibilidad, tolerancia a fallos y cumplimiento normativo ecuatoriano.

Decisiones Arquitectónicas (ADR)

- App Móvil	
- SPA Web	
- Flujo OAuth2	
- Onboarding Biométrico	
- Patrón de Datos	CQRS	
- Integración	API Gateway 
- Comunicación Asíncrona	
- Cache


Diagramas C4:

Contexto
┌─────────────────┐     ┌─────────────────────────────┐     ┌─────────────────┐
│   Cliente       │────▶│  Sistema de Banca por       │────▶│   Core Bancario │
│   [Persona]     │     │  Internet (BP)              │     │   [Externo]     │
└─────────────────┘     │  [Software System]          │     └─────────────────┘
                        └─────────────────────────────┘
                               │         │         │
                               ▼         ▼         ▼
                        ┌──────────┐ ┌──────────┐ ┌──────────┐
                        │ Onfido   │ │ AD B2C   │ │Notificac.│
                        │[Externo] │ │[Externo] │ │[Externo] │
                        └──────────┘ └──────────┘ └──────────┘

