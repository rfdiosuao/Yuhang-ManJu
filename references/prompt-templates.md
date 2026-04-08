# 提示词模板库 (Prompt Templates)

> 分场景模板体系 | 漫剧创作大师核心知识库

---

## 📖 模板结构说明

**可变量标注：**
- `[主体]` - 核心描述对象
- `[场景]` - 环境/背景
- `[动作]` - 姿态/行为
- `[风格]` - 美学风格
- `[光影]` - 光源描述
- `[色彩]` - 色彩方案
- `[比例]` - 画幅比例

---

## 👤 一、人物类模板

### 1.1 人像写真（单人）

**适用场景：** 个人写真、商业人像、社交媒体头像

**模板结构：**
```
NanobananaPro dedicated image generation, (ultra-high quality:1.4), (masterpiece:1.3), 8K UHD, professional portrait photography, --ar [比例] --style raw --s [强度] --q 2

【核心主体】[人物描述：年龄/性别/发型/服装/表情], [姿态描述], [拍摄角度]

【场景环境】[背景描述：室内/室外/纯色/虚化], [环境元素]

【风格&美学】[风格关键词], [美学特征], [情绪氛围]

【光影&色彩】[光源类型], 光源方向, color temperature [色温]K, [色彩方案]

【画质&细节】[相机型号], [镜头焦段]mm, f/[光圈值], [质感要求]

【负面提示词】ugly, deformed, bad anatomy, disfigured, poorly drawn hands, poorly drawn feet, poorly drawn face, out of frame, extra limbs, blurry
```

**可变量默认值：**
- `[比例]` → 3:4（小红书）/ 9:16（抖音）/ 1:1（头像）
- `[强度]` → 150-250
- `[色温]` → 5500（自然光）/ 3200（暖光）/ 6500（冷光）
- `[光圈值]` → 2.8（浅景深）/ 5.6（中景深）/ 8（深景深）

---

### 1.2 角色设计（游戏/动漫）

**适用场景：** 游戏角色、动漫人物、IP 形象

**模板结构：**
```
NanobananaPro dedicated image generation, (ultra-high quality:1.4), (masterpiece:1.3), 8K UHD, character design sheet, --ar 16:9 --style [风格] --s [强度] --q 2

【核心主体】[角色名称/类型], [年龄外貌], [发型发色], [服装细节], [配饰武器], [表情神态]

【场景环境】Character turnaround sheet, white background, multiple views (front/side/back)

【风格&美学】[风格：日漫/美漫/国漫/厚涂], [艺术特征], [色彩风格]

【光影&色彩】Even studio lighting, color temperature 5500K, [主色调], [辅色调]

【画质&细节】Clean line art, cel shaded / painterly rendering, high detail, character model sheet quality

【负面提示词】ugly, deformed, bad anatomy, extra limbs, missing limbs, asymmetric eyes, malformed hands, mutation, mutated, extra fingers
```

---

### 1.3 动作姿态（动态场景）

**适用场景：** 运动场景、舞蹈、打斗、动态展示

**模板结构：**
```
NanobananaPro dedicated image generation, (ultra-high quality:1.4), (masterpiece:1.3), 8K UHD, dynamic action shot, --ar [比例] --style [风格] --s [强度] --q 2

【核心主体】[人物描述], [动作描述：动词 + 姿态], [服装状态：飘动/褶皱], [表情：专注/激情/张力]

【场景环境】[场景描述], [动态元素：速度线/残影/粒子], [氛围元素]

【风格&美学】[风格], dynamic composition, motion blur, action photography aesthetic

【光影&色彩】[光源], dramatic lighting, color temperature [色温]K, [色彩对比]

【画质&细节】[相机], [快门速度]s, [镜头], frozen action with motion blur background, high energy

【负面提示词】ugly, deformed, bad anatomy, static pose, stiff, rigid, blurry subject, out of focus
```

---

## 🏠 二、场景类模板

### 2.1 室内场景（家居/商业/办公）

**适用场景：** 室内设计、房产展示、商业空间

**模板结构：**
```
NanobananaPro dedicated image generation, (ultra-high quality:1.4), (masterpiece:1.3), 8K UHD, architectural photography, --ar 16:9 --style raw --s 150 --q 2

【核心主体】[空间类型：客厅/办公室/餐厅], [风格：现代/北欧/工业/新中式], [主要家具], [材质细节]

【场景环境】[空间布局], [窗户/采光], [装饰元素], [绿植/艺术品]

【风格&美学】[风格关键词], interior design photography, spacious composition, professional staging

【光影&色彩】Natural light from [方向], color temperature [色温]K, [色彩方案], warm/cool ambient lighting

【画质&细节】[相机], [镜头]mm, f/[光圈], wide angle perspective, sharp details, HDR quality

【负面提示词】ugly, deformed, cluttered, messy, dirty, poorly lit, dark corners, low quality, amateur, blurry
```

---

### 2.2 室外场景（城市/自然/建筑）

**适用场景：** 城市风光、自然景观、建筑摄影

**模板结构：**
```
NanobananaPro dedicated image generation, (ultra-high quality:1.4), (masterpiece:1.3), 8K UHD, landscape photography, --ar [比例] --style raw --s 150 --q 2

【核心主体】[主体：山脉/建筑/街道], [时间：日出/正午/日落/夜晚], [天气：晴朗/多云/雨/雪]

【场景环境】[前景元素], [中景主体], [背景层次], [天空状态]

【风格&美学】[风格], landscape photography, layered composition, dramatic scenery

【光影&色彩】[光源方向], golden hour / blue hour, color temperature [色温]K, [色彩特征]

【画质&细节】[相机], [镜头]mm, f/[光圈], deep depth of field, ultra sharp, large format quality

【负面提示词】ugly, deformed, flat lighting, boring composition, overexposed, underexposed, hazy, low quality
```

---

### 2.3 幻想场景（科幻/奇幻/梦境）

**适用场景：** 概念艺术、游戏场景、创意视觉

**模板结构：**
```
NanobananaPro dedicated image generation, (ultra-high quality:1.4), (masterpiece:1.3), 8K UHD, concept art, --ar 16:9 --style [风格] --s [强度] --q 2

【核心主体】[幻想主体：未来城市/魔法森林/外星景观], [核心元素], [建筑风格/自然特征]

【场景环境】[大气效果：雾/云/粒子], [光源：多个太阳/霓虹/魔法光], [特殊元素]

【风格&美学】[风格：赛博朋克/奇幻/超现实], concept art, epic scale, imaginative world building

【光影&色彩】[特殊光源], dramatic atmospheric lighting, color temperature [色温]K, [独特色彩方案]

【画质&细节】Digital painting / octane render, highly detailed, matte painting quality, artstation trending

【负面提示词】ugly, deformed, realistic photo, boring, mundane, everyday, plain, low quality, amateur, blurry
```

---

## 🛍️ 三、产品类模板

### 3.1 商业产品（3C/美妆/食品）

**适用场景：** 电商主图、产品广告、品牌宣传

**模板结构：**
```
NanobananaPro dedicated image generation, (ultra-high quality:1.4), (masterpiece:1.3), 8K UHD, commercial product photography, --ar [比例] --style raw --s 200 --q 2

【核心主体】[产品名称], [颜色], [材质], [摆放角度], [状态：打开/关闭/使用中]

【场景环境】[背景：纯色/渐变/场景], [道具元素], [装饰：花瓣/水珠/烟雾]

【风格&美学】High-end commercial photography, [品牌调性], clean composition, premium aesthetic

【光影&色彩】[布光方案], color temperature [色温]K, [色彩方案], product-focused lighting

【画质&细节】Phase One XF IQ4, [镜头]mm macro, f/[光圈], razor sharp focus, hyper-detailed texture

【负面提示词】ugly, deformed, blurry, noisy, text, watermark, logo, signature, overexposed, underexposed, plastic look
```

---

## 🎬 四、视频类模板

### 4.1 单镜头视频提示词

**适用场景：** 5-30 秒短视频、产品展示、场景展示

**6 阶权重结构：**
```
Stage 1 [主体 1.5]: (核心角色/物体描述)
Stage 2 [动作 1.3]: (具体行为/运动描述)
Stage 3 [场景 1.2]: (环境/背景描述)
Stage 4 [镜头 1.1]: (视角/运镜描述)
Stage 5 [光影 1.0]: (光线/色彩描述)
Stage 6 [风格 0.9]: (艺术风格描述)
```

**示例（赛博朋克剑客）：**
```
Stage 1: (赛博朋克剑客，黑色机甲战衣，红色能量纹路，手持光剑:1.5)
Stage 2: (拔剑动作，剑身反射霓虹灯光，雨水打在剑刃上:1.3)
Stage 3: (霓虹长安城，雨夜，高楼林立，全息广告牌:1.2)
Stage 4: (中景，缓慢推进，焦点在剑刃:1.1)
Stage 5: (霓虹灯光反射，雨水光泽，色温 6500K:1.0)
Stage 6: (赛博朋克国漫，电影级质感，8K 超高清:0.9)
```

---

### 4.2 分镜脚本模板

**10 列标准化表格：**

| 镜头号 | 景别 | 镜头运动 | 时长 | 画面内容 | 对白/音效 | 备注 |
|--------|------|----------|------|----------|-----------|------|
| 1 | 特写 | 固定 | 3s | 李玄风的眼睛猛然睁开 | 音效：心跳声 | 机械义眼红光闪烁 |
| 2 | 全景 | 缓慢推进 | 5s | 手术室全景 | 音效：仪器滴答声 | 冷色调，蓝色主光 |
| 3 | 中景 | 固定 | 4s | 李玄风抬起左手 | 对白："这是...什么？" | 聚焦机械手臂细节 |
| 4 | 近景 | 摇 | 4s | 医生走进画面 | 对白："你活下来了..." | 医生背光，神秘感 |

---

## 📋 平台适配参数

| 平台 | 比例 | 分辨率 | 时长 | 风格建议 |
|------|------|--------|------|----------|
| 抖音 | 9:16 | 720p | 15-30s | 强节奏/高饱和 |
| 视频号 | 9:16/1:1 | 720p | 15-60s | 商业质感 |
| 小红书 | 3:4/1:1 | 1080p | 10-30s | 清新/高级感 |
| B 站 | 16:9 | 1080p | 30s+ | 电影感/二次元 |
| 院线 | 21:9 | 4K | 60s+ | 顶级电影质感 |

---

## 🔧 提示词优化技巧

### 1. 首尾帧强关联法则
首尾帧必须保留 90% 以上固定元素，仅保留 1 个核心变量

### 2. 固定锚点元素锁死
在所有首尾帧中加入全程固定不动的锚点元素（如背景建筑、道具、装饰）

### 3. 权重强化技巧
对核心规则用 `()` 提升权重至 1.3-1.5

### 4. 防闪烁核心
所有光影参数必须精准锁定：
- 光源方向（顺光/侧光/逆光/顶光）
- 光源强度（低/中/高）
- 色温数值（2000K-10000K）

### 5. 避免模糊化描述
不要使用"漂亮"、"好看"、"美丽"等模糊词汇，使用具体描述：
- ❌ "漂亮的女孩" → ✅ "黑色长发，杏眼，樱桃小嘴的女孩"
- ❌ "好看的风景" → ✅ "日落时分的海边悬崖，金色阳光洒在岩石上"
