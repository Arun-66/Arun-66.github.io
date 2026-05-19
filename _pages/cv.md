---
layout: page
permalink: /cv/
title: cv
nav: true
nav_order: 6
---

<style>
  .cv-shell { display: flex; gap: 2.5rem; align-items: flex-start; }
  .cv-sidenav { position: sticky; top: 80px; flex: 0 0 130px; font-size: 0.82rem; line-height: 2.2; }
  .cv-sidenav a { display: block; color: inherit; text-decoration: none; opacity: 0.65; transition: opacity 0.15s; }
  .cv-sidenav a:hover { opacity: 1; }
  .cv-main { flex: 1; min-width: 0; }
  .cv-entry { margin-bottom: 1.1rem; }
  .cv-entry:last-child { margin-bottom: 0; }
  .cv-row { display: flex; justify-content: space-between; flex-wrap: wrap; gap: 0.25rem; }
  .cv-date { color: #888; font-size: 0.88em; white-space: nowrap; }
  .cv-sub { color: #666; font-size: 0.88em; margin-top: 0.15rem; }
  .cv-body { font-size: 0.93em; margin-top: 0.35rem; margin-bottom: 0.2rem; }
  .cv-table td { vertical-align: top; padding: 0.25rem 0; }
  .cv-table td:first-child { white-space: nowrap; padding-right: 1.25rem; color: #888; font-size: 0.88em; }
  @media (max-width: 680px) {
    .cv-shell { flex-direction: column; }
    .cv-sidenav { position: static; flex: none; display: flex; flex-wrap: wrap; gap: 0 1.2rem; }
  }
</style>

<div style="margin-bottom: 1.5rem;">
  <a href="/assets/pdf/Devesh_Academic_CV.pdf" target="_blank" rel="noopener noreferrer"
     style="display: inline-flex; align-items: center; gap: 0.4rem; background: #2C5F5D; color: #fff;
            padding: 0.35rem 0.9rem; border-radius: 4px; font-size: 0.85rem; text-decoration: none;">
    <i class="fa-solid fa-file-pdf"></i> Download PDF
  </a>
</div>

<div class="cv-shell">

  <!-- Sidebar navigation -->
  <nav class="cv-sidenav">
    <a href="#experience">Experience</a>
    <a href="#education">Education</a>
    <a href="#awards">Awards</a>
    <a href="#leadership">Leadership</a>
    <a href="#skills">Technical Skills</a>
    <a href="#certificates">Certificates</a>
    <a href="#memberships">Memberships</a>
  </nav>

  <!-- Main content -->
  <div class="cv-main">

    <!-- ── Experience ─────────────────────────────── -->
    <a id="experience"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Experience</h3>

      <div class="cv-entry">
        <div class="cv-row"><strong>Digital Design Engineer</strong><span class="cv-date">2025 – present</span></div>
        <div class="cv-sub">Analog Devices India · Bengaluru, India</div>
        <p class="cv-body">Working on 10BASE-T1S PHY, PLL, GPT, UART, and PWM architectures for next-generation battery-management ICs in electric vehicles.</p>
        <ul style="margin:0; font-size:0.9em;"><li>Focus on system-level timing, jitter, and ISO functional safety.</li></ul>
      </div>

      <div class="cv-entry">
        <div class="cv-row"><strong>Digital Design Intern</strong><span class="cv-date">Jan 2025 – Jun 2025</span></div>
        <div class="cv-sub">Analog Devices India · Bengaluru, India</div>
        <p class="cv-body">Developed split configuration architecture for a dual-core lockstep processor.</p>
        <ul style="margin:0; font-size:0.9em;"><li>Implemented a functionally safe SPI module with configurable clock polarity and phase.</li></ul>
      </div>

      <div class="cv-entry">
        <div class="cv-row"><strong>Digital Design Intern</strong><span class="cv-date">Jun 2024 – Jul 2024</span></div>
        <div class="cv-sub">Analog Devices India · Bengaluru, India</div>
        <p class="cv-body">Optimized a PWM IP core (10% improvement in modulation accuracy).</p>
        <ul style="margin:0; font-size:0.9em;"><li>Integrated and analyzed a CAN FD architecture increasing data rates to 5 Mbps.</li></ul>
      </div>

      <div class="cv-entry">
        <div class="cv-row"><strong>Teaching Assistant – RF Microelectronics</strong><span class="cv-date">Jan 2025 – Mar 2025</span></div>
        <div class="cv-sub">PES University · Bengaluru, India</div>
        <p class="cv-body" style="margin-bottom:0;">Designed and delivered an advanced module on oscillator circuit design, developing Spectre RF simulation workflows.</p>
      </div>

      <div class="cv-entry">
        <div class="cv-row"><strong>Teaching Assistant – Computer Organization and Design</strong><span class="cv-date">Aug 2024 – Dec 2024</span></div>
        <div class="cv-sub">PES University · Bengaluru, India</div>
        <p class="cv-body" style="margin-bottom:0;">Taught RISC-V Assembly and guided students in designing single-cycle RISC-V processors.</p>
      </div>
    </div>

    <!-- ── Education ──────────────────────────────── -->
    <a id="education"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Education</h3>

      <div class="cv-entry">
        <div class="cv-row"><strong>B.Tech, Electronics and Communication Engineering</strong><span class="cv-date">2021 – 2025</span></div>
        <div class="cv-sub">PES University · Bengaluru, India</div>
        <div style="font-size:0.9em; margin-top:0.25rem;">GPA 9.32/10 · Silver Medal (9th Rank) · Best Outgoing Student, ECE</div>
      </div>

      <div class="cv-entry">
        <div class="cv-row"><strong>Pre-University Education</strong><span class="cv-date">2019 – 2021</span></div>
        <div class="cv-sub">Christ Junior College · Bengaluru, India</div>
        <div style="font-size:0.9em; margin-top:0.25rem;">Grade: 96.5%</div>
      </div>

      <div class="cv-entry">
        <div class="cv-row"><strong>Secondary Education (ICSE)</strong><span class="cv-date">2017 – 2019</span></div>
        <div class="cv-sub">Clarence High School · Bengaluru, India</div>
        <div style="font-size:0.9em; margin-top:0.25rem;">Grade: 95.6%</div>
        <ul style="margin:0.3rem 0 0; font-size:0.9em;">
          <li>Principal's Trophy for Excellence</li>
          <li>Smt. Narayanikutty Menon Memorial Trophy (perfect score, ICSE Mathematics)</li>
        </ul>
      </div>
    </div>

    <!-- ── Awards ─────────────────────────────────── -->
    <a id="awards"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Awards</h3>
      <table class="cv-table" style="width:100%; font-size:0.9em;">
        <tbody>
          <tr>
            <td>2025</td>
            <td><strong>Silver Medal — 9th Rank in University</strong><br><span style="color:#666;">PES University</span></td>
          </tr>
          <tr>
            <td>2025</td>
            <td><strong>Best Outgoing Student, ECE</strong><br><span style="color:#666;">PES University</span></td>
          </tr>
          <tr>
            <td>2024</td>
            <td><strong>Tiny Tapeout Award — Chipalooza ($300)</strong><br><span style="color:#666;">Efabless Corporation</span></td>
          </tr>
          <tr>
            <td>2022</td>
            <td><strong>MRD Scholarship — Top 5% of university</strong><br><span style="color:#666;">PES University</span> · Semesters III–VI (2022–2025)</td>
          </tr>
          <tr>
            <td>2023</td>
            <td><strong>Second Place — Mahil AI Hackathon</strong><br><span style="color:#666;">PES University</span></td>
          </tr>
          <tr>
            <td>2021</td>
            <td><strong>C.N. Rao Scholarship — Top 10% of university</strong><br><span style="color:#666;">PES University</span> · Semesters I–II (2021–2022)</td>
          </tr>
          <tr>
            <td>2021</td>
            <td><strong>Third Place — HackLoop Hackathon</strong><br><span style="color:#666;">PES University</span></td>
          </tr>
          <tr>
            <td>2019</td>
            <td><strong>Principal's Trophy for Excellence</strong><br><span style="color:#666;">Clarence High School</span></td>
          </tr>
        </tbody>
      </table>
    </div>

    <!-- ── Leadership ─────────────────────────────── -->
    <a id="leadership"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Leadership</h3>
      <ul class="list-group list-group-flush font-weight-light" style="font-size:0.93em;">
        <li class="list-group-item"><strong>Workshop Instructor — SoC Architecture &amp; Design Theory for IoT</strong> · PES University · Jun 2025 — 5-day intensive program, IoT MakerSpace, Department of ECE.</li>
        <li class="list-group-item"><strong>Co-founder &amp; Treasurer — IEEE RAS and Sensors Council Student Branch</strong> · PES University · Nov 2022–May 2024 — Co-founded the branch. Event Head for national-level hackathon UNIMATE and ideathon HealthSpark.</li>
        <li class="list-group-item"><strong>President — IEEE SSCS and Photonics Student Branch</strong> · PES University · Apr 2023–Apr 2024 — Hosted Prof. Shanthi Pavan (IIT Madras) for IEEE Day. Organized layout hackathons with Marvell Technology.</li>
        <li class="list-group-item"><strong>Mentor Head — InFeynite Hackathon</strong> · PES University · Jun–Sep 2024 — Led the mentorship team, managed technical sessions, supported participant project development.</li>
      </ul>
    </div>

    <!-- ── Technical Skills ───────────────────────── -->
    <a id="skills"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Technical Skills</h3>
      <ul class="list-group list-group-flush font-weight-light" style="font-size:0.93em;">
        <li class="list-group-item"><strong>Languages:</strong> SystemVerilog, Verilog, C, C++, Python, Java, Embedded C, Assembly, SQL</li>
        <li class="list-group-item"><strong>Specialized:</strong> Digital Circuit Design, RF Circuit Design, Analog Circuit Design, Mixed-Signal Systems</li>
        <li class="list-group-item"><strong>Tools:</strong> Cadence Virtuoso/SpectreRF/Genus, Vivado, Quartus Prime, LT-Spice, CST Studio, MATLAB, QUCS, RIPES</li>
        <li class="list-group-item"><strong>Spoken languages:</strong> English (Advanced), Hindi (Intermediate), Telugu (Intermediate), Kannada (Intermediate), Tamil (Novice)</li>
      </ul>
    </div>

    <!-- ── Certificates ────────────────────────────── -->
    <a id="certificates"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Certificates</h3>
      <table class="cv-table" style="width:100%; font-size:0.9em;">
        <tbody>
          <tr>
            <td>Mar 2025</td>
            <td><strong>IEEE Webinar on Pre-Silicon RTL Verification using UVM</strong><br><span style="color:#666;">IEEE Bangalore Section</span></td>
          </tr>
          <tr>
            <td>Mar 2025</td>
            <td><strong>Webinar on Science Narrative — Twisted Radio Waves</strong><br><span style="color:#666;">BIT Mesra</span></td>
          </tr>
          <tr>
            <td>Dec 2024</td>
            <td><strong>Analog IC Design — Schematic to Layout Workshop</strong><br><span style="color:#666;">ABV-IIITM Gwalior</span></td>
          </tr>
          <tr>
            <td>Sep 2024</td>
            <td><strong>BHARAT 6G VISION</strong><br><span style="color:#666;">Department of Telecommunications, India</span></td>
          </tr>
          <tr>
            <td>Jun 2024</td>
            <td><strong>CeNSE Summer School on Semiconductor Technology and Microfabrication</strong><br><span style="color:#666;">IISc</span></td>
          </tr>
          <tr>
            <td>Jan 2024</td>
            <td><strong>Standard Cell Design, Characterization and Synthesis</strong><br><span style="color:#666;">CHIPS, PES University</span></td>
          </tr>
          <tr>
            <td>Dec 2023</td>
            <td><strong>Semiconductor Device Modelling and Simulation</strong><br><span style="color:#666;">QuaNaD, PES University</span></td>
          </tr>
          <tr>
            <td>Oct 2023</td>
            <td><strong>VLSI Design Flow — RTL to GDS</strong><br><span style="color:#666;">NPTEL</span></td>
          </tr>
        </tbody>
      </table>
    </div>

    <!-- ── Memberships ────────────────────────────── -->
    <a id="memberships"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Memberships</h3>
      <ul class="list-group list-group-flush font-weight-light" style="font-size:0.93em;">
        <li class="list-group-item">IEEE Member (CAS, SSCS, MTTS) — Membership ID: 98147149 · Aug 2022–Present</li>
      </ul>
    </div>

    <!-- ── Further Information ────────────────────── -->
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">Further Information</h3>
      <ul class="list-group list-group-flush font-weight-light" style="font-size:0.93em;">
        <li class="list-group-item">References available on request.</li>
      </ul>
    </div>

  </div><!-- end .cv-main -->
</div><!-- end .cv-shell -->
