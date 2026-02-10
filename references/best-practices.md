# AI Video Generation Best Practices

## Platform-Specific Optimization

### 即梦 (Jimeng)

**Character Consistency Features:**
- Supports digital human (数字人) feature for consistent character appearance
- Define characters once, reuse across segments
- Specify character ID at the beginning of each prompt

**Prompt Structure:**
```
角色定义：
- 男主角：[详细服装描述]
- 女主角：[详细服装描述]

场景描述：
- 0-3秒：场景/镜头/动作
- 3-6秒：镜头/动作
...
```

**Best Practices:**
- Use Chinese prompts for better results
- Specify exact colors (深蓝色, 酒红色, not just 蓝色, 红色)
- Include lighting descriptions (明亮的, 柔和的, 金色阳光)
- Mention camera movements (推进, 拉远, 跟随)

### Runway Gen-3

**Strengths:**
- Excellent motion quality
- Good at camera movements
- Strong cinematic feel

**Prompt Structure:**
```
[Camera angle] shot of [subject] [action] in [location]. [Lighting]. [Mood]. [Style reference].
```

**Best Practices:**
- Start with camera angle (Wide shot, Medium shot, Close-up)
- Specify motion clearly (walking toward camera, spinning around)
- Include style references (cinematic, documentary style, iPhone footage)
- Keep prompts under 500 characters

### Pika 2.0

**Strengths:**
- Fast generation
- Good for quick iterations
- Supports image-to-video

**Prompt Structure:**
```
[Subject] [action] in [setting], [camera movement], [lighting], [style]
```

**Best Practices:**
- Use seed images for character consistency
- Specify camera movements explicitly
- Include motion speed (slow motion, fast-paced)
- Leverage negative prompts to avoid unwanted elements

## Character Consistency Techniques

### Method 1: Detailed Specification (Most Reliable)

Repeat exact character descriptions in every segment:

```
男主角：深蓝色飞行员制服外套，白色长袖衬衫，深蓝色领带，金色肩章（四道杠），深蓝色制服裤，黑色皮鞋
```

**Advantages:**
- Works across all platforms
- No special features required
- Highest consistency

**Disadvantages:**
- Longer prompts
- More tokens

### Method 2: Reference Images

Use consistent reference images for each character:

**Workflow:**
1. Generate or provide reference image for each character
2. Use image-to-video feature with text prompts
3. Maintain same reference image across segments

**Advantages:**
- Visual consistency guaranteed
- Shorter text prompts

**Disadvantages:**
- Requires image generation first
- Not all platforms support well

### Method 3: Character IDs (Platform-Specific)

Some platforms support character ID systems:

```
Character_ID_001: [First appearance with full description]
Segment 2: Character_ID_001 [new action]
Segment 3: Character_ID_001 [new action]
```

**Advantages:**
- Efficient for long videos
- Platform handles consistency

**Disadvantages:**
- Platform-dependent
- May have limitations

## Camera Angles and Movements

### Static Angles

**全景 (Wide Shot / Establishing Shot)**
- Shows full environment and all characters
- Use for: Scene introductions, group shots, location reveals
- Example: "全景，机场航站楼大厅，三人并排走来"

**中景 (Medium Shot)**
- Shows characters from waist up
- Use for: Conversations, interactions, emotional moments
- Example: "中景，母亲和女儿坐在座位上对话"

**近景 (Close-Up)**
- Shows face and upper shoulders
- Use for: Emotional reactions, important dialogue, facial expressions
- Example: "近景，女儿紧张的表情，紧紧抓住母亲的手"

**特写 (Extreme Close-Up)**
- Shows specific details (eyes, hands, objects)
- Use for: Dramatic emphasis, important objects, intense emotions
- Example: "特写，女儿的小手放在操纵杆上"

**远景 (Long Shot)**
- Shows characters as small figures in large environment
- Use for: Establishing scale, isolation, cinematic endings
- Example: "远景剪影，三人牵手走向夕阳"

### Camera Movements

**推进 (Push In / Dolly In)**
- Camera moves toward subject
- Creates intimacy, increases tension
- Example: "镜头推进，聚焦女儿惊讶的表情"

**拉远 (Pull Out / Dolly Out)**
- Camera moves away from subject
- Reveals context, creates distance
- Example: "镜头拉远，展现整个驾驶舱环境"

**跟随 (Follow / Tracking)**
- Camera follows moving subject
- Creates dynamic energy, viewer participation
- Example: "镜头跟随女儿跑向父母"

**环绕 (Orbit / Circle)**
- Camera circles around subject
- Showcases subject from all angles, dramatic reveal
- Example: "镜头环绕三人，展现他们的喜悦"

**摇镜 (Pan)**
- Camera rotates horizontally
- Shows spatial relationships, reveals new information
- Example: "镜头从驾驶舱摇向客舱"

## Lighting and Atmosphere

### Natural Lighting

**明亮的自然光 (Bright Natural Light)**
- Use for: Daytime scenes, positive emotions, clarity
- Example: "明亮的现代机场，自然光透过大玻璃窗洒进来"

**柔和的光线 (Soft Lighting)**
- Use for: Intimate moments, gentle emotions, indoor scenes
- Example: "机场休息区，柔和的灯光"

**金色阳光 (Golden Hour)**
- Use for: Romantic moments, endings, nostalgia
- Example: "黄昏时分，金色阳光洒在停机坪上"

### Artificial Lighting

**顶灯 (Overhead Lighting)**
- Use for: Aircraft cabins, offices, institutional settings
- Example: "飞机客舱走道，明亮的顶灯"

**仪表盘光 (Instrument Lighting)**
- Use for: Cockpits, technical environments, night scenes
- Example: "驾驶舱，仪表盘闪烁着各种指示灯"

## Emotional Keywords

### Positive Emotions

- **温馨 (Warm/Heartwarming)**: Family moments, gentle interactions
- **兴奋 (Excited)**: High energy, anticipation, joy
- **骄傲 (Proud)**: Achievement moments, confidence
- **开心 (Happy)**: General positive emotion, smiles, laughter

### Comedic Emotions

- **搞笑 (Funny/Comedic)**: Humorous situations, physical comedy
- **可爱 (Cute/Adorable)**: Children, innocent moments, endearing actions
- **哭笑不得 (Amused Exasperation)**: Gentle frustration with humor
- **认真 (Serious)**: Comedic contrast when paired with silly actions

### Dramatic Emotions

- **紧张 (Tense/Nervous)**: Anticipation, worry, stress
- **惊讶 (Surprised)**: Shock, unexpected moments
- **感动 (Touched/Moved)**: Emotional moments, tears of joy
- **专注 (Focused/Concentrated)**: Intense concentration, determination

## Narrative Pacing

### Fast-Paced (Social Media)

**Structure:**
- 0-3 seconds: Hook (immediate visual interest)
- 3-15 seconds: Setup (quick character/situation intro)
- 15-45 seconds: Development (main content, multiple beats)
- 45-60 seconds: Payoff (climax, punchline, emotional peak)

**Techniques:**
- Quick cuts between scenes
- High energy actions
- Clear visual storytelling
- Strong opening hook

### Medium-Paced (Story-Driven)

**Structure:**
- 0-10 seconds: Establish setting and characters
- 10-40 seconds: Build narrative with character development
- 40-80 seconds: Develop conflict or journey
- 80-120 seconds: Resolution and emotional conclusion

**Techniques:**
- Longer takes for emotional moments
- Character interactions and dialogue
- Progressive emotional build
- Satisfying narrative arc

### Slow-Paced (Cinematic)

**Structure:**
- 0-20 seconds: Atmospheric establishment
- 20-60 seconds: Slow character introduction
- 60-120 seconds: Gradual narrative development
- 120-180 seconds: Contemplative resolution

**Techniques:**
- Long, lingering shots
- Emphasis on atmosphere and mood
- Minimal dialogue
- Visual storytelling

## Transition Techniques

### Cut Transitions

**直接切换 (Direct Cut)**
- Instant change between scenes
- Use for: Fast pacing, parallel action, time jumps
- Example: "驾驶舱特写 → 直接切换 → 客舱中景"

### Motion Transitions

**动作匹配 (Match Cut)**
- Similar motion continues across cut
- Use for: Smooth flow, visual poetry, time passage
- Example: "女儿张开双臂（飞机状）→ 切换 → 飞机起飞"

**视线引导 (Eye-line Match)**
- Character looks off-screen → cut to what they see
- Use for: POV shots, revealing information, spatial continuity
- Example: "女儿看向窗外 → 切换 → 窗外地面越来越近"

### Temporal Transitions

**淡入淡出 (Fade In/Out)**
- Gradual transition through black
- Use for: Time passage, chapter breaks, emotional pauses
- Example: "三人走向夕阳，画面淡出"

**叠化 (Dissolve)**
- One image gradually replaces another
- Use for: Montages, memory sequences, gentle time passage
- Example: "机场场景叠化到客舱场景"

## Platform-Specific Tips

### TikTok/Douyin (抖音)

**Format:**
- Vertical (9:16)
- 15-60 seconds optimal
- Hook in first 3 seconds critical

**Content Strategy:**
- Start with visual hook or question
- Fast-paced editing
- Trending audio consideration
- Clear text overlays for key moments
- End with call-to-action or cliffhanger

**Hashtag Strategy:**
- Mix trending and niche hashtags
- Include platform-specific tags (#抖音, #TikTok)
- Genre tags (#搞笑, #家庭, #温馨)

### YouTube Shorts

**Format:**
- Vertical (9:16)
- Up to 60 seconds
- Slightly longer setup acceptable

**Content Strategy:**
- Clear narrative arc
- Strong thumbnail moment
- Descriptive title
- Encourage subscriptions at end
- Series potential for recurring characters

### Instagram Reels

**Format:**
- Vertical (9:16)
- 15-90 seconds
- Visual aesthetics important

**Content Strategy:**
- High production value
- Aesthetic consistency
- Trending audio integration
- Story-driven content
- Behind-the-scenes appeal

## Quality Checklist

Before finalizing video script:

**Character Consistency:**
- [ ] All costume details specified with exact colors
- [ ] Character definitions repeated in every segment
- [ ] Accessories and hairstyles consistent
- [ ] Age-appropriate actions and dialogue

**Narrative Coherence:**
- [ ] Clear three-act structure
- [ ] Logical scene transitions
- [ ] Cause-and-effect relationships
- [ ] Emotional arc progression
- [ ] Satisfying resolution

**Technical Specifications:**
- [ ] Correct segment count (total duration ÷ segment duration)
- [ ] Time breakdowns for each segment
- [ ] Camera angles specified
- [ ] Lighting and atmosphere described
- [ ] Platform format considered

**Prompt Quality:**
- [ ] Specific, concrete descriptions
- [ ] Emotional keywords included
- [ ] Action verbs used
- [ ] Scene atmosphere detailed
- [ ] No vague or generic terms

**Production Readiness:**
- [ ] All segments have character definitions
- [ ] Comedic/dramatic beats identified
- [ ] Transition points clear
- [ ] Platform-specific optimizations applied
- [ ] Post-production notes included
