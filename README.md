<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Black Box – Industrial Data Logger</title>
</head>
<body>
<h1>Black Box – The $20 Industrial Flight Recorder</h1>

render render_generated_image with prompt is A realistic photo of a tiny professional prototype PCB (approx 2 inches by 1 inch) for an industrial data logger called "Black Box". The board is dark green, features a small STM32 microcontroller, a microSD card slot with a card partially inserted, a coin cell battery holder with a CR2032 battery, several protected ADC input connectors and GPIO headers, a 5V power input, and SWD programming pads. Clean modern electronics aesthetic, well-lit studio product shot on a dark background, high detail, sharp focus orientation is landscape layout is block

<h2>The Problem</h2>
<p>Machines fail months or years after installation with intermittent, unreproducible problems. Engineers can’t recreate the issue, and the root cause is lost forever.</p>

<p>At the same time, IoT and AI startups need real-world machine data to train models. The usual solution is a Raspberry Pi + sensors + enclosure + power + networking setup that costs hundreds of dollars, is bulky, power-hungry, and often unreliable in industrial environments. The cheapest commercial “black-box” style loggers start around $500 and are still overkill or too expensive for widespread deployment.</p>

<h2>The Solution</h2>
<p><strong>Black Box</strong> is a tiny, ultra-low-cost data logger that you simply wire into a machine and leave for months or years.</p>

<h3>Core Hardware (target &lt; $20, &lt; 2" × 1")</h3>
<ul>
<li>STM32 microcontroller</li>
<li>8 protected ADC inputs + 12 GPIOs</li>
<li>microSD card for long-term storage</li>
<li>Coin-cell battery that is constantly charged from the 5 V supply</li>
<li>Programming interface (SWD / USB)</li>
</ul>

<h3>Smart Power Behavior</h3>
<ul>
<li>Runs fully from the machine’s 5 V supply while available</li>
<li>When 5 V drops, the coin cell seamlessly takes over and keeps logging for ~15 minutes</li>
<li>After that it drops into pure RTC mode (only keeps accurate time)</li>
<li>When 5 V returns, the system powers up again and continues logging with correct timestamps</li>
</ul>

<p>Everything that can be handled in firmware (power state machine, logging strategy, timekeeping, etc.) is done in firmware to keep the board simple and cheap.</p>

<h2>Product Roadmap</h2>
<ol>
<li><strong>Basic model</strong> – SD card + battery (the pure “black box”)</li>
<li><strong>Wi-Fi model</strong> – optional wireless upload</li>
<li><strong>Ethernet model</strong> – for permanent installations</li>
</ol>

<p>All variants stay under $20 in volume and smaller than 2" × 1".</p>

<h2>Software</h2>
<p>A simple cross-platform desktop application that:</p>
<ul>
<li>Reads data from many Black Boxes at once</li>
<li>Requires zero technical training</li>
<li>Lets any technician or engineer extract and analyze months/years of signals in minutes</li>
</ul>

<h2>Why It Wins</h2>
<ul>
<li><strong>25× cheaper</strong> than the cheapest comparable industrial loggers</li>
<li>Tiny enough to hide inside almost any machine</li>
<li>Survives power interruptions while keeping accurate time</li>
<li>Perfect for two high-value use cases:
  <ol>
  <li>Capturing elusive intermittent failures</li>
  <li>Cheap, scalable data collection for AI/IoT model training</li>
  </ol>
</li>
</ul>

<h2>The Ask</h2>
<p>We are raising <strong>$20,000</strong> to deliver a production-ready product that can be sold in volume. This covers:</p>
<ul>
<li>Final hardware design, testing, and certification</li>
<li>Robust firmware</li>
<li>Cross-platform extraction software</li>
<li>First production batch and initial go-to-market</li>
</ul>

<hr>

<p><em>For confidentiality reasons, the actual PCB design files, firmware source code, and software source code currently under development are not included in this repository.</em></p>

</body>
</html>