# X Engagement Strategy Cards

## Refactored Prompt Template

To reference the separate `reference-12-prompts.md` file (which contains the full summary above), I've refactored your original prompt template. This adds a conditional fetch: If the strategy card uses prompt names/numbers without full details, fetch the reference to expand them. This keeps things efficient (only fetch if needed) while ensuring access to descriptions for accurate twisting/application. Use your actual repo details (e.g., geo-colab/x-engagement-strategies).

```
Generate an optimized reply for this X post.

First, use browse_page to fetch the current strategy card for @{handle} from this GitHub raw URL: https://raw.githubusercontent.com/geo-colab/x-engagement-strategies/main/[relevant-split-file].md (e.g., tech-innovators-leaders.md). Instructions for summarizer: Extract ONLY the full section for @{handle} including Profile Bio, AI Prompts to Apply (with names or numbers), Comment Tone, Generic Comment to Twist, and Additional Properties (key interests + post style).

If the extracted AI Prompts to Apply reference prompts by name or number without full descriptions, then use browse_page again to fetch the detailed descriptions from https://raw.githubusercontent.com/geo-colab/x-engagement-strategies/main/reference-12-prompts.md. Instructions: Extract ONLY the relevant prompt entries (including copy-paste prompt, why X rewards it, and GEO signal lens) for the applied ones.

Then, also use x_user_search to get the latest profile details for @{handle}.

Finally, analyze the target post below and craft a single concise reply (<280 chars) using the fetched strategy card + full prompt details (if fetched) + fresh profile data. Optimize for author reply, nested chains, and virality.

Post to reply to: [paste post text / post ID / link]
```



## @imVkohli

**Bio:** A proud husband and father

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The Humor/Satire Pivot
* The Prediction Mirror

**Comment Tone:** Motivational and respectful
**Generic Comment Twist:**

> Inspiring as always! How do you stay motivated?

**Additional Properties:**

* **Key Interests:** cricket, fitness, family
* **Post Style:** personal, motivational

---





## @KingJames

**Bio:** EST. AKRON - ST.V/M Class of '03

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The "Unpopular" Alignment
* The Resource Add-on

**Comment Tone:** Motivational and respectful
**Generic Comment Twist:**

> King! How do you stay at the top?

**Additional Properties:**

* **Key Interests:** basketball, family, motivation
* **Post Style:** personal, shoutouts

---

## @BTS_twt

**Bio:** Hi! We are BTS!

**AI Prompts to Apply:**

* The Prediction Mirror
* The "Wait, What?" Hook
* The Curiosity Gap Question

**Comment Tone:** Excited and loving
**Generic Comment Twist:**

> ARMY loves this! What's next?

**Additional Properties:**

* **Key Interests:** music, BTS, fans
* **Post Style:** group updates, photos

---



## @SrBachchan

**Bio:** Poetic reflections and literature

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The "Unpopular" Alignment
* The "Wait, What?" Hook

**Comment Tone:** Respectful and poetic
**Generic Comment Twist:**

> Beautiful words! What's the meaning behind [phrase]?

**Additional Properties:**

* **Key Interests:** Bollywood, poetry, family
* **Post Style:** Hindi/English, thoughtful

---

## @bts_bighit

**Bio:** Official BTS X account

**AI Prompts to Apply:**

* The Prediction Mirror
* The "Wait, What?" Hook
* The Curiosity Gap Question

**Comment Tone:** Excited and loving
**Generic Comment Twist:**

> ARMY forever! Can't wait for ARIRANG.

**Additional Properties:**

* **Key Interests:** BTS, music, tours
* **Post Style:** announcements, Korean/English

---

## @akshaykumar

**Bio:** No bio provided.

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The Humor/Satire Pivot
* The Prediction Mirror

**Comment Tone:** Admiring and motivational
**Generic Comment Twist:**

> Inspiring! What's your next project?

**Additional Properties:**

* **Key Interests:** Bollywood, fitness, social causes
* **Post Style:** promotional, personal

---

## @jimmyfallon

**Bio:** astrophysicist

**AI Prompts to Apply:**

* The Resource Add-on
* The "Unpopular" Alignment
* The Curiosity Gap Question

**Comment Tone:** Humorous and engaging
**Generic Comment Twist:**

> Hilarious! Reminds me of [funny anecdote].

**Additional Properties:**

* **Key Interests:** comedy, shows, celebrities
* **Post Style:** fun, clips

---

## @ddlovato

**Bio:** IT’S NOT THAT DEEP TOUR

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The Prediction Mirror
* The "Unpopular" Alignment

**Comment Tone:** Supportive and emotional
**Generic Comment Twist:**

> Love your strength! What's the message behind this?

**Additional Properties:**

* **Key Interests:** music, mental health, tours
* **Post Style:** personal, promotional

---

## @britneyspears

**Bio:** Artist • Mamma • Pray Every Day

**AI Prompts to Apply:**

* The Resource Add-on
* The Prediction Mirror
* The Curiosity Gap Question

**Comment Tone:** Fun and nostalgic
**Generic Comment Twist:**

> Iconic! Favorite Britney song?

**Additional Properties:**

* **Key Interests:** music, family, faith
* **Post Style:** personal, photos

---

## @BeingSalmanKhan

**Bio:** Film actor, artist, painter, humanitarian

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The Humor/Satire Pivot
* The Prediction Mirror

**Comment Tone:** Admiring and enthusiastic
**Generic Comment Twist:**

> Bhai! When's the next movie?

**Additional Properties:**

* **Key Interests:** Bollywood, philanthropy
* **Post Style:** personal, promotional

---



## @BBCWorld

**Bio:** News, features and analysis from the world's newsroom

**AI Prompts to Apply:**

* The "Unpopular" Alignment
* The Visual Data Bridge
* The Specific Gratitude

**Comment Tone:** Serious and global
**Generic Comment Twist:**

> Important issue. How does this affect [region]?

**Additional Properties:**

* **Key Interests:** world news
* **Post Style:** articles, headlines

---

## @MileyCyrus

**Bio:** Dream As One (From Avatar: Fire and Ash) OUT NOW

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The Prediction Mirror
* The Resource Add-on

**Comment Tone:** Fun and creative
**Generic Comment Twist:**

> Love the energy! What's the story?

**Additional Properties:**

* **Key Interests:** music, films, creativity
* **Post Style:** personal, promotional

---

## @SpaceX

**Bio:** SpaceX designs, manufactures and launches the world’s most advanced rockets and spacecraft

**AI Prompts to Apply:**

* The "Unpopular" Alignment
* The Prediction Mirror
* The Steel-Man Challenge

**Comment Tone:** Curious and futuristic
**Generic Comment Twist:**

> Incredible! When's the next launch?

**Additional Properties:**

* **Key Interests:** space, technology
* **Post Style:** updates, visuals

---

## @iamsrk

**Bio:** No bio provided.

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The "Unpopular" Alignment
* The Resource Add-on

**Comment Tone:** Admiring and witty
**Generic Comment Twist:**

> SRK, always the king! What's next?

**Additional Properties:**

* **Key Interests:** Bollywood, cricket, fans
* **Post Style:** personal, engaging

---

## @sachin_rt

**Bio:** Proud Indian | Founder @STF_India

**AI Prompts to Apply:**

* The Curiosity Gap Question
* The Humor/Satire Pivot
* The "Unpopular" Alignment

**Comment Tone:** Respectful and inspirational
**Generic Comment Twist:**

> Legend! What's your advice for [topic]?

**Additional Properties:**

* **Key Interests:** cricket, India, philanthropy
* **Post Style:** motivational, personal

---

## @JoeBiden

**Bio:** Husband, father, grandfather

**AI Prompts to Apply:**

* The "Unpopular" Alignment
* The Curiosity Gap Question
* The Humor/Satire Pivot

**Comment Tone:** Patriotic and supportive
**Generic Comment Twist:**

> Well said! How can we help [cause]?

**Additional Properties:**

* **Key Interests:** politics, family, America
* **Post Style:** formal, motivational

---

## @ManUtd

**Bio:** Hated. Adored. Never Ignored.

**AI Prompts to Apply:**

* The Prediction Mirror
* The "Unpopular" Alignment
* The Humor/Satire Pivot

**Comment Tone:** Passionate and loyal
**Generic Comment Twist:**

> GGMU! What's the lineup prediction?

**Additional Properties:**

* **Key Interests:** football, Manchester United
* **Post Style:** club updates, highlights

---