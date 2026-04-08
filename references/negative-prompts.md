# 负面提示词库 (Negative Prompts)

> 7 类负面提示词 | 漫剧创作大师核心知识库

---

## 📖 使用说明

负面提示词用于告诉 AI **不要生成什么**，是提升生成质量的关键工具。

**使用原则：**
1. 针对性：根据场景选择对应的负面词
2. 精简性：不要堆砌过多，10-20 个关键词即可
3. 权重性：重要问题可加权重 `(keyword:1.5)`

---

## 1️⃣ 人物崩坏类

**问题表现：** 五官变形、肢体异常、手指数量错误

**负面提示词：**
```
ugly, deformed, bad anatomy, disfigured, poorly drawn hands, 
poorly drawn feet, poorly drawn face, out of frame, extra limbs, 
missing limbs, floating limbs, disconnected limbs, malformed hands, 
mutation, mutated, extra fingers, missing fingers, too many fingers, 
long neck, double head, multiple heads, cloned face, distorted face, 
asymmetric eyes, crossed eyes, lazy eye, bad proportions, 
grotesque, horror, zombie
```

**针对性强化：**
- 手指问题：`(extra fingers:1.5), (bad hands:1.4), (missing fingers:1.3)`
- 面部问题：`(deformed face:1.5), (distorted features:1.4)`
- 肢体问题：`(extra limbs:1.5), (bad anatomy:1.4)`

---

## 2️⃣ 画质问题类

**问题表现：** 模糊、噪点、低分辨率、锯齿

**负面提示词：**
```
blurry, low quality, low resolution, pixelated, noisy, 
grainy, jpeg artifacts, compression artifacts, overexposed, 
underexposed, bad lighting, dark, dim, washed out, 
oversaturated, undersaturated, dull colors, muddy colors, 
aliasing, moire pattern, banding, posterization, 
watermark, signature, text, logo, username, date stamp
```

**针对性强化：**
- 模糊问题：`(blurry:1.5), (out of focus:1.4), (unsharp:1.3)`
- 噪点问题：`(noisy:1.5), (grainy:1.4), (low quality:1.3)`
- 水印问题：`(watermark:1.5), (text:1.4), (signature:1.3)`

---

## 3️⃣ 风格跳变类

**问题表现：** 风格不统一、元素混搭、画风突变

**负面提示词：**
```
style inconsistency, mixed styles, inconsistent art style, 
amateur, beginner, unskilled, rough, sketchy, unfinished, 
incomplete, rough draft, doodle, scribble, messy, 
unprofessional, low effort, hasty, careless, 
cartoon in realistic, realistic in cartoon, 
anime in photorealistic, photorealistic in anime
```

**针对性强化：**
- 风格统一：`(style inconsistency:1.5), (mixed styles:1.4)`
- 专业度：`(amateur:1.4), (beginner:1.3), (unprofessional:1.3)`

---

## 4️⃣ 场景错误类

**问题表现：** 逻辑错误、物体穿模、环境不合理

**负面提示词：**
```
impossible geometry, non-euclidean, escher-like, 
physically impossible, gravity defying, floating objects, 
clipping, intersecting objects, overlapping incorrectly, 
wrong perspective, distorted perspective, fish eye, 
barrel distortion, pincushion distortion, 
inconsistent lighting, multiple suns, wrong shadows, 
indoor outdoor mix, day night mix, season mix
```

**针对性强化：**
- 透视问题：`(wrong perspective:1.5), (distorted:1.4)`
- 穿模问题：`(clipping:1.5), (intersecting:1.4)`
- 光影问题：`(inconsistent lighting:1.5), (wrong shadows:1.4)`

---

## 5️⃣ 内容违规类

**问题表现：** 低俗、暴力、血腥、敏感内容

**负面提示词：**
```
nsfw, nude, naked, explicit, sexual, erotic, 
violent, gore, blood, bloody, horror, scary, 
disturbing, offensive, inappropriate, 
political, religious controversy, 
hate speech, discrimination, racism, sexism
```

**注意：** 此类负面词为安全红线，必须添加

---

## 6️⃣ 角色一致性问题类

**问题表现：** 角色外貌变化、服装变化、特征丢失

**负面提示词：**
```
inconsistent character, character change, 
different face, different hair, different clothes, 
different body, different age, different gender, 
costume change, outfit change, 
hair color change, eye color change, 
accessory missing, prop missing
```

**针对性强化：**
- 外貌一致：`(inconsistent character:1.5), (different face:1.4)`
- 服装一致：`(costume change:1.5), (outfit change:1.4)`

---

## 7️⃣ 视频特有问题类

**问题表现：** 闪烁、抖动、画面跳动、动作不连贯

**负面提示词：**
```
flickering, jittering, shaking, unstable, 
jumping, skipping, stuttering, lagging, 
inconsistent motion, jerky movement, 
unnatural movement, robotic movement, 
morphing, shape shifting, 
frame inconsistency, temporal artifacts
```

**针对性强化：**
- 闪烁问题：`(flickering:1.5), (frame inconsistency:1.4)`
- 动作问题：`(unnatural movement:1.5), (jerky:1.4)`

---

## 📋 场景化负面词组合

### 人像摄影
```
ugly, deformed, bad anatomy, disfigured, poorly drawn face, 
extra limbs, blurry, low quality, watermark, text, 
plastic skin, doll-like, artificial, over-retouched
```

### 产品摄影
```
blurry, low quality, noisy, watermark, text, logo, 
overexposed, underexposed, plastic look, cheap appearance, 
damaged, scratched, dirty, dusty
```

### 风景摄影
```
blurry, low quality, noisy, overexposed, underexposed, 
flat lighting, boring composition, hazy, 
watermark, text, signature
```

### 动漫角色
```
realistic, photorealistic, 3d render, cgi, 
ugly, deformed, bad anatomy, extra limbs, 
western style, american comic
```

### 科幻场景
```
medieval, historical, natural, pastoral, 
realistic photo, mundane, everyday, 
low quality, amateur
```

### 视频生成
```
flickering, jittering, frame inconsistency, 
morphing, shape shifting, 
unnatural movement, jerky, 
inconsistent character, style change
```

---

## 🔧 权重调整建议

| 问题严重程度 | 权重建议 |
|-------------|---------|
| 轻微问题 | `keyword:1.2` |
| 中等问题 | `keyword:1.3` |
| 严重问题 | `keyword:1.5` |
| 极严重问题 | `keyword:1.7` |

**示例：**
```
# 手指问题严重
(extra fingers:1.7), (bad hands:1.5), (deformed:1.3)

# 画面闪烁严重
(flickering:1.7), (frame inconsistency:1.5), (unstable:1.3)
```
