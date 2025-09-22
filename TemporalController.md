### TemporalController

The **TemporalController** is the module that decides whether ENTITÀ should speak or remain silent. Unlike traditional chatbots, which always reply, this system introduces a probabilistic logic based on three key elements:

1. **[Multi-scale EMA (Exponential Moving Average)](https://www.bing.com/search?q=what+is+ema+in+data&FORM=QSRE3)**

   * The system tracks silence and tension over multiple time scales: short, medium, and long.
   * This allows ENTITÀ to consider not only the immediate moment but also the overall trend of the scene.

2. **Internal emotional states**

   * ENTITÀ has three basic states: **curious**, **bored**, and **irritated**.
   * Each state biases the probability of speaking:

     * **Curious** → slightly more likely to respond
     * **Bored** → less likely to respond
     * **Irritated** → more likely to speak suddenly and sharply

3. **[Hysteresis](https://www.bing.com/search?qs=CT&pq=Hysteresis+&sk=CSYN1&sc=11-11&q=hysteresis+definition&cvid=ac75d3a66349444ba8fbbcd34b8c2e4e&gs_lcrp=EgRlZGdlKgYIARAAGEAyBggAEEUYOTIGCAEQABhAMgYIAhAAGEAyBggDEAAYQDIGCAQQABhAMgYIBRAAGEAyBggGEAAYQDIGCAcQABhAMgYICBAAGEDSAQgyNDAzajBqOagCALACAA&FORM=ANAB01&PC=U531) rules**

   * Emotional states do not change back and forth erratically.
   * Once ENTITÀ enters a state (e.g., irritated), it remains there for a minimum dwell time, making behavior more stable and believable.

4. **Additional constraints**

   * **Cooldown**: after speaking, ENTITÀ must wait before replying again.
   * **Rate control**: if it talks too often, probability decreases; if it stays silent for too long, probability increases.
   * **Random noise**: a small random factor keeps behavior unpredictable.

**In short:** the TemporalController allows ENTITÀ to decide **whether** to respond, not just **what** to say. This shifts the paradigm from *input → output* to *input → decision → (response | silence)*.

---

### Glossary

* **EMA (Exponential Moving Average):** a moving average that “forgets” older data and gives more weight to recent events. Used here to track tension and silence.
* **Multi-scale:** the use of multiple EMAs at different time windows (short, medium, long) to capture both quick fluctuations and long-term trends.
* **Emotional states:** internal conditions (curious, bored, irritated) that bias the probability of speaking.
* **Hysteresis:** mechanism that prevents rapid state changes, requiring a minimum dwell time before switching.
* **Cooldown:** mandatory pause after speaking to avoid excessive responses.
* **Noise:** a random component added to probability calculations to make the system less predictable.

---

### Summary Table

| **Concept**      | **Role in the system**                                    | **Effect on ENTITÀ**                                       |
| ---------------- | --------------------------------------------------------- | ---------------------------------------------------------- |
| EMA multi-scale  | Tracks silence/tension across short, medium, long windows | Builds “memory” of context, avoids purely reactive replies |
| Emotional states | Internal mood (curious, bored, irritated)                 | Biases speaking probability up or down                     |
| Hysteresis       | Prevents rapid state flipping                             | Keeps behavior stable and believable                       |
| Cooldown         | Mandatory pause after speaking                            | Limits frequency, ensures natural pacing                   |
| Rate control     | Adjusts based on how often ENTITÀ spoke recently          | Balances silence vs. verbosity                             |
| Random noise     | Adds stochastic variation                                 | Makes ENTITÀ less predictable, more “human-like”           |

---
