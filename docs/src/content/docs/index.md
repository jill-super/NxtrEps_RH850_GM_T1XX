---
title: Electric Power Steering Documentation
description: Technical documentation for the AUTOSAR-based Electric Power Steering system.
template: splash
hero:
  title: Electric Power Steering Documentation
  tagline: AUTOSAR-based steering control for the General Motors T1XX platform on the Renesas RH850 microcontroller.
  actions:
    - text: Browse the AUTOSAR layers
      link: /overview/autosar-layers/
      icon: right-arrow
    - text: Vector versus in-house code
      link: /overview/vector-vs-inhouse/
      icon: document
---

import { Card, CardGrid } from '@astrojs/starlight/components';

## Documentation map

<CardGrid stagger>
  <Card title="Application Software" icon="puzzle">
    Steering functions, customer functions, communication proxies and diagnostics. [Open the layer](/application-software/).
  </Card>
  <Card title="Complex Device Drivers" icon="setting">
    Microcontroller configuration, sensing, actuation and power electronics. [Open the layer](/complex-device-drivers/).
  </Card>
  <Card title="Basic Software and Microcontroller Abstraction" icon="layers">
    Services, Electronic Control Unit abstraction and microcontroller drivers. [Open the services](/basic-software-services/).
  </Card>
  <Card title="Communication, Operating System and Runtime" icon="rocket">
    Controller Area Network stack, operating system and runtime environment. [Open the stack](/communication-stack/).
  </Card>
  <Card title="Libraries, Tools and Integration" icon="open-book">
    Shared libraries, host tools and the top-level integration project. [Open libraries](/libraries/).
  </Card>
  <Card title="Glossary" icon="document">
    Every abbreviation is expanded to its long name. [Open the glossary](/overview/glossary/).
  </Card>
</CardGrid>

Every module page states its **origin** (Vector-provided or in-house) and links
its converted reference documents. See [how to read this documentation](/overview/document-conventions/).
