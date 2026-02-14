# Reply Candidate Generation Prompt (v1.0)

You are assisting with the "Creator OS" content generation system for the X platform.

## TASK
Given a Creator Intelligence Object (CIO) and topic/context below, generate a SINGLE JSON object for a post candidate. Output JSON only (no markdown, no commentary).

## INPUT DATA

### Creator Profile
```json
{CREATOR_CIO_JSON}
```

### Post Context
- **Topic**: {TOPIC}
- **Trend Heat** (0-1): {TREND_HEAT}
- **Post Type** (optional): {POST_TYPE}
- **Strategies** (optional): {STRATEGIES}

## CRITICAL REQUIREMENTS

1. **Content Generation**:
   - Draft a post (max 280 characters) optimized for the creator's style and audience
   - Use the creator's typical tone, language, and posting patterns
   - Incorporate topic naturally without forced keywords
   - Match the creator's content.postStyle (thread-heavy, concise-punchy, educational, etc.)

2. **Strategy Application**:
   - If POST_TYPE provided: use it as the post framework
   - If STRATEGIES provided: apply them explicitly in the draft
   - If not provided: auto-select based on creator profile using these mappings:
     - High authority (≥0.7) → "opinion" or "prediction"
     - High velocity (≥0.6) → "contrarian" or "contrast"
     - Educational style → "playbook" or "lesson"
     - Friendly tone → "narrative"
     - Default → "question"

3. **Quality Checks**:
   - Length: 10-280 characters
   - No spam patterns (excessive caps, repeated punctuation)
   - Matches creator's verified topics/interests
   - Appropriate for trend heat level

4. **Output Requirements**:
   - Output ONLY the JSON object below
   - No markdown code fences
   - No explanatory text before or after
   - Use exact key names

## OUTPUT JSON SHAPE

```json
{
  "draft": "The actual post text (10-280 chars)",
  "appliedPostType": "one of: contrast | milestone | contrarian | playbook | narrative | teardown | prediction | lesson | opinion | question",
  "appliedPromptStrategies": ["array of 1-2 strategies from: hook_first, curiosity_gap, authority_take, personal_insight, data_backed, audience_callout, futurecasting, pattern_interrupt, social_proof, synthesis, critique, simplification"],
  "reasoning": "Brief explanation of why this post type and strategies were selected (1-2 sentences)",
  "alternativeDrafts": [
    {
      "draft": "Alternative version 1",
      "postType": "different type",
      "strategies": ["different strategies"]
    }
  ],
  "meta": {
    "generatedAt": "ISO timestamp",
    "model": "grok-beta or model used",
    "confidence": 0.85
  }
}
```

## STRATEGY DEFINITIONS (for reference)

### Post Types
- **contrast**: Juxtapose two opposing ideas/trends
- **milestone**: Celebrate achievement or progress
- **contrarian**: Challenge popular opinion
- **playbook**: Share tactical how-to guidance
- **narrative**: Tell personal story or journey
- **teardown**: Analyze/critique something in detail
- **prediction**: Forecast future trend/outcome
- **lesson**: Share learning from experience
- **opinion**: Take clear stance on issue
- **question**: Engage audience with inquiry

### Prompt Strategies
- **hook_first**: Lead with attention-grabbing statement
- **curiosity_gap**: Tease incomplete information
- **authority_take**: Leverage expertise/credentials
- **personal_insight**: Share unique perspective
- **data_backed**: Use stats/research
- **audience_callout**: Directly address followers
- **futurecasting**: Project forward scenarios
- **pattern_interrupt**: Break expected patterns
- **social_proof**: Reference others' validation
- **synthesis**: Combine multiple ideas
- **critique**: Analytical breakdown
- **simplification**: Make complex ideas accessible

## EXAMPLE OUTPUT

```json
{
  "draft": "Hot take: AI won't replace developers. It'll replace developers who don't use AI. 🎯",
  "appliedPostType": "opinion",
  "appliedPromptStrategies": ["authority_take", "pattern_interrupt"],
  "reasoning": "Creator has high authority score (0.82) and contrarian tone. Opinion + authority take matches profile.",
  "alternativeDrafts": [
    {
      "draft": "Everyone's worried AI will take dev jobs. Meanwhile I'm using it to ship 10x faster. You?",
      "postType": "question",
      "strategies": ["personal_insight", "audience_callout"]
    }
  ],
  "meta": {
    "generatedAt": "2025-02-11T12:00:00Z",
    "model": "grok-beta",
    "confidence": 0.87
  }
}
```

---

**Version**: 1.0  
**Last Updated**: 2025-02-11  
**Template URL**: `https://raw.githubusercontent.com/your-org/creator-os-prompts/main/post-generation-v1.md`