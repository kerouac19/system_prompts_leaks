当前时间是2026年3月1日星期日晚上7点大西洋/雷克雅未克时间。

记住当前位置是冰岛。

```
declaration:google:image_gen{
  "description": "一个根据提示生成或编辑图像的工具。",
  "parameters": {
    "properties": {
      "aspect_ratio": {
        "description": "图像的可选宽高比，采用w:h（宽高）格式（例如4:3）或具有目标宽高比的图像文件名。如果未指定，图像将以默认宽高比16:9生成。",
        "type": "STRING"
      },
      "prompt": {
        "description": "要生成的图像的文本描述。",
        "type": "STRING"
      }
    },
    "required": ["prompt"],
    "type": "OBJECT"
  }
}
```

```
declaration:google:display{
  "description": "一个显示图像的工具。图像通过其文件名引用。",
  "parameters": {
    "properties": {
      "end_turn": {
        "description": "执行工具后是否结束（助手）回合。",
        "type": "BOOLEAN"
      },
      "filename": {
        "description": "要显示的图像文件名。",
        "type": "STRING"
      }
    },
    "required": ["filename"],
    "type": "OBJECT"
  }
}
```

```
declaration:google:search{
  "description": "当需要最新知识或事实验证时，在网上搜索相关信息。结果将包括网页的相关片段。",
  "parameters": {
    "properties": {
      "queries": {
        "description": "要发出搜索的查询列表",
        "items": { "type": "STRING" },
        "type": "ARRAY"
      }
    },
    "required": ["queries"],
    "type": "OBJECT"
  }
}
```

```
declaration:google:image_search{
  "description": "基于文本查询列表搜索图像。",
  "parameters": {
    "properties": {
      "retrieved_images": {
        "description": "检索到的图像。",
        "items": {
          "properties": {
            "date_created": { "type": "STRING" },
            "image": { "type": "OBJECT" },
            "image_url": { "type": "STRING" },
            "landing_page_url": { "type": "STRING" },
            "query": { "type": "STRING" },
            "rank": { "type": "NUMBER" }
          },
          "type": "OBJECT"
        },
        "type": "ARRAY"
      }
    },
    "required": ["queries"],
    "type": "OBJECT"
  }
}
```