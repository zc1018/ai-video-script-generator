---
name: ai-video-script-generator
description: This skill should be used when the user asks to "生成视频脚本", "创建视频提示词", "AI视频分段", "视频剧本", "分镜脚本", "generate video script", "create video prompts", "segment video", or "video storyboard". Generates time-segmented prompts for AI video tools (Runway, Pika, 即梦) with character consistency and narrative coherence.
version: 0.1.0
---

# AI Video Script Generator

## Overview

Generate segmented video prompts for AI video generation tools with guaranteed character consistency, costume uniformity, and narrative coherence. This skill transforms user stories into production-ready, time-segmented prompts optimized for tools like Runway, Pika, 即梦 (Jimeng), and other text-to-video platforms.

## When to Use This Skill

Trigger this skill when the user needs:
- Segmented video prompts for AI video generation
- Character-consistent video scripts across multiple segments
- Detailed costume and appearance specifications
- Time-based scene breakdowns (e.g., 12-second segments)
- Narrative structure with logical scene transitions
- Social media video scripts (TikTok, Instagram, YouTube Shorts)

## Core Workflow

### Phase 1: Gather Requirements

Collect essential information through targeted questions:

**1. Characters and Roles**
Ask: "Who are the characters in your video? Please describe each character's role and basic traits."

Collect for each character:
- Name and role (e.g., "Father, pilot")
- Age and basic appearance
- Personality traits relevant to the story

**2. Story Background and Theme**
Ask: "What's the story background and overall theme? What style are you aiming for?"

Options to present:
- A. Warm family moments
- B. Professional/inspirational
- C. Humorous/comedic
- D. Mixed style

**3. Technical Specifications**
Ask: "What are the technical requirements?"

Collect:
- Total video duration (e.g., 2 minutes)
- Single prompt duration (e.g., 12 seconds)
- Target platform (TikTok, YouTube, Instagram, etc.)
- Video generation tool (Runway, Pika, 即梦, etc.)

**4. Reference Material (Optional)**
Ask: "Do you have any reference videos, scripts, or style guides?"

### Phase 2: Define Character Specifications

Create detailed character specifications with costume consistency:

**Character Template:**
```
### Character Name (Role)
**Identity**: [Role description]
**Costume Details** (must remain consistent across all segments):
- Primary color: [Specific color]
- Upper garment: [Detailed description]
- Lower garment: [Detailed description]
- Accessories: [Specific items with colors]
- Footwear: [Type and color]
- Hairstyle: [Specific style]
**Personality**: [Key traits]
```

**Critical Rule**: Every costume detail must be specified with exact colors, styles, and accessories. This specification will be repeated in every segment's character definition to ensure AI consistency.

### Phase 3: Structure the Narrative

Calculate segment breakdown:
- Total segments = Total duration ÷ Single prompt duration
- Example: 120 seconds ÷ 12 seconds = 10 segments

Design three-act structure:
1. **Setup** (30% of segments): Introduce characters, establish setting
2. **Development** (40% of segments): Main action, conflicts, interactions
3. **Resolution** (30% of segments): Climax, conclusion, emotional payoff

For each segment, define:
- Scene location and atmosphere
- Character actions and interactions
- Emotional tone
- Comedic/dramatic beats
- Transition to next segment

### Phase 4: Generate Segmented Prompts

For detailed prompt patterns, camera angles, and emotional keywords, consult `references/prompt-patterns.md`.

For each segment, create structured prompts with:

**1. Character Definition Block** (appears at the start of every segment)
```
**角色定义：**
- Character 1: [Full costume specification from Phase 2]
- Character 2: [Full costume specification from Phase 2]
- Character 3: [Full costume specification from Phase 2]
```

**2. Time-Based Action Breakdown**
Break the segment into sub-intervals (e.g., for 12-second segments, use 3-second intervals):

```
**0-3秒：**
- 场景：[Detailed scene description]
- 镜头：[Camera angle: 全景/中景/近景/特写]
- 动作：[Specific character actions]

**3-6秒：**
- 镜头：[Camera transition]
- 动作：[Character actions and interactions]

**6-9秒：**
- 镜头：[Camera angle]
- 动作：[Character actions]

**9-12秒：**
- 镜头：[Camera angle]
- 动作：[Character actions and emotional beats]
```

**3. Highlight Key Moments**
```
**搞笑点/亮点**：[Describe the comedic beat, emotional moment, or visual highlight]
```

### Phase 5: Document and Deliver

Create a comprehensive design document with:

1. **Project Overview**: Summary of concept, duration, style
2. **Character Specifications**: Detailed costume and personality specs
3. **Story Structure**: Three-act breakdown with segment allocation
4. **Detailed Segment Prompts**: All segments with character definitions and time breakdowns
5. **Production Notes**:
   - Character consistency guidelines
   - Platform-specific recommendations
   - Post-production suggestions

Save the document as: `docs/plans/YYYY-MM-DD-[project-name]-script.md`

## Key Principles

### 1. Character Consistency is Critical

**Problem**: AI video tools often generate inconsistent character appearances across segments.

**Solution**:
- Define exact costume specifications once
- Repeat full specifications in every segment's character definition
- Use specific colors, not generic terms (e.g., "深蓝色" not "蓝色")
- Include all accessories and details

### 2. Progressive Disclosure in Prompts

Structure prompts from general to specific:
1. Scene setting (location, lighting, atmosphere)
2. Camera angle (establishing context)
3. Character actions (specific movements)
4. Emotional beats (reactions, expressions)

### 3. Narrative Coherence

Ensure logical flow between segments:
- Each segment should end with a natural transition point
- Actions should have cause-and-effect relationships
- Emotional arcs should build progressively
- Callbacks and payoffs should be planned

### 4. Platform Optimization

Tailor content for target platforms:
- **TikTok/Douyin**: Fast-paced, hook in first 3 seconds, vertical format
- **YouTube Shorts**: Slightly longer setup, clear narrative arc
- **Instagram Reels**: Visual aesthetics, trending audio consideration

## Chinese Prompt Best Practices

For detailed Chinese prompt techniques, consult `references/prompt-patterns.md`.

Key points:
- Use specific colors: "深蓝色飞行员制服" not "制服"
- Specify camera angles: 全景/中景/近景/特写/远景
- Include emotional keywords: 温馨/搞笑/紧张/兴奋
- Describe lighting: 明亮的/柔和的/金色阳光
- Use action verbs: 走来/跑过来/转身/蹲下来

## Common Pitfalls to Avoid

For comprehensive pitfall patterns, see `references/prompt-patterns.md`.

Critical mistakes:
- ❌ Vague costumes → ✅ Detailed specifications with exact colors
- ❌ Inconsistent definitions → ✅ Copy exact specs to every segment
- ❌ Missing time breakdowns → ✅ Break into 3-second intervals
- ❌ Weak narrative → ✅ Clear three-act structure
- ❌ Generic scenes → ✅ Detailed atmosphere and lighting

## Additional Resources

### Reference Files

For detailed guidance and techniques:
- **`references/best-practices.md`** - AI video generation best practices, platform-specific tips
- **`references/prompt-patterns.md`** - Effective prompt patterns, camera angles, emotional keywords

### Example Files

Complete working examples:
- **`examples/family-aviation-story.md`** - Full 2-minute family video script with 10 segments

## Workflow Summary

1. **Gather Requirements** → Characters, story, technical specs, references
2. **Define Characters** → Detailed costume specifications for consistency
3. **Structure Narrative** → Calculate segments, design three-act structure
4. **Generate Prompts** → Character definitions + time-based breakdowns for each segment
5. **Document** → Comprehensive design document with production notes

Focus on character consistency through detailed specifications, narrative coherence through structured planning, and platform optimization through targeted formatting.
