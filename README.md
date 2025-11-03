# AIpoju

小红书评论采集器 - 最简单的实现

## 功能说明

这是一个最简单的小红书评论采集工具，提供了基础的评论采集框架。

## 安装依赖

```bash
pip install -r requirements.txt
```

## 使用方法

### 基础使用

```python
python xiaohongshu_comments.py
```

### 在代码中使用

```python
from xiaohongshu_comments import XiaohongshuCommentCollector

# 创建采集器
collector = XiaohongshuCommentCollector()

# 采集评论
note_id = "your_note_id_here"
comments = collector.collect_comments(note_id, max_comments=20)

# 保存评论
collector.save_comments(comments, 'output.json')
```

## 重要说明

⚠️ **注意事项：**

1. 这是一个**最简单的框架实现**，用于学习和演示
2. 小红书有严格的反爬虫机制，实际使用需要：
   - 登录认证（Cookie）
   - 请求签名（X-Sign等参数）
   - 设备指纹信息
   - 合理的请求间隔
3. 建议使用官方API或遵守平台使用规则
4. 本工具仅供学习交流使用

## 评论数据结构

```json
{
  "comment_id": "评论ID",
  "user_id": "用户ID",
  "user_name": "用户昵称",
  "content": "评论内容",
  "create_time": "创建时间",
  "like_count": 0,
  "reply_count": 0
}
```

## 文件说明

- `xiaohongshu_comments.py` - 主程序文件
- `requirements.txt` - 依赖包列表
- `README.md` - 使用说明文档

## 许可证

本项目仅供学习使用，请遵守相关法律法规和平台规则。
