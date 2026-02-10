# AI Video Script Generator

A Claude Code skill for generating segmented video prompts for AI video generation tools with guaranteed character consistency, costume uniformity, and narrative coherence.

## Overview

This skill transforms user stories into production-ready, time-segmented prompts optimized for AI video generation tools like Runway, Pika, 即梦 (Jimeng), and other text-to-video platforms.

## Features

- ✅ **Character Consistency**: Detailed costume specifications repeated in every segment
- ✅ **Narrative Coherence**: Structured three-act storytelling with logical transitions
- ✅ **Time-Based Segmentation**: Precise breakdowns (e.g., 3-second intervals within 12-second segments)
- ✅ **Platform Optimization**: Tailored for TikTok, YouTube Shorts, Instagram Reels
- ✅ **Bilingual Support**: Works with both English and Chinese prompts
- ✅ **Production-Ready**: Complete design documents with implementation notes

## When to Use

Use this skill when you need to:
- Generate segmented video prompts for AI video generation
- Create character-consistent video scripts across multiple segments
- Design detailed costume and appearance specifications
- Structure narratives with logical scene transitions
- Produce social media video scripts (TikTok, Instagram, YouTube Shorts)

## Installation

### For Claude Code

1. Copy the `ai-video-script-generator` directory to your Claude Code skills directory:
   ```bash
   cp -r ai-video-script-generator ~/.claude/skills/
   ```

2. Restart Claude Code or reload skills

3. The skill will automatically activate when you ask to "生成视频脚本", "创建视频提示词", or similar phrases

### For Claude Code Plugins

1. Add to your plugin's `skills/` directory:
   ```bash
   cp -r ai-video-script-generator your-plugin/skills/
   ```

2. The skill will be auto-discovered when the plugin is loaded

## Usage

### Basic Usage

Simply ask Claude to generate a video script:

```
"帮我生成一个2分钟的家庭短片脚本，12秒一段"
```

```
"Create a 60-second TikTok video script with 3 characters"
```

### Detailed Usage

Provide specific requirements:

```
"我需要一个《冲上云霄》风格的短片脚本：
- 人物：飞行员父亲、乘务长母亲、3岁女儿
- 风格：幽默搞笑
- 时长：2分钟，12秒一段
- 平台：抖音"
```

### What You'll Get

The skill will guide you through:

1. **Requirements Gathering**: Characters, story, technical specs
2. **Character Definition**: Detailed costume specifications
3. **Narrative Structure**: Three-act breakdown with segment allocation
4. **Segmented Prompts**: Time-based action breakdowns for each segment
5. **Design Document**: Complete production-ready documentation

## Example Output

See `examples/family-aviation-story.md` for a complete 2-minute, 10-segment video script with:
- Detailed character costume specifications
- Scene-by-scene breakdowns
- 3-second interval action descriptions
- Camera angles and movements
- Emotional beats and comedic timing
- Production notes and platform recommendations

## Skill Structure

```
ai-video-script-generator/
├── SKILL.md                          # Core skill instructions
├── README.md                         # This file
├── references/
│   ├── best-practices.md            # AI video generation best practices
│   └── prompt-patterns.md           # Effective prompt patterns and techniques
└── examples/
    └── family-aviation-story.md     # Complete working example
```

## Key Principles

### 1. Character Consistency Through Detailed Specification

**Problem**: AI video tools often generate inconsistent character appearances across segments.

**Solution**: Define exact costume specifications once and repeat in every segment:

```
男主角：深蓝色飞行员制服外套，白色长袖衬衫，深蓝色领带，金色肩章（四道杠），深蓝色制服裤，黑色皮鞋
```

### 2. Time-Based Action Breakdowns

Structure each segment with precise timing:

```
**0-3秒：**
- 场景：明亮的现代机场航站楼大厅
- 镜头：中景
- 动作：男主角和女主角并肩走来

**3-6秒：**
- 镜头：特写切换
- 动作：女儿从后面跑过来
```

### 3. Three-Act Narrative Structure

- **Setup** (30%): Introduce characters, establish setting
- **Development** (40%): Main action, conflicts, interactions
- **Resolution** (30%): Climax, conclusion, emotional payoff

### 4. Platform-Specific Optimization

- **TikTok/Douyin**: Fast-paced, hook in first 3 seconds, vertical format
- **YouTube Shorts**: Slightly longer setup, clear narrative arc
- **Instagram Reels**: Visual aesthetics, trending audio consideration

## Supported Platforms

### AI Video Generation Tools

- **即梦 (Jimeng)**: Optimized for Chinese prompts with digital human feature
- **Runway Gen-3**: Cinematic quality, excellent motion
- **Pika 2.0**: Fast iteration, image-to-video support
- **Other text-to-video tools**: General prompt structure works across platforms

### Social Media Platforms

- **TikTok/Douyin (抖音)**: Vertical 9:16, 15-60 seconds
- **YouTube Shorts**: Vertical 9:16, up to 60 seconds
- **Instagram Reels**: Vertical 9:16, 15-90 seconds

## Best Practices

### ✅ DO

- Use specific, concrete descriptions ("深蓝色飞行员制服" not "制服")
- Specify camera angles clearly (全景/中景/近景/特写)
- Include emotional keywords (温馨/搞笑/紧张/兴奋)
- Describe lighting and atmosphere (明亮的/柔和的/金色阳光)
- Use action verbs (走来/跑过来/转身/蹲下来)
- Repeat character definitions in every segment
- Break segments into 3-second intervals

### ❌ DON'T

- Use vague costume descriptions
- Have inconsistent character definitions across segments
- Skip time breakdowns
- Use generic scene descriptions
- Forget to specify camera angles
- Neglect emotional beats

## Advanced Features

### Character Consistency Techniques

1. **Detailed Specification** (Most Reliable): Repeat exact descriptions
2. **Reference Images**: Use consistent reference images
3. **Character IDs**: Platform-specific character ID systems

### Camera Angles and Movements

- **Static**: 全景, 中景, 近景, 特写, 远景
- **Dynamic**: 推进, 拉远, 跟随, 环绕, 摇镜

### Emotional Keywords

- **Positive**: 温馨, 兴奋, 骄傲, 开心
- **Comedic**: 搞笑, 可爱, 哭笑不得, 认真
- **Dramatic**: 紧张, 惊讶, 感动, 专注

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

### Areas for Improvement

- Additional platform-specific optimizations
- More example scripts in different genres
- Support for longer-form content (5+ minutes)
- Integration with specific AI video tools' APIs

## License

MIT License - feel free to use and modify for your projects.

## Credits

Created by Claude Code based on real-world video script generation workflows.

## Support

For questions or issues:
- Open an issue on GitHub
- Check the `references/` directory for detailed guidance
- Review `examples/` for working examples

## Version History

### v0.1.0 (2026-02-10)
- Initial release
- Core workflow implementation
- Character consistency system
- Time-based segmentation
- Platform optimization
- Complete example (family aviation story)
- Comprehensive references (best practices, prompt patterns)

---

**Happy video scripting! 🎬**
