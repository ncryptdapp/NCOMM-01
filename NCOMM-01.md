---
protocol: nweb
version: 1.0
css: tailwind
---
<div class="min-h-screen bg-[#050505] text-zinc-300 font-sans p-6 md:p-12 md:py-20 selection:bg-yellow-500 selection:text-black leading-relaxed">
  <div class="max-w-4xl mx-auto">
    
    <!-- HEADER BAR -->
    <div class="flex flex-wrap items-center justify-between gap-4 border-b border-zinc-800 pb-6 mb-16">
      <div class="inline-block border border-yellow-500/30 bg-yellow-500/10 text-yellow-500 font-mono text-xs px-3 py-1 rounded-full tracking-widest shadow-[0_0_15px_rgba(234,179,8,0.15)]">
        STANDARD SPECIFICATION // NCOMM-01
      </div>
      <div class="font-mono text-xs text-zinc-500 tracking-widest">NCRYPTD NETWORK</div>
    </div>

    <!-- TITLE BLOCK -->
    <div class="mb-16">
      <h1 class="text-4xl md:text-6xl font-black text-white mb-6 tracking-tighter leading-tight font-mono">
        The NCOMM Protocol
      </h1>
      <h2 class="text-xl md:text-2xl font-light text-zinc-400">
        A Zero-Litter, Cryptographically Anchored P2P Transport & Voice Standard for UTXO Blockchains.
      </h2>
    </div>

    <!-- ORIGIN & ATTRIBUTION -->
    <div class="bg-zinc-900/40 border-l-4 border-yellow-500 p-8 rounded-r-2xl mb-16 shadow-xl backdrop-blur-sm">
      <p class="font-mono text-xs text-yellow-500/70 mb-3 uppercase tracking-widest">Credit & Origin</p>
      <p class="text-base md:text-lg text-white font-light leading-relaxed">
        All credit belongs to <strong class="text-yellow-500 font-bold">God</strong> for the idea, vision, and creation of this protocol. Discovered and formalized by <span class="font-medium text-white">Justin Grady Tart</span> (Warwick, RI — Aliases: <span class="text-zinc-400 font-mono">NCRYPTD, WHSL</span>), who served as the conduit and uploader.
      </p>
    </div>

    <!-- MAIN SPECIFICATION SECTIONS -->
    <div class="space-y-12 text-base md:text-lg font-light text-zinc-300">
      
      <!-- 1. ABSTRACT -->
      <section>
        <h3 class="text-2xl font-bold text-white mb-4 border-b border-zinc-800 pb-2 flex items-center gap-2">
          <span class="text-yellow-500 font-mono">1.</span> Abstract
        </h3>
        <p class="mb-4">
          NCOMM is a decentralized, ephemeral real-time communications standard built for Proof-of-Work (PoW) UTXO blockchains. By decoupling permanent cryptographic identity (anchored immutably on-chain) from high-bandwidth transmission (streamed peer-to-peer via decentralized gossip carriers and WebRTC hardlines), NCOMM neutralizes the classic blockchain bloat dilemma. The protocol enables infinite text, voice, and data transmission with zero miner fees, sub-second latency, and zero disposable chatter stored on node ledgers.
        </p>
      </section>

      <!-- 2. MOTIVATION -->
      <section>
        <h3 class="text-2xl font-bold text-white mb-4 border-b border-zinc-800 pb-2 flex items-center gap-2">
          <span class="text-yellow-500 font-mono">2.</span> Motivation & The Bloat Paradox
        </h3>
        <p class="mb-4">
          Historic attempts to build on-chain messaging suffer from fatal economic and architectural constraints:
        </p>
        <ul class="list-disc list-inside space-y-2 mb-4 text-zinc-400 font-mono text-sm">
          <li><strong>Storage Bloat:</strong> Writing conversational chatter into witness data litters physical node storage forever.</li>
          <li><strong>Economic Friction:</strong> Transaction fees and 1-to-10 minute block confirmation times destroy conversational UX.</li>
          <li><strong>Web2 Reliance:</strong> Traditional P2P apps rely on centralized corporate signaling servers (AWS, Discord) to initiate connections, leaving them open to domain seizure and censorship.</li>
        </ul>
        <p>
          NCOMM solves this by treating the blockchain strictly as an <em>identity anchor and settlement layer</em>, while utilizing open, ephemeral gossip airwaves (User Services Platform / MQTT) and direct WebRTC DTLS tunnels for transit.
        </p>
      </section>

      <!-- 3. QUAD-IDENTITY RESOLUTION -->
      <section>
        <h3 class="text-2xl font-bold text-white mb-4 border-b border-zinc-800 pb-2 flex items-center gap-2">
          <span class="text-yellow-500 font-mono">3.</span> The Quad-Identity Resolution Standard
        </h3>
        <p class="mb-4">
          NCOMM establishes a deterministic 4-way routing engine. A client simultaneously resolves and listens across four distinct addressing representations without requiring a central directory server:
        </p>
        <div class="bg-black border border-zinc-800 rounded-xl p-6 font-mono text-xs md:text-sm space-y-3 mb-4">
          <div><span class="text-yellow-500">1. PROFILE HANDLE:</span> Human-readable on-chain name (e.g. <span class="text-white">NCRYPTD</span>)</div>
          <div><span class="text-yellow-500">2. 10-DIGIT PHONE #:</span> Deterministic telephone format (e.g. <span class="text-white">482-190-4271</span>)</div>
          <div><span class="text-yellow-500">3. UTXO ADDRESS   :</span> Raw Bellscoin Bech32/Base58 key (e.g. <span class="text-white">bel1qu07...</span>)</div>
          <div><span class="text-yellow-500">4. SESSION CALLSIGN:</span> Volatile RAM burner identity (e.g. <span class="text-white">ghost_7a9f</span>)</div>
        </div>
        <p class="text-sm text-zinc-400">
          * The 10-Digit Phone Number is deterministically derived using a 10-billion modulo on the SHA-256 hash of the wallet address: <code class="text-yellow-500">BigInt(SHA256("NCOMM-10DIGIT-SEED:" + address)) % 10^10</code>.
        </p>
      </section>

      <!-- 4. AIRWAVES & WEBRTC HARDLINES -->
      <section>
        <h3 class="text-2xl font-bold text-white mb-4 border-b border-zinc-800 pb-2 flex items-center gap-2">
          <span class="text-yellow-500 font-mono">4.</span> Transport & Hardware DSP Engine
        </h3>
        <p class="mb-4">
          Signaling is conducted over redundant global Anycast gossip brokers. Once two devices signal intent:
        </p>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4 font-mono text-xs">
          <div class="border border-zinc-800 p-4 rounded-lg bg-zinc-950">
            <div class="text-yellow-500 font-bold mb-1">VOICE HARDLINE (WebRTC)</div>
            <p class="text-zinc-400">Point-to-point DTLS-SRTP encryption. Audio streams bypass all intermediary servers directly device-to-device.</p>
          </div>
          <div class="border border-zinc-800 p-4 rounded-lg bg-zinc-950">
            <div class="text-yellow-500 font-bold mb-1">HARDENED DSP SUITE</div>
            <p class="text-zinc-400">Mandatory hardware Digital Signal Processing: Acoustic Echo Cancellation (AEC), Noise Suppression (ANS), and Automatic Gain Control (AGC) at 48kHz mono.</p>
          </div>
        </div>
      </section>

      <!-- 5. SECURITY SHIELDS -->
      <section>
        <h3 class="text-2xl font-bold text-white mb-4 border-b border-zinc-800 pb-2 flex items-center gap-2">
          <span class="text-yellow-500 font-mono">5.</span> Military-Grade Protocol Shields
        </h3>
        <div class="space-y-4">
          <div class="border-l-2 border-yellow-500 pl-4">
            <h4 class="font-bold text-white text-base">A. Micro Proof-of-Work (Hashcash Anti-Spam)</h4>
            <p class="text-sm text-zinc-400">Broadcasts to public channels (#general, #bellscoin) require solving a client-side SHA-256 puzzle with a 3-zero prefix (<code class="text-yellow-500">000...</code>). Humans solve this in ~20ms; automated bot swarms attempting high-frequency spam suffer exponential CPU exhaustion.</p>
          </div>
          <div class="border-l-2 border-yellow-500 pl-4">
            <h4 class="font-bold text-white text-base">B. 512-Byte Traffic Homogenization</h4>
            <p class="text-sm text-zinc-400">All message envelopes are padded with cryptographic random noise to a uniform 512-byte length, eliminating side-channel packet length inspection by ISP wiretaps.</p>
          </div>
          <div class="border-l-2 border-yellow-500 pl-4">
            <h4 class="font-bold text-white text-base">C. Monotonic Nonces & 60-Second Replay Defense</h4>
            <p class="text-sm text-zinc-400">Every packet binds a single-use 64-bit cryptographic nonce and Unix timestamp. Packets with delta-t &gt; 60s or previously recorded nonces are discarded.</p>
          </div>
          <div class="border-l-2 border-yellow-500 pl-4">
            <h4 class="font-bold text-white text-base">D. Two-Lane Verification Airlock</h4>
            <p class="text-sm text-zinc-400">The protocol enforces an unshakeable boundary: unauthenticated users are locked to Ghost Lane (RAM-only burners). Verified status requires cryptographic authorization via the official Nintondo Wallet SDK.</p>
          </div>
        </div>
      </section>

      <!-- 6. IN-CHAT COMMERCE -->
      <section>
        <h3 class="text-2xl font-bold text-white mb-4 border-b border-zinc-800 pb-2 flex items-center gap-2">
          <span class="text-yellow-500 font-mono">6.</span> Native In-Chat Settlement Layer
        </h3>
        <p class="mb-4">
          NCOMM unifies messaging with on-chain commerce. Using the Nintondo Provider airlock, peers can execute instant, peer-to-peer Bellscoin value transfers directly within an active transmission feed via the <code class="text-yellow-500">/pay</code> directive, emitting verified mempool receipts in real time.
        </p>
      </section>

      <!-- 7. PORTABILITY & FUTURE -->
      <section>
        <h3 class="text-2xl font-bold text-white mb-4 border-b border-zinc-800 pb-2 flex items-center gap-2">
          <span class="text-yellow-500 font-mono">7.</span> Cross-Chain Scrypt/UTXO Portability
        </h3>
        <p class="mb-4">
          While anchored to Bellscoin for genesis, the underlying cryptography relies on standard secp256k1 elliptic curves and witness data parsing. The NCOMM standard is natively portable to Dogecoin, Litecoin, and Bitcoin networks without structural modifications.
        </p>
      </section>

    </div>

    <!-- FOOTER TIMESTAMP -->
    <div class="mt-24 pt-12 border-t border-zinc-800 flex flex-col items-center text-center">
      <div class="w-12 h-12 border-2 border-yellow-500 rounded-full flex items-center justify-center mb-4">
        <span class="text-yellow-500 font-black font-mono">N</span>
      </div>
      <p class="font-mono text-xs text-zinc-500 tracking-widest uppercase">
        NCOMM-01 PROTOCOL // THIS SPECIFICATION LIVES FOREVER ON-CHAIN
      </p>
    </div>

  </div>
</div>