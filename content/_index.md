---
title: agentgateway
toc: false
description: ""
---

<style>
  .home-hero {
    position: relative;
    min-height: min(820px, calc(100svh - 1rem));
    display: flex;
    align-items: center;
    overflow: hidden;
    color: #101828;
    background: #f7f9fc;
    border-bottom: 1px solid #dbe3ef;
    isolation: isolate;
  }

  .home-hero::before {
    display: none;
  }

  .home-hero::after {
    display: none;
  }

  .landing-navbar .link {
    color: #273449 !important;
  }

  .landing-navbar .link:hover {
    color: #111827 !important;
  }

  .landing-navbar a[href="/"] svg path,
  nav.absolute.top-0 a[href="/"] svg path {
    fill: #111827;
  }

  .landing-navbar a[href="/"] svg path:nth-of-type(-n + 10),
  nav.absolute.top-0 a[href="/"] svg path:nth-of-type(-n + 10) {
    fill: #7734be;
  }

  nav.absolute.top-0 button {
    background: #111827;
  }

  .home-hero-inner {
    position: relative;
    z-index: 1;
    width: 100%;
    max-width: 1240px;
    box-sizing: border-box;
    margin: 0 auto;
    padding: 9rem 1.5rem 5rem;
  }

  .home-hero-layout {
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(360px, 430px);
    align-items: center;
    gap: 3.5rem;
  }

  .home-hero-copyblock {
    min-width: 0;
  }

  .home-eyebrow {
    display: inline-flex;
    align-items: center;
    gap: 0.625rem;
    color: #a78bfa;
    font-size: 0.8125rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 1.25rem;
  }

  .home-eyebrow img {
    width: 1.375rem;
    height: 1.375rem;
  }

  .home-hero h1 {
    max-width: 900px;
    color: #111827;
    font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    font-size: clamp(3.4rem, 5.7vw, 5rem);
    line-height: 0.9;
    font-weight: 850;
    letter-spacing: 0;
    text-shadow: none;
  }

  .home-hero-subtitle {
    max-width: 760px;
    margin-top: 1.5rem;
    color: #2f3a4f;
    font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    font-size: clamp(1.3rem, 2.2vw, 2rem);
    line-height: 1.25;
    font-weight: 760;
  }

  .home-hero-copy {
    max-width: 700px;
    margin-top: 1.25rem;
    color: #4b5565;
    font-size: 1.0625rem;
    line-height: 1.7;
  }

  .home-hero-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.875rem;
    margin-top: 2rem;
  }

  .home-proof {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1px;
    max-width: 660px;
    margin-top: 2.75rem;
    overflow: hidden;
    border: 1px solid rgba(119, 52, 190, 0.16);
    border-radius: 8px;
    background: rgba(119, 52, 190, 0.16);
    box-shadow: 0 24px 80px rgba(15, 23, 42, 0.08);
  }

  .home-proof div {
    min-height: 5.5rem;
    padding: 1rem;
    background: rgba(255, 255, 255, 0.76);
    backdrop-filter: blur(12px);
  }

  .home-proof strong {
    display: block;
    color: #111827;
    font-size: 1.35rem;
    line-height: 1.1;
  }

  .home-proof span {
    display: block;
    margin-top: 0.45rem;
    color: #596579;
    font-size: 0.78rem;
    line-height: 1.35;
  }

  .home-traffic-diagram {
    position: relative;
    width: 100%;
    max-width: 100%;
    box-sizing: border-box;
    min-width: 0;
    min-height: 500px;
    padding: 1.25rem;
    border: 1px solid rgba(119, 52, 190, 0.18);
    border-radius: 8px;
    background: rgba(255, 255, 255, 0.72);
    box-shadow: 0 28px 90px rgba(15, 23, 42, 0.1);
    overflow: hidden;
  }

  .home-traffic-diagram::before {
    content: "";
    position: absolute;
    inset: 1.25rem;
    border: 1px dashed rgba(119, 52, 190, 0.18);
    border-radius: 6px;
    pointer-events: none;
  }

  .home-diagram-label {
    position: relative;
    z-index: 1;
    color: #7a8496;
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }

  .home-diagram-row {
    position: relative;
    z-index: 1;
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 0.625rem;
    min-width: 0;
    margin-top: 0.75rem;
  }

  .home-diagram-node {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
    min-height: 3.35rem;
    padding: 0.75rem;
    border: 1px solid rgba(119, 52, 190, 0.18);
    border-radius: 8px;
    background: #ffffff;
    color: #182235;
    font-size: 0.88rem;
    font-weight: 740;
    text-align: center;
    box-shadow: 0 12px 34px rgba(15, 23, 42, 0.06);
  }

  .home-diagram-node span {
    display: block;
    margin-top: 0.2rem;
    color: #667085;
    font-size: 0.68rem;
    font-weight: 600;
  }

  .home-diagram-bus {
    position: relative;
    z-index: 1;
    display: grid;
    place-items: center;
    min-height: 11rem;
  }

  .home-diagram-bus::before,
  .home-diagram-bus::after {
    content: "";
    position: absolute;
    left: 50%;
    width: 1px;
    height: 3.25rem;
    background: #9b67d8;
    transform: translateX(-50%);
  }

  .home-diagram-bus::before {
    top: 0.875rem;
  }

  .home-diagram-bus::after {
    bottom: 0.875rem;
  }

  .home-diagram-core {
    position: relative;
    z-index: 1;
    display: grid;
    place-items: center;
    box-sizing: border-box;
    width: min(70%, 300px);
    min-height: 6rem;
    border: 2px solid rgba(119, 52, 190, 0.48);
    border-radius: 8px;
    background: #ffffff;
    color: #111827;
    text-align: center;
    box-shadow: 0 24px 70px rgba(119, 52, 190, 0.14);
  }

  .home-diagram-core strong {
    display: block;
    font-size: 1.15rem;
  }

  .home-diagram-core span {
    display: block;
    margin-top: 0.25rem;
    color: #596579;
    font-size: 0.75rem;
    font-weight: 640;
  }

  .home-diagram-backends {
    position: relative;
    z-index: 1;
  }

  .home-company-strip {
    background: #eef4ff;
    border-top: 1px solid rgba(119, 52, 190, 0.12);
    border-bottom: 1px solid rgba(119, 52, 190, 0.12);
  }

  .home-company-strip p {
    color: #7a8496;
  }

  .home-company-strip .logo-item span {
    color: #6b7280;
  }

  .home-company-strip .logo-item img {
    filter: none !important;
    opacity: 0.72;
  }

  .home-start-strip {
    background: #f7f9fc;
  }

  .home-start-strip .home-quick-card,
  .home-explain .home-explain-card,
  .home-features .feature-item {
    background: rgba(255, 255, 255, 0.82) !important;
    border-color: rgba(119, 52, 190, 0.14) !important;
    box-shadow: 0 18px 55px rgba(15, 23, 42, 0.07);
  }

  .home-start-strip .home-quick-card:hover,
  .home-explain .home-explain-card:hover,
  .home-features .feature-item:hover {
    border-color: rgba(119, 52, 190, 0.38) !important;
  }

  .home-start-strip h3,
  .home-explain h2,
  .home-explain h3,
  .home-explain .home-pill,
  .home-features h2,
  .home-features h3 {
    color: #111827 !important;
  }

  .home-start-strip p,
  .home-explain p,
  .home-explain span,
  .home-features p,
  .home-features th,
  .home-features td {
    color: #4b5565 !important;
  }

  .home-start-strip .w-10,
  .home-features .w-10 {
    background: #f3efff !important;
  }

  .home-explain {
    position: relative;
    overflow: hidden;
    background: #ffffff;
    border-top: 1px solid #edf1f7;
  }

  .home-explain::after {
    display: none;
  }

  .home-explain > div {
    position: relative;
    z-index: 1;
  }

  .home-explain .home-flow-panel {
    background: rgba(255, 255, 255, 0.78) !important;
    border-color: rgba(119, 52, 190, 0.16) !important;
    box-shadow: 0 26px 80px rgba(15, 23, 42, 0.08);
  }

  .home-explain .home-flow-core {
    background: #ffffff !important;
    border-color: rgba(119, 52, 190, 0.48) !important;
    box-shadow: 0 18px 45px rgba(119, 52, 190, 0.12);
  }

  .home-explain .home-pill {
    background: #f7f5ff !important;
    border-color: rgba(119, 52, 190, 0.18) !important;
  }

  .home-features {
    background: #f7f9fc !important;
  }

  .home-features button:hover {
    background: #f7f5ff !important;
  }

  .home-features .bg-tertiary-bg\/50 {
    background: #f7f5ff !important;
  }

  .home-light-section {
    background: #ffffff !important;
    border-top: 1px solid #edf1f7;
  }

  .home-light-section-alt {
    background: #f7f9fc !important;
    border-top: 1px solid #dbe3ef;
  }

  .home-light-section h2,
  .home-light-section h3,
  .home-light-section h4,
  .home-light-section-alt h2,
  .home-light-section-alt h3,
  .home-light-section-alt h4 {
    color: #111827 !important;
  }

  .home-light-section p,
  .home-light-section code,
  .home-light-section .text-secondary-text,
  .home-light-section-alt p,
  .home-light-section-alt code,
  .home-light-section-alt .text-secondary-text {
    color: #4b5565 !important;
  }

  .home-light-section .bg-primary-bg,
  .home-light-section .bg-secondary-bg,
  .home-light-section .bg-tertiary-bg,
  .home-light-section-alt .bg-primary-bg,
  .home-light-section-alt .bg-secondary-bg,
  .home-light-section-alt .bg-tertiary-bg {
    background: #ffffff !important;
  }

  .home-light-section .border-secondary-border,
  .home-light-section-alt .border-secondary-border {
    border-color: #dbe3ef !important;
  }

  .home-light-section a.bg-primary-bg,
  .home-light-section a.bg-secondary-bg,
  .home-light-section a.bg-tertiary-bg,
  .home-light-section-alt a.bg-primary-bg,
  .home-light-section-alt a.bg-secondary-bg,
  .home-light-section-alt a.bg-tertiary-bg,
  .home-light-card {
    background: #ffffff !important;
    border-color: #dbe3ef !important;
    box-shadow: 0 14px 42px rgba(15, 23, 42, 0.05);
  }

  .home-light-section a.bg-primary-bg:hover,
  .home-light-section a.bg-secondary-bg:hover,
  .home-light-section a.bg-tertiary-bg:hover,
  .home-light-section-alt a.bg-primary-bg:hover,
  .home-light-section-alt a.bg-secondary-bg:hover,
  .home-light-section-alt a.bg-tertiary-bg:hover {
    border-color: rgba(119, 52, 190, 0.38) !important;
  }

  .home-light-section .font-mono,
  .home-light-section-alt .font-mono {
    background: #0f172a !important;
  }

  .home-light-section .font-mono code,
  .home-light-section-alt .font-mono code {
    color: #e5e7eb !important;
  }

  .home-light-section .font-mono .text-secondary-text,
  .home-light-section-alt .font-mono .text-secondary-text {
    color: #94a3b8 !important;
  }

  .home-light-section button.bg-secondary-bg,
  .home-light-section-alt button.bg-secondary-bg {
    background: #f7f9fc !important;
  }

  .home-light-section a.text-primary-text:not(.bg-tertiary-text),
  .home-light-section-alt a.text-primary-text:not(.bg-tertiary-text) {
    color: #111827 !important;
    background: #ffffff !important;
    border-color: #dbe3ef !important;
  }

  .home-hero-actions a:first-child {
    background: #7734be;
    box-shadow: 0 12px 28px rgba(119, 52, 190, 0.24);
  }

  .home-hero-actions a:not(:first-child) {
    color: #111827;
    background: rgba(255, 255, 255, 0.72);
    border-color: rgba(119, 52, 190, 0.2);
    box-shadow: 0 12px 30px rgba(15, 23, 42, 0.06);
    backdrop-filter: blur(10px);
  }

  .home-hero-actions a:hover {
    border-color: rgba(119, 52, 190, 0.48);
  }

  .home-quick-card {
    display: block;
    border-radius: 8px;
    min-width: 0;
    max-width: 100%;
    overflow: hidden;
    overflow-wrap: anywhere;
    box-sizing: border-box;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.18);
  }

  .home-start-strip,
  .home-light-section,
  .home-light-section-alt {
    overflow-x: hidden;
  }

  .home-start-strip .grid > *,
  .home-light-section .grid > *,
  .home-light-section-alt .grid > * {
    min-width: 0;
  }

  .home-quick-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 24px 70px rgba(0, 0, 0, 0.26);
  }

  @media (max-width: 900px) {
    .home-hero {
      min-height: auto;
    }

    .home-hero-layout {
      grid-template-columns: 1fr;
      gap: 3rem;
    }

    .home-hero-inner {
      padding-top: 8rem;
      padding-bottom: 5rem;
    }

    .home-proof {
      grid-template-columns: 1fr;
      max-width: 360px;
    }
  }

  @media (max-width: 640px) {
    .home-hero h1 {
      font-size: clamp(2.35rem, 10.5vw, 2.6rem);
      line-height: 0.98;
    }

    .home-hero-subtitle,
    .home-hero-copy {
      max-width: 21.5rem;
    }

    .home-hero-inner {
      padding-bottom: 5rem;
    }

    .home-hero-actions {
      display: grid;
      grid-template-columns: 1fr;
      max-width: 18rem;
    }

    .home-traffic-diagram {
      width: calc(100% - 0.75rem);
      min-height: auto;
      padding: 0.875rem;
    }

    .home-diagram-row {
      grid-template-columns: 1fr;
    }

    .home-diagram-bus {
      min-height: 9rem;
    }

    .home-diagram-core {
      width: 100%;
    }

    .home-start-strip > div,
    .home-light-section > div,
    .home-light-section-alt > div {
      width: 100% !important;
      max-width: 100vw !important;
      box-sizing: border-box;
    }

    .home-start-strip .grid,
    .home-light-section .grid,
    .home-light-section-alt .grid {
      grid-template-columns: minmax(0, 1fr) !important;
    }
  }
</style>

<section class="home-hero">
<div class="home-hero-inner">
<div class="home-hero-layout">
  <div class="home-hero-copyblock">
    <div class="home-eyebrow"><img src="/mark-transparent.svg" alt="" aria-hidden="true" />Open source API and AI gateway</div>
    <h1 class="font-heading">agentgateway</h1>
    <p class="home-hero-subtitle font-heading">
    One high-performance gateway for service, LLM, and MCP traffic.
    </p>
    <p class="home-hero-copy">
    An open source HTTP and gRPC gateway that handles traditional application traffic and AI-native protocols in one data plane. Route, secure, observe, and govern services, LLM provider traffic, MCP tools, and agent-to-agent communication without stitching together separate gateways.
    </p>
    <div class="home-hero-actions">
    {{< button style="primary" href="/docs/quickstart/" iconRight="true" text="Get Started" icon="arrow-right" >}}
    {{< button style="secondary" href="https://github.com/agentgateway/agentgateway" text="View on GitHub" icon="github" >}}
    {{< button style="secondary" href="https://discord.gg/y9efgEmppm" text="Discord" icon="discord" >}}
    </div>
    <div class="home-proof">
      <div>
        <strong>LLM</strong>
        <span>Provider routing, model traffic governance, and OpenAI-compatible APIs</span>
      </div>
      <div>
        <strong>MCP</strong>
        <span>Federate tools and expose existing APIs as MCP-native servers</span>
      </div>
      <div>
        <strong>Services</strong>
        <span>One unified gateway for all your traffic: traditional HTTP services with high performance and rich functionality</span>
      </div>
    </div>
  </div>

  <div class="home-traffic-diagram" aria-label="agentgateway traffic diagram">
    <div class="home-diagram-label">Incoming traffic</div>
    <div class="home-diagram-row">
      <div class="home-diagram-node">Apps<span>HTTP / gRPC</span></div>
      <div class="home-diagram-node">Agents<span>A2A / tools</span></div>
      <div class="home-diagram-node">Services<span>east-west</span></div>
    </div>
    <div class="home-diagram-bus">
      <div class="home-diagram-core">
        <strong>agentgateway</strong>
        <span>route / secure / observe / govern</span>
      </div>
    </div>
    <div class="home-diagram-backends">
      <div class="home-diagram-label">Backends</div>
      <div class="home-diagram-row">
        <div class="home-diagram-node">LLM<span>providers</span></div>
        <div class="home-diagram-node">MCP<span>tools</span></div>
        <div class="home-diagram-node">Services<span>APIs</span></div>
      </div>
    </div>
  </div>
</div>
</div>
</section>

<section class="home-company-strip py-12 bg-primary-bg overflow-hidden">
  <p class="text-center text-secondary-text text-lg font-medium mb-8">Contributing Companies</p>
  <div class="marquee-container">
    <div class="marquee-track">
      <div class="marquee-content">
        <div class="logo-item">
          <img src="/adopters/solo-io-light.png" alt="Solo.io" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Solo.io</span>
        </div>
        <div class="logo-item">
          <img src="/quotes/microsoft.svg" alt="Microsoft" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Microsoft</span>
        </div>
        <div class="logo-item">
          <img src="/logos/apple.svg" alt="Apple" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Apple</span>
        </div>
        <div class="logo-item">
          <img src="/logos/alibaba.svg" alt="Alibaba" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Alibaba</span>
        </div>
        <div class="logo-item">
          <img src="/logos/adobe.svg" alt="Adobe" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Adobe</span>
        </div>
        <div class="logo-item">
          <img src="/logos/aws.svg" alt="AWS" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>AWS</span>
        </div>
        <div class="logo-item">
          <img src="/logos/cisco.svg" alt="Cisco" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Cisco</span>
        </div>
        <div class="logo-item">
          <img src="/logos/salesforce.svg" alt="Salesforce" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Salesforce</span>
        </div>
        <div class="logo-item">
          <img src="/logos/huawei.svg" alt="Huawei" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Huawei</span>
        </div>
        <div class="logo-item">
          <img src="/logos/amdocs.svg" alt="Amdocs" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Amdocs</span>
        </div>
      </div>
      <div class="marquee-content" aria-hidden="true">
        <div class="logo-item">
          <img src="/adopters/solo-io-light.png" alt="Solo.io" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Solo.io</span>
        </div>
        <div class="logo-item">
          <img src="/quotes/microsoft.svg" alt="Microsoft" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Microsoft</span>
        </div>
        <div class="logo-item">
          <img src="/logos/apple.svg" alt="Apple" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Apple</span>
        </div>
        <div class="logo-item">
          <img src="/logos/alibaba.svg" alt="Alibaba" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Alibaba</span>
        </div>
        <div class="logo-item">
          <img src="/logos/adobe.svg" alt="Adobe" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Adobe</span>
        </div>
        <div class="logo-item">
          <img src="/logos/aws.svg" alt="AWS" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>AWS</span>
        </div>
        <div class="logo-item">
          <img src="/logos/cisco.svg" alt="Cisco" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Cisco</span>
        </div>
        <div class="logo-item">
          <img src="/logos/salesforce.svg" alt="Salesforce" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Salesforce</span>
        </div>
        <div class="logo-item">
          <img src="/logos/huawei.svg" alt="Huawei" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Huawei</span>
        </div>
        <div class="logo-item">
          <img src="/logos/amdocs.svg" alt="Amdocs" class="logo-img" style="filter: brightness(0) invert(1);" />
          <span>Amdocs</span>
        </div>
      </div>
    </div>
  </div>
  <style>
    .marquee-container {
      width: 100%;
      overflow: hidden;
    }
    .marquee-track {
      display: flex;
      width: fit-content;
      animation: scroll-left 30s linear infinite;
      will-change: transform;
      backface-visibility: hidden;
      -webkit-backface-visibility: hidden;
      perspective: 1000px;
      -webkit-perspective: 1000px;
      transform: translate3d(0, 0, 0);
      -webkit-transform: translate3d(0, 0, 0);
    }
    .marquee-content {
      display: flex;
      align-items: flex-start;
      gap: 5rem;
      padding: 0 2.5rem;
      flex-shrink: 0;
    }
    .logo-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 0.75rem;
      min-width: 140px;
    }
    .logo-item span {
      color: #9ca3af;
      font-size: 0.875rem;
      font-weight: 500;
    }
    .logo-item img {
      image-rendering: -webkit-optimize-contrast;
      height: 56px;
      width: auto;
      max-width: 160px;
      object-fit: contain;
    }
    @keyframes scroll-left {
      0% { transform: translate3d(0, 0, 0); }
      100% { transform: translate3d(-50%, 0, 0); }
    }
  </style>
</section>


<section class="home-start-strip py-16 bg-secondary-bg" id="get-started">
  <div class="max-w-7xl mx-auto px-6">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
      <!-- Install -->
      <a href="/docs/quickstart/" class="home-quick-card group bg-tertiary-bg border border-secondary-border p-6 hover:border-tertiary-text transition-all">
        <div class="w-10 h-10 bg-primary-bg rounded-lg flex items-center justify-center mb-4">
          <svg class="w-5 h-5 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"></path>
          </svg>
        </div>
        <h3 class="text-primary-text text-lg font-bold mb-2">Install</h3>
        <p class="text-secondary-text text-sm">Get started with binary, Docker, or Kubernetes deployment options.</p>
      </a>
      <!-- Tutorials -->
      <a href="/tutorials/" class="home-quick-card group bg-tertiary-bg border border-secondary-border p-6 hover:border-tertiary-text transition-all">
        <div class="w-10 h-10 bg-primary-bg rounded-lg flex items-center justify-center mb-4">
          <svg class="w-5 h-5 text-violet-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"></path>
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
          </svg>
        </div>
        <h3 class="text-primary-text text-lg font-bold mb-2">Tutorials</h3>
        <p class="text-secondary-text text-sm">Step-by-step guides for APIs, MCP connectivity, A2A, and LLM routing.</p>
      </a>
      <!-- Documentation -->
      <a href="/docs/" class="home-quick-card group bg-tertiary-bg border border-secondary-border p-6 hover:border-tertiary-text transition-all">
        <div class="w-10 h-10 bg-primary-bg rounded-lg flex items-center justify-center mb-4">
          <svg class="w-5 h-5 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path>
          </svg>
        </div>
        <h3 class="text-primary-text text-lg font-bold mb-2">Documentation</h3>
        <p class="text-secondary-text text-sm">Complete reference for configuration, security, and policies.</p>
      </a>
      <!-- Integrations -->
      <a href="/docs/integrations/" class="home-quick-card group bg-tertiary-bg border border-secondary-border p-6 hover:border-tertiary-text transition-all">
        <div class="w-10 h-10 bg-primary-bg rounded-lg flex items-center justify-center mb-4">
          <svg class="w-5 h-5 text-amber-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"></path>
          </svg>
        </div>
        <h3 class="text-primary-text text-lg font-bold mb-2">Integrations</h3>
        <p class="text-secondary-text text-sm">Connect services, OpenAI, Anthropic, Gemini, Bedrock, Azure OpenAI, and MCP servers.</p>
      </a>
    </div>
  </div>
</section>

<!-- What is Agent Gateway Section -->
<section class="home-explain py-20 bg-primary-bg">
  <div class="max-w-7xl mx-auto px-6">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
      <div>
        <h2 class="text-primary-text text-3xl lg:text-4xl font-bold mb-6">What is Agent Gateway?</h2>
        <p class="text-secondary-text text-lg mb-4">
          Agent Gateway is an all-in-one gateway for application services, LLMs, and MCP tools. It handles standard service traffic alongside agent-to-LLM, agent-to-tool (MCP), and agent-to-agent (A2A) communication from one high-performance data plane.
        </p>
        <p class="text-secondary-text mb-8">
          Built to tackle enterprise traffic management, Agent Gateway gives teams one place to connect, secure, audit, and observe both application services and AI workloads.
        </p>
        <div class="space-y-4">
          <div class="home-explain-card bg-secondary-bg rounded-xl border border-secondary-border p-4">
            <div class="flex items-center gap-3 mb-2">
              <svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
              </svg>
              <h3 class="text-primary-text font-semibold">API and AI Native</h3>
            </div>
            <p class="text-secondary-text text-sm pl-8">Built for HTTP, gRPC, MCP, A2A, and LLM provider APIs in one gateway</p>
          </div>
          <div class="home-explain-card bg-secondary-bg rounded-xl border border-secondary-border p-4">
            <div class="flex items-center gap-3 mb-2">
              <svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
              </svg>
              <h3 class="text-primary-text font-semibold">Security First</h3>
            </div>
            <p class="text-secondary-text text-sm pl-8">RBAC, JWT authentication, TLS, and CEL-based access policies for service and AI traffic</p>
          </div>
          <div class="home-explain-card bg-secondary-bg rounded-xl border border-secondary-border p-4">
            <div class="flex items-center gap-3 mb-2">
              <svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
              </svg>
              <h3 class="text-primary-text font-semibold">High Performance</h3>
            </div>
            <p class="text-secondary-text text-sm pl-8">Written in Rust for low overhead, predictable latency, and any-scale deployment</p>
          </div>
        </div>
        <div class="mt-8">
          {{< button style="primary" href="#features" iconRight="true" text="Learn more about features" icon="arrow-right" >}}
        </div>
      </div>
      <div class="flex justify-center">
        <div class="home-flow-panel bg-secondary-bg rounded-xl border border-secondary-border p-8 w-full max-w-md">
          <div class="space-y-4">
            <div class="text-center">
              <span class="text-secondary-text text-xs uppercase tracking-wider">CLIENTS</span>
              <div class="flex justify-center gap-2 mt-3">
                <span class="home-pill bg-tertiary-bg border border-secondary-border rounded-lg px-4 py-2 text-primary-text text-sm">Apps</span>
                <span class="home-pill bg-tertiary-bg border border-secondary-border rounded-lg px-4 py-2 text-primary-text text-sm">Agents</span>
                <span class="home-pill bg-tertiary-bg border border-secondary-border rounded-lg px-4 py-2 text-primary-text text-sm">Services</span>
              </div>
            </div>
            <div class="flex justify-center">
              <div class="w-px h-6 bg-tertiary-text"></div>
            </div>
            <div class="flex justify-center">
              <div class="home-flow-core bg-primary-bg border-2 border-tertiary-text rounded-lg px-8 py-4 flex items-center justify-center">
                <img src="/mark-transparent.svg" alt="Agent Gateway" class="h-10 w-auto">
              </div>
            </div>
            <div class="flex justify-center">
              <div class="w-px h-6 bg-tertiary-text"></div>
            </div>
            <div class="text-center">
              <span class="text-secondary-text text-xs uppercase tracking-wider">BACKENDS</span>
              <div class="flex justify-center gap-2 mt-3">
                <span class="home-pill bg-tertiary-bg border border-secondary-border rounded-lg px-3 py-2 text-primary-text text-xs">Services</span>
                <span class="home-pill bg-tertiary-bg border border-secondary-border rounded-lg px-3 py-2 text-primary-text text-xs">LLMs</span>
                <span class="home-pill bg-tertiary-bg border border-secondary-border rounded-lg px-3 py-2 text-primary-text text-xs">MCP Tools</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Features Section -->
<section class="home-features py-16 bg-primary-bg" id="features">
<div class="max-w-4xl mx-auto px-6">
<h2 class="text-primary-text text-3xl lg:text-4xl font-bold text-center pb-4">Features</h2>
<p class="text-secondary-text text-center text-lg pb-10 max-w-2xl mx-auto">Everything you need for service traffic, LLM routing, and MCP connectivity in one fast gateway</p>
<div class="space-y-3" id="features-list">

<!-- Service Gateway -->
<div class="feature-item bg-secondary-bg rounded-xl border border-secondary-border overflow-hidden">
<button onclick="toggleFeature('api')" class="w-full flex items-center gap-4 p-5 text-left hover:bg-tertiary-bg/50 transition-colors">
<div class="w-10 h-10 bg-tertiary-bg rounded-lg flex items-center justify-center shrink-0">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7h16M4 12h16M4 17h16"></path></svg>
</div>
<div class="flex-1">
<h3 class="text-primary-text font-semibold">Service Gateway</h3>
<p class="text-secondary-text text-sm">Route and secure everyday HTTP and gRPC services with policy, TLS, auth, and observability</p>
</div>
<svg id="chevron-api" class="w-5 h-5 text-secondary-text transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
</button>
<div id="detail-api" class="hidden px-5 pb-5">
<div class="pl-14 border-l-2 border-tertiary-text/30 ml-5">
<p class="text-secondary-text text-sm mb-4">Use the same gateway for service traffic, LLM routing, and MCP connectivity instead of operating separate stacks for each traffic class.</p>
<ul class="text-secondary-text text-sm space-y-2 mb-4">
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">HTTP and gRPC proxying</strong> — Standard service-to-service and edge traffic</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">Traffic policies</strong> — TLS, CORS, rate limits, external auth, and request controls</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">Observability</strong> — Metrics, logs, and traces across API and AI traffic</span></li>
</ul>
<a href="/docs/" class="text-tertiary-text hover:underline text-sm font-medium">Learn more →</a>
</div>
</div>
</div>

<!-- LLM Gateway -->
<div class="feature-item bg-secondary-bg rounded-xl border border-secondary-border overflow-hidden">
<button onclick="toggleFeature('llm')" class="w-full flex items-center gap-4 p-5 text-left hover:bg-tertiary-bg/50 transition-colors">
<div class="w-10 h-10 bg-tertiary-bg rounded-lg flex items-center justify-center shrink-0">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path></svg>
</div>
<div class="flex-1">
<h3 class="text-primary-text font-semibold">LLM Gateway</h3>
<p class="text-secondary-text text-sm">Route traffic to major LLM providers with budget and spend controls through a unified OpenAI-compatible API</p>
</div>
<svg id="chevron-llm" class="w-5 h-5 text-secondary-text transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
</button>
<div id="detail-llm" class="hidden px-5 pb-5">
<div class="pl-14 border-l-2 border-tertiary-text/30 ml-5">
<p class="text-secondary-text text-sm mb-4">Seamlessly switch between providers without changing your application code.</p>
<table class="w-full text-sm mb-4 border-collapse">
<thead>
<tr class="border-b border-secondary-border">
<th class="text-left text-secondary-text py-2 font-medium">Provider</th>
<th class="text-center text-secondary-text py-2 font-medium">Chat Completions</th>
<th class="text-center text-secondary-text py-2 font-medium">Streaming</th>
</tr>
</thead>
<tbody class="text-secondary-text">
<tr class="border-b border-secondary-border/50"><td class="py-2">OpenAI / Azure OpenAI</td><td class="text-center text-emerald-400">✓</td><td class="text-center text-emerald-400">✓</td></tr>
<tr class="border-b border-secondary-border/50"><td class="py-2">Anthropic</td><td class="text-center text-emerald-400">✓</td><td class="text-center text-emerald-400">✓</td></tr>
<tr class="border-b border-secondary-border/50"><td class="py-2">Google Gemini</td><td class="text-center text-emerald-400">✓</td><td class="text-center text-emerald-400">✓</td></tr>
<tr class="border-b border-secondary-border/50"><td class="py-2">Google Vertex AI</td><td class="text-center text-emerald-400">✓</td><td class="text-center text-emerald-400">✓</td></tr>
<tr><td class="py-2">Amazon Bedrock</td><td class="text-center text-emerald-400">✓</td><td class="text-center text-emerald-400">✓</td></tr>
</tbody>
</table>
<div class="bg-tertiary-bg/50 rounded-lg p-3 mb-4">
<p class="text-primary-text text-sm font-medium mb-2">OpenAI-compatible providers</p>
<p class="text-secondary-text text-xs mb-2">Route to any provider that supports the OpenAI API format:</p>
<p class="text-secondary-text text-xs">Cohere, Mistral, Groq, Together AI, Fireworks, Ollama, LM Studio, vLLM, llama.cpp, and any custom endpoint with <code class="text-tertiary-text">/v1/chat/completions</code></p>
</div>
<a href="/docs/llm/" class="text-tertiary-text hover:underline text-sm font-medium">Learn more →</a>
</div>
</div>
</div>

<!-- Inference Routing -->
<div class="feature-item bg-secondary-bg rounded-xl border border-secondary-border overflow-hidden">
<button onclick="toggleFeature('inference')" class="w-full flex items-center gap-4 p-5 text-left hover:bg-tertiary-bg/50 transition-colors">
<div class="w-10 h-10 bg-tertiary-bg rounded-lg flex items-center justify-center shrink-0">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
</div>
<div class="flex-1">
<h3 class="text-primary-text font-semibold">Inference Routing</h3>
<p class="text-secondary-text text-sm">Intelligent routing to self-hosted models and local LLM workloads</p>
</div>
<svg id="chevron-inference" class="w-5 h-5 text-secondary-text transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
</button>
<div id="detail-inference" class="hidden px-5 pb-5">
<div class="pl-14 border-l-2 border-tertiary-text/30 ml-5">
<p class="text-secondary-text text-sm mb-4">Running your own models on GPU infrastructure? Agentgateway implements the Kubernetes Inference Gateway extensions for intelligent routing to local LLM workloads.</p>
<p class="text-primary-text text-sm font-medium mb-2">Route based on:</p>
<ul class="text-secondary-text text-sm space-y-2 mb-4">
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">GPU & KV cache utilization</strong> — Send requests to the least-loaded model</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">Prompt criticality</strong> — Prioritize high-priority requests</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">LoRA adapters</strong> — Route to models with specific fine-tuned adapters</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">Work queue depth</strong> — Avoid overloaded inference servers</span></li>
</ul>
<a href="/docs/llm/" class="text-tertiary-text hover:underline text-sm font-medium">Learn more →</a>
</div>
</div>
</div>

<!-- MCP Gateway -->
<div class="feature-item bg-secondary-bg rounded-xl border border-secondary-border overflow-hidden">
<button onclick="toggleFeature('mcp')" class="w-full flex items-center gap-4 p-5 text-left hover:bg-tertiary-bg/50 transition-colors">
<div class="w-10 h-10 bg-tertiary-bg rounded-lg flex items-center justify-center shrink-0">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 4a2 2 0 114 0v1a1 1 0 001 1h3a1 1 0 011 1v3a1 1 0 01-1 1h-1a2 2 0 100 4h1a1 1 0 011 1v3a1 1 0 01-1 1h-3a1 1 0 01-1-1v-1a2 2 0 10-4 0v1a1 1 0 01-1 1H7a1 1 0 01-1-1v-3a1 1 0 00-1-1H4a2 2 0 110-4h1a1 1 0 001-1V7a1 1 0 011-1h3a1 1 0 001-1V4z"></path></svg>
</div>
<div class="flex-1">
<h3 class="text-primary-text font-semibold">MCP Gateway</h3>
<p class="text-secondary-text text-sm">Connect LLMs to tools and external data sources using MCP</p>
</div>
<svg id="chevron-mcp" class="w-5 h-5 text-secondary-text transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
</button>
<div id="detail-mcp" class="hidden px-5 pb-5">
<div class="pl-14 border-l-2 border-tertiary-text/30 ml-5">
<p class="text-secondary-text text-sm mb-4">Connect LLMs to tools and external data sources using the Model Context Protocol (MCP).</p>
<ul class="text-secondary-text text-sm space-y-2 mb-4">
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">Tool federation</strong> — Aggregate multiple MCP servers behind a single endpoint</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">Protocol support</strong> — stdio, HTTP/SSE, and Streamable HTTP transports</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">OpenAPI integration</strong> — Expose existing REST APIs as MCP-native tools</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span><strong class="text-primary-text">Authentication & authorization</strong> — Built-in MCP auth spec compliance with OAuth providers (Auth0, Keycloak)</span></li>
</ul>
<a href="/docs/mcp/" class="text-tertiary-text hover:underline text-sm font-medium">Learn more →</a>
</div>
</div>
</div>

<!-- A2A Gateway -->
<div class="feature-item bg-secondary-bg rounded-xl border border-secondary-border overflow-hidden">
<button onclick="toggleFeature('agent')" class="w-full flex items-center gap-4 p-5 text-left hover:bg-tertiary-bg/50 transition-colors">
<div class="w-10 h-10 bg-tertiary-bg rounded-lg flex items-center justify-center shrink-0">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
</div>
<div class="flex-1">
<h3 class="text-primary-text font-semibold">A2A Gateway</h3>
<p class="text-secondary-text text-sm">Enable secure communication between AI agents using A2A</p>
</div>
<svg id="chevron-agent" class="w-5 h-5 text-secondary-text transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
</button>
<div id="detail-agent" class="hidden px-5 pb-5">
<div class="pl-14 border-l-2 border-tertiary-text/30 ml-5">
<p class="text-secondary-text text-sm mb-4">Enable secure communication between AI agents using the Agent-to-Agent (A2A) protocol. Agents can:</p>
<ul class="text-secondary-text text-sm space-y-2 mb-4">
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span>Discover each other's capabilities</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span>Negotiate interaction modalities (text, forms, media)</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span>Collaborate on long-running tasks</span></li>
<li class="flex items-start gap-2"><span class="text-tertiary-text">•</span><span>Operate without exposing internal state or tools</span></li>
</ul>
<a href="/docs/agent/" class="text-tertiary-text hover:underline text-sm font-medium">Learn more →</a>
</div>
</div>
</div>

<!-- Security & Observability -->
<div class="feature-item bg-secondary-bg rounded-xl border border-secondary-border overflow-hidden">
<button onclick="toggleFeature('security')" class="w-full flex items-center gap-4 p-5 text-left hover:bg-tertiary-bg/50 transition-colors">
<div class="w-10 h-10 bg-tertiary-bg rounded-lg flex items-center justify-center shrink-0">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
</div>
<div class="flex-1">
<h3 class="text-primary-text font-semibold">Security & Observability</h3>
<p class="text-secondary-text text-sm">Enterprise-grade authentication, authorization, and monitoring</p>
</div>
<svg id="chevron-security" class="w-5 h-5 text-secondary-text transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
</button>
<div id="detail-security" class="hidden px-5 pb-5">
<div class="pl-14 border-l-2 border-tertiary-text/30 ml-5">
<div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
<div class="bg-tertiary-bg/50 rounded-lg p-3">
<p class="text-primary-text text-sm font-medium mb-2">Authentication</p>
<p class="text-secondary-text text-xs">JWT, API keys, basic auth, MCP auth spec</p>
</div>
<div class="bg-tertiary-bg/50 rounded-lg p-3">
<p class="text-primary-text text-sm font-medium mb-2">Authorization</p>
<p class="text-secondary-text text-xs">Fine-grained RBAC with CEL policy engine</p>
</div>
<div class="bg-tertiary-bg/50 rounded-lg p-3">
<p class="text-primary-text text-sm font-medium mb-2">Traffic Policies</p>
<p class="text-secondary-text text-xs">Rate limiting, CORS, TLS, external authz</p>
</div>
<div class="bg-tertiary-bg/50 rounded-lg p-3">
<p class="text-primary-text text-sm font-medium mb-2">Observability</p>
<p class="text-secondary-text text-xs">Built-in OpenTelemetry metrics, logs, and distributed tracing</p>
</div>
</div>
<a href="/docs/configuration/security/" class="text-tertiary-text hover:underline text-sm font-medium">Learn more →</a>
</div>
</div>
</div>

</div>
</div>
</section>

<script>
function toggleFeature(feature) {
var detail = document.getElementById('detail-' + feature);
var chevron = document.getElementById('chevron-' + feature);
var isHidden = detail.classList.contains('hidden');
if (isHidden) {
detail.classList.remove('hidden');
chevron.classList.add('rotate-180');
} else {
detail.classList.add('hidden');
chevron.classList.remove('rotate-180');
}
}
</script>

<!-- Getting Started Section -->
<section class="home-light-section-alt py-16 bg-secondary-bg" id="getting-started">
<div class="max-w-4xl mx-auto px-6">
<div class="flex justify-between items-center mb-6">
<h2 class="text-primary-text text-2xl lg:text-3xl font-bold">Getting Started</h2>
<a href="/docs/deployment/" class="text-tertiary-text hover:underline text-sm font-medium flex items-center gap-1">View all docs <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg></a>
</div>
<div class="bg-primary-bg rounded-lg border border-secondary-border overflow-hidden mb-6">
<div class="flex items-center justify-between border-b border-secondary-border px-4 py-2">
<span class="text-xs font-medium text-tertiary-text">Binary</span>
<button onclick="copyGettingStarted()" id="copy-btn" class="px-3 py-1 text-xs text-secondary-text hover:text-primary-text bg-secondary-bg rounded border border-secondary-border transition-colors">Copy</button>
</div>
<div class="p-4 space-y-3 text-xs font-mono">
<div class="flex gap-3"><span class="text-tertiary-text">$</span><code class="text-primary-text">curl https://raw.githubusercontent.com/agentgateway/agentgateway/refs/heads/main/common/scripts/get-agentgateway | bash</code></div>
<div class="flex gap-3"><span class="text-tertiary-text">$</span><code class="text-primary-text">curl -sL https://raw.githubusercontent.com/agentgateway/agentgateway/main/examples/basic/config.yaml -o config.yaml</code></div>
<div class="flex gap-3"><span class="text-tertiary-text">$</span><code class="text-primary-text">agentgateway -f config.yaml</code></div>
<div class="text-secondary-text pt-1"># Open UI at localhost:15000</div>
</div>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
<a href="/docs/quickstart/" class="bg-primary-bg rounded-lg border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors">
<div class="flex items-center gap-2 mb-2">
<svg class="w-4 h-4 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
<h3 class="text-primary-text font-semibold">Quick Start</h3>
</div>
<p class="text-secondary-text text-sm">Get up and running with Agent Gateway in under 5 minutes.</p>
</a>
<a href="/docs/mcp/" class="bg-primary-bg rounded-lg border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors">
<div class="flex items-center gap-2 mb-2">
<svg class="w-4 h-4 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
<h3 class="text-primary-text font-semibold">MCP Connectivity Guide</h3>
</div>
<p class="text-secondary-text text-sm">Connect agents to MCP tool servers with auth.</p>
</a>
</div>
</div>
</section>

<script>
function copyGettingStarted() {
var commands = 'curl https://raw.githubusercontent.com/agentgateway/agentgateway/refs/heads/main/common/scripts/get-agentgateway | bash\ncurl -sL https://raw.githubusercontent.com/agentgateway/agentgateway/main/examples/basic/config.yaml -o config.yaml\nagentgateway -f config.yaml';
navigator.clipboard.writeText(commands);
var btn = document.getElementById('copy-btn');
btn.textContent = 'Copied!';
setTimeout(function() { btn.textContent = 'Copy'; }, 2000);
}
</script>

<!-- Tutorials Section -->
<section class="home-light-section py-16 bg-primary-bg" id="tutorials">
<div class="max-w-7xl mx-auto px-6">
<div class="flex justify-between items-center mb-4">
<h2 class="text-primary-text text-2xl lg:text-3xl font-bold">Tutorials</h2>
<a href="/tutorials/" class="text-tertiary-text hover:underline text-sm font-medium flex items-center gap-1">View all tutorials <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg></a>
</div>
<p class="text-secondary-text text-lg mb-8">Hands-on guides to get you up and running with agentgateway in minutes.</p>

<div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
<!-- Standalone Tutorials -->
<div>
<div class="flex items-center gap-2 mb-4">
<svg class="w-5 h-5 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2"></path></svg>
<h3 class="text-primary-text text-lg font-bold">Standalone</h3>
</div>
<div class="space-y-3">
<a href="/docs/standalone/latest/tutorials/llm-gateway/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">LLM Gateway</h4>
<p class="text-secondary-text text-xs mt-1">Route requests to OpenAI, Anthropic, and Gemini</p>
</div>
<span class="inline-block bg-tertiary-text/20 text-tertiary-text text-xs font-medium px-2 py-0.5 rounded-full">LLM</span>
</div>
</a>
<a href="/docs/standalone/latest/tutorials/basic/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">Basic MCP Server</h4>
<p class="text-secondary-text text-xs mt-1">Connect to your first MCP tool server</p>
</div>
<span class="inline-block bg-violet-400/20 text-violet-400 text-xs font-medium px-2 py-0.5 rounded-full">MCP</span>
</div>
</a>
<a href="/docs/standalone/latest/tutorials/mcp-federation/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">MCP Federation</h4>
<p class="text-secondary-text text-xs mt-1">Federate multiple MCP servers behind one endpoint</p>
</div>
<span class="inline-block bg-violet-400/20 text-violet-400 text-xs font-medium px-2 py-0.5 rounded-full">MCP</span>
</div>
</a>
<a href="/docs/standalone/latest/tutorials/" class="text-tertiary-text hover:underline text-sm font-medium flex items-center gap-1 mt-3 ml-1">View all standalone tutorials <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg></a>
</div>
</div>

<!-- Kubernetes Tutorials -->
<div>
<div class="flex items-center gap-2 mb-4">
<svg class="w-5 h-5 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path></svg>
<h3 class="text-primary-text text-lg font-bold">Kubernetes</h3>
</div>
<div class="space-y-3">
<a href="/docs/kubernetes/latest/tutorials/llm-gateway/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">LLM Gateway</h4>
<p class="text-secondary-text text-xs mt-1">Route to LLM providers on Kubernetes with Gateway API</p>
</div>
<span class="inline-block bg-tertiary-text/20 text-tertiary-text text-xs font-medium px-2 py-0.5 rounded-full">LLM</span>
</div>
</a>
<a href="/docs/kubernetes/latest/tutorials/basic/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">Basic MCP Server</h4>
<p class="text-secondary-text text-xs mt-1">Deploy and route to an MCP server on K8s</p>
</div>
<span class="inline-block bg-violet-400/20 text-violet-400 text-xs font-medium px-2 py-0.5 rounded-full">MCP</span>
</div>
</a>
<a href="/docs/kubernetes/latest/tutorials/azure-ai-foundry/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">Azure AI Foundry</h4>
<p class="text-secondary-text text-xs mt-1">Route to Azure OpenAI through agentgateway</p>
</div>
<span class="inline-block bg-blue-400/20 text-blue-400 text-xs font-medium px-2 py-0.5 rounded-full">Azure</span>
</div>
</a>
<a href="/docs/kubernetes/latest/tutorials/jwt-authorization/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">JWT Authorization</h4>
<p class="text-secondary-text text-xs mt-1">Secure your gateway with JWT authentication</p>
</div>
<span class="inline-block bg-amber-400/20 text-amber-400 text-xs font-medium px-2 py-0.5 rounded-full">Security</span>
</div>
</a>
<a href="/docs/kubernetes/latest/llm/guardrails/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">AI Prompt Guard</h4>
<p class="text-secondary-text text-xs mt-1">Block sensitive data in LLM requests</p>
</div>
<span class="inline-block bg-amber-400/20 text-amber-400 text-xs font-medium px-2 py-0.5 rounded-full">Security</span>
</div>
</a>
<a href="/docs/kubernetes/latest/tutorials/prompt-enrichment/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">Prompt Enrichment</h4>
<p class="text-secondary-text text-xs mt-1">Inject context at the gateway layer for better LLM output</p>
</div>
<span class="inline-block bg-tertiary-text/20 text-tertiary-text text-xs font-medium px-2 py-0.5 rounded-full">LLM</span>
</div>
</a>
<a href="/docs/kubernetes/latest/tutorials/claude-code-proxy/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">Claude Code CLI Proxy</h4>
<p class="text-secondary-text text-xs mt-1">Proxy and secure agentic CLI traffic</p>
</div>
<span class="inline-block bg-amber-400/20 text-amber-400 text-xs font-medium px-2 py-0.5 rounded-full">Security</span>
</div>
</a>
<a href="/docs/kubernetes/latest/tutorials/telemetry/" class="bg-secondary-bg rounded-xl border border-secondary-border p-4 hover:border-tertiary-text/50 transition-colors block">
<div class="flex items-center justify-between">
<div>
<h4 class="text-primary-text font-semibold text-sm">Telemetry & Observability</h4>
<p class="text-secondary-text text-xs mt-1">Distributed tracing with OpenTelemetry and Jaeger</p>
</div>
<span class="inline-block bg-cyan-400/20 text-cyan-400 text-xs font-medium px-2 py-0.5 rounded-full">Ops</span>
</div>
</a>
<a href="/docs/kubernetes/latest/tutorials/" class="text-tertiary-text hover:underline text-sm font-medium flex items-center gap-1 mt-3 ml-1">View all Kubernetes tutorials <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg></a>
</div>
</div>
</div>
</div>
</section>

<!-- Popular Integrations Section -->
<section class="home-light-section-alt py-16 bg-secondary-bg" id="integrations">
<div class="max-w-7xl mx-auto px-6">
<div class="flex justify-between items-center mb-8">
<h2 class="text-primary-text text-2xl lg:text-3xl font-bold">Popular Integrations</h2>
<a href="/docs/integrations/" class="text-tertiary-text hover:underline text-sm font-medium flex items-center gap-1">View all integrations <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg></a>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
<a href="/docs/integrations/llm-providers/" class="bg-primary-bg rounded-xl border border-secondary-border p-5 hover:border-tertiary-text/50 transition-colors">
<div class="flex items-center gap-3 mb-2">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
<h3 class="text-primary-text font-bold">LLM Providers</h3>
</div>
<p class="text-secondary-text text-sm">Connect to OpenAI, Anthropic, Azure OpenAI, Amazon Bedrock, and Google Gemini.</p>
</a>
<a href="/docs/integrations/mcp-servers/" class="bg-primary-bg rounded-xl border border-secondary-border p-5 hover:border-tertiary-text/50 transition-colors">
<div class="flex items-center gap-3 mb-2">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 9l3 3-3 3m5 0h3M5 20h14a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
<h3 class="text-primary-text font-bold">MCP Servers</h3>
</div>
<p class="text-secondary-text text-sm">Expose and federate MCP tool servers with stdio, SSE, and streamable HTTP transports.</p>
</a>
<a href="/docs/integrations/platforms/kubernetes/" class="bg-primary-bg rounded-xl border border-secondary-border p-5 hover:border-tertiary-text/50 transition-colors">
<div class="flex items-center gap-3 mb-2">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path></svg>
<h3 class="text-primary-text font-bold">Kubernetes Gateway API</h3>
</div>
<p class="text-secondary-text text-sm">Deploy and dynamically configure agentgateway on Kubernetes using a built-in control plane.</p>
</a>
<a href="/docs/integrations/observability/" class="bg-primary-bg rounded-xl border border-secondary-border p-5 hover:border-tertiary-text/50 transition-colors">
<div class="flex items-center gap-3 mb-2">
<svg class="w-5 h-5 text-tertiary-text" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path></svg>
<h3 class="text-primary-text font-bold">Observability</h3>
</div>
<p class="text-secondary-text text-sm">OpenTelemetry, Prometheus, Grafana, and Jaeger for metrics, tracing, and visualization.</p>
</a>
</div>
</div>
</section>

<script>
function copyCode(button) {
  const codeBlock = button.previousElementSibling;
  const text = codeBlock.innerText;
  navigator.clipboard.writeText(text).then(() => {
    const originalSvg = button.innerHTML;
    button.innerHTML = '<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>';
    button.classList.add('text-green-400');
    setTimeout(() => {
      button.innerHTML = originalSvg;
      button.classList.remove('text-green-400');
    }, 2000);
  });
}
function showDockerOption(option) {
  document.querySelectorAll('.docker-content').forEach(el => el.classList.add('hidden'));
  document.querySelectorAll('.docker-option').forEach(el => {
    el.classList.remove('bg-tertiary-text', 'text-white', 'border-tertiary-text');
    el.classList.add('bg-secondary-bg', 'text-primary-text', 'border-secondary-border', 'hover:border-tertiary-text', 'hover:bg-tertiary-bg');
  });
  document.getElementById('docker-' + option).classList.remove('hidden');
  const selectedOpt = document.getElementById('docker-opt-' + option);
  selectedOpt.classList.add('bg-tertiary-text', 'text-white', 'border-tertiary-text');
  selectedOpt.classList.remove('bg-secondary-bg', 'text-primary-text', 'border-secondary-border', 'hover:border-tertiary-text', 'hover:bg-tertiary-bg');
}
function switchLLMProvider(provider) {
  document.querySelectorAll('.llm-provider-content').forEach(el => el.classList.add('hidden'));
  document.getElementById('llm-' + provider).classList.remove('hidden');
  const exportEl = document.getElementById('docker-llm-export');
  const exports = {
    openai: 'export OPENAI_API_KEY=your-api-key',
    gemini: 'export GEMINI_API_KEY=your-api-key',
    anthropic: 'export ANTHROPIC_API_KEY=your-api-key',
    bedrock: 'export AWS_ACCESS_KEY_ID=your-access-key-id\nexport AWS_SECRET_ACCESS_KEY=your-secret-access-key\nexport AWS_REGION=us-east-1'
  };
  exportEl.textContent = exports[provider];
}
function showBinaryOption(option) {
  document.querySelectorAll('.binary-content').forEach(el => el.classList.add('hidden'));
  document.querySelectorAll('.binary-option').forEach(el => {
    el.classList.remove('bg-tertiary-text', 'text-white', 'border-tertiary-text');
    el.classList.add('bg-secondary-bg', 'text-primary-text', 'border-secondary-border', 'hover:border-tertiary-text', 'hover:bg-tertiary-bg');
  });
  document.getElementById('binary-' + option).classList.remove('hidden');
  const selectedOpt = document.getElementById('binary-opt-' + option);
  selectedOpt.classList.add('bg-tertiary-text', 'text-white', 'border-tertiary-text');
  selectedOpt.classList.remove('bg-secondary-bg', 'text-primary-text', 'border-secondary-border', 'hover:border-tertiary-text', 'hover:bg-tertiary-bg');
}
function switchBinaryLLMProvider(provider) {
  document.querySelectorAll('.binary-llm-provider-content').forEach(el => el.classList.add('hidden'));
  document.getElementById('binary-llm-' + provider).classList.remove('hidden');
  const exportEl = document.getElementById('binary-llm-export');
  const exports = {
    openai: 'export OPENAI_API_KEY=your-api-key',
    gemini: 'export GEMINI_API_KEY=your-api-key',
    anthropic: 'export ANTHROPIC_API_KEY=your-api-key',
    bedrock: 'export AWS_ACCESS_KEY_ID=your-access-key-id\nexport AWS_SECRET_ACCESS_KEY=your-secret-access-key\nexport AWS_REGION=us-east-1'
  };
  exportEl.textContent = exports[provider];
}
function showK8sOption(option) {
  document.querySelectorAll('.k8s-content').forEach(el => el.classList.add('hidden'));
  document.querySelectorAll('.k8s-option').forEach(el => {
    el.classList.remove('bg-tertiary-text', 'text-white', 'border-tertiary-text');
    el.classList.add('bg-secondary-bg', 'text-primary-text', 'border-secondary-border', 'hover:border-tertiary-text', 'hover:bg-tertiary-bg');
  });
  document.getElementById('k8s-' + option).classList.remove('hidden');
  const selectedOpt = document.getElementById('k8s-opt-' + option);
  selectedOpt.classList.add('bg-tertiary-text', 'text-white', 'border-tertiary-text');
  selectedOpt.classList.remove('bg-secondary-bg', 'text-primary-text', 'border-secondary-border', 'hover:border-tertiary-text', 'hover:bg-tertiary-bg');
}
</script>

<section class="home-light-section text-center py-20">
  <h2 class="text-primary-text text-3xl font-bold pb-12">
    AI-native connectivity for agentic applications
  </h2>
  <div class="flex flex-col md:flex-row text-start gap-8 items-center md:items-stretch justify-center mx-6 min-h-36">
    <a class="bg-secondary-bg rounded-xl md:max-w-96 p-4 border-secondary-border border-[1px] hover:border-primary-border" href="/docs/mcp/">
      <h3 class="font-bold text-primary-text">
        <span class="text-tertiary-text">Tool Federation</span>
      </h3>
      <p class="text-secondary-text text-sm">
        Provide a single MCP endpoint for all the tools your agents consume, with unified security, observability, and governance for all agent-to-tool communication.
      </p>
    </a>
    <a class="bg-secondary-bg rounded-xl md:max-w-96 p-4 border-secondary-border border-[1px] hover:border-primary-border" href="/docs/mcp/connect/">
      <h3 class="font-bold  text-primary-text">
        <span class="text-tertiary-text">Unified Connectivity</span>
      </h3>
      <p class="text-secondary-text text-sm">
        Support for industry standard AI protocols for agent and tool connectivity including A2A and MCP with the ability to automatically expose existing REST APIs as MCP-native tools.
      </p>
    </a>
    <a class="bg-secondary-bg rounded-xl md:max-w-96 p-4 border-secondary-border border-[1px] hover:border-primary-border" href="/docs/quickstart/mcp/#step-4-explore-the-ui">
      <h3 class="font-bold  text-primary-text">
        <span class="text-tertiary-text">Developer Portal</span>
      </h3>
      <p class="text-secondary-text text-sm">
        Self-service developer portal for agent and tool developers to create, configure, discover, and debug tools and agents from a single pane of glass UI.
      </p>
    </a>
  </div>
</section>

<!-- Community Meeting Section -->
<section class="home-light-section-alt py-16 bg-primary-bg" id="community-meeting">
  <div class="max-w-5xl mx-auto px-6">
    <h2 class="text-primary-text text-3xl lg:text-4xl font-bold text-center mb-4">Join the Community</h2>
    <p class="text-center text-secondary-text text-lg mb-8 max-w-3xl mx-auto">
      Calling all agent creators, tool providers, platform engineers, and AI enthusiasts - come build the future of AI agent connectivity.
    </p>
    <div class="flex justify-center gap-4 mb-12">
      {{< button style="secondary" href="https://discord.gg/y9efgEmppm" text="Discord" icon="discord" >}}
      {{< button style="secondary" href="https://github.com/agentgateway/agentgateway" text="GitHub" icon="github" >}}
    </div>
    {{< community-meeting >}}
  </div>
</section>

{{< quotes-carousel >}}

<section class="home-light-section text-center py-20 bg-secondary-bg">
  <h2 class="text-primary-text text-3xl font-bold pb-12">
    Solving AI Connectivity Challenges
  </h2>
  <div class="text-start max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-8">
    <div class="bg-tertiary-bg rounded-xl p-4 border-secondary-border border-[1px]">
      <h3 class="font-bold text-primary-text">
        <span class="text-tertiary-text">Agent and Tool Interoperability</span>
      </h3>
      <p class="text-secondary-text text-sm">
        Built on the leading industry protocols for agent and tool connectivity, agentgateway allows you to seamlessly integrate any agent and tool supporting A2A and MCP.
      </p>
    </div>
    <div class="bg-tertiary-bg rounded-xl p-4 border-secondary-border border-[1px]">
      <h3 class="font-bold text-primary-text">
        <span class="text-tertiary-text">Agent Governance</span>
      </h3>
      <p class="text-secondary-text text-sm">
        Agentic applications will be composed of multiple tools and agents working together to achieve a goal, creating a fragmented landscape for security and observability. Agentgateway is a drop-in solution transparent to agents and tools to secure, govern, and audit agent and tool communications.
      </p>
    </div>
    <div class="bg-tertiary-bg rounded-xl p-4 border-secondary-border border-[1px]">
      <h3 class="font-bold text-primary-text">
        <span class="text-tertiary-text">Tool Sprawl</span>
      </h3>
      <p class="text-secondary-text text-sm">
        Agent development will never scale treating every tool integration as a 1:1 integration. Agentgateway provides a federated MCP endpoint with a centralized registry, self-service discovery, and dynamic configuration of agents and tools.
      </p>
    </div>
    <div class="bg-tertiary-bg rounded-xl p-4 border-secondary-border border-[1px]">
      <h3 class="font-bold text-primary-text">
        <span class="text-tertiary-text">Leveraging Existing APIs</span>
      </h3>
      <p class="text-secondary-text text-sm">
        No need to create custom MCP tool server implementations for every REST API you have today. Agentgateway automatically translates OpenAPI resources into MCP tools ready to consume from agents.
      </p>
    </div>
  </div>
</section>
