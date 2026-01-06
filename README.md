# qzhls-server-authority-kit
A strict server-authoritative action framework for Roblox  that enforces intent-based networking and state control.

# Core
> **Clients express intent. 
> Servers decide outcomes.**

qzhl's server authority kit assumes
- Clients are **untrusted**
- Network paylods are **hostile**
- State mutations are **explicit and gated**
- Every action must be **validated, rate-limitied, and authorized**

If any assumptions do not align with your game, the framework is **not for your game**.

# Guarntees
qzhl's server-authority kit gurantees;

- The **server is the sole owner of game state**
- Clients cannot directly execute gameplay logic
- All client requests are trated as **intents**, never commands
- ALl intents pass through:
   - Validation
   - Authorization
   - Rate limiting
   - State changes are **deterministic and auditable**
   - No implicit replication or trust-based shortcuts

   If any of these gunatees are broken, the framework is being misused.

   # When to Use

   qzhl's server-authoirty framework is recommended for:

   - Competitive PvP games
   - Ability-based combat systems
   - Match-based of session-based games
   - Anti-exploit-critical projects
   - Backend-heavy Roblox games
   - Studios enforcing engineering standards

   # When NOT to use
Do **not** use this framework if:

- Your game is a simple obby or tycoon
- You rely on client-driven gameplay (Never trust the client)
- You prioritize rapid prototyping over security
- You are unfamilar with server-authoritative design

qzhl's server authority framework is for correctness instead of simplicity.

# Installation

# Rojo / Package Usage

Place the repository in your project and expose it via Rojo

# Lua
local ServerAuthority = require(pathto["qzhls-server-authority-kit"])

