# API 配置参考

## api.heang.top 配置

### Seedance 2.0 视频生成

**API 端点：**
```
POST https://api.heang.top/v1/videos/generations
```

**模型列表：**
- Pro版：`doubao-seedance-2-0-260128` (高质量)
- Fast版：`doubao-seedance-2-0-fast-260128` (快速)
- 1.5 Pro版：`doubao-seedance-1-5-pro-251215`
- 1.0 Pro版：`doubao-seedance-1-0-pro-250528`
- Lite版：`doubao-seedance-1-0-lite-t2v` / `doubao-seedance-1-0-lite-i2v`

**完整参数：**

| 参数 | 简写 | 说明 | 默认值 |
|------|------|------|--------|
| `--mode` | | 模式: fast / pro | pro |
| `--model` | `-m` | 指定模型 ID | 自动选择 |
| `--ratio` | `-r` | 视频比例 | 16:9 |
| `--duration` | `-d` | 时长 (5-30s) | 10 |
| `--resolution` | `--res` | 分辨率 | 720p |
| `--audio` | | 生成音频 (true/false) | true |
| `--no-audio` | | 不生成音频 | - |
| `--image` | `-i` | 参考图片 URL (可多个) | - |
| `--video` | `-v` | 参考视频 URL (可多个) | - |
| `--audio-file` | | 参考音频 URL (可多个) | - |
| `--first-frame` | | 首帧图片 URL | - |
| `--last-frame` | | 尾帧图片 URL | - |
| `--seed` | | 随机种子 | 随机 |
| `--frames` | | 帧数 | 自动 |
| `--camera-fixed` | | 固定镜头 | false |
| `--watermark` | | 添加水印 | false |
| `--service-tier` | | 服务等级: default / flex | default |
| `--timeout` | | 任务超时 (秒) | 172800 |
| `--callback-url` | | 回调 URL | - |
| `--return-last-frame` | | 返回尾帧图片 | false |
| `--draft` | | 样片模式 | false |
| `--web-search` | | 启用联网搜索 | false |
| `--safety-id` | | 终端用户标识 | - |

### Nano Banana Pro 图像生成

**API 端点：**
```
POST https://api.heang.top/v1/images/generations
```

**模型列表：**
- Pro版：`doubao-nanobanana-pro-260103`
- 标准版：`doubao-nanobanana-260103`

**参数说明：**

| 参数 | 可选值 | 默认值 | 说明 |
|------|--------|--------|------|
| `aspect_ratio` | 1:1 / 2:3 / 3:2 / 3:4 / 4:3 / 4:5 / 5:4 / 9:16 / 16:9 / 21:9 / adaptive | adaptive | 画幅比例 |
| `resolution` | 480p / 720p / 1080p / 2K / 4K | 1080p | 分辨率 |
| `output_format` | png / jpg | png | 输出格式 |
| `image_input` | URL 数组（最多 8 张） | [] | 参考图片 |

### 配置文件示例

**config.json:**
```json
{
  "baseUrl": "https://api.heang.top",
  "apiKey": "YOUR_API_KEY_HERE",
  "defaultMode": "pro",
  "defaultRatio": "16:9",
  "defaultDuration": 10,
  "defaultResolution": "720p",
  "defaultGenerateAudio": true
}
```

### 环境变量配置

```bash
export SEEDANCE_API_KEY="YOUR_API_KEY_HERE"
export SEEDANCE_BASE_URL="https://api.heang.top"
export KIE_API_KEY="YOUR_API_KEY_HERE"
export HEANG_BASE_URL="https://api.heang.top"
```