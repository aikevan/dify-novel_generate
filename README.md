```markdown
# 这是一个简单的小说生成工作流
平台 - Dify
请使用novel.yml

下载yml文件，导入Dify
<img width="378" alt="image" src="https://github.com/user-attachments/assets/b755366f-d493-48bb-9490-0c252f30ccc8" />

## 介绍
- **basic_info**: 小说基础信息，包括名称，大纲，类型
- **current_chapter_overview**: 当前章节概述
- **precondition_chapter_list**: 前置章节列表
- **character_relation_file**: 小说人物关系，可以是TXT, MD格式，
- **knowledge_query**: 你需要的知识

## 流程节点介绍
- **文档内容提取**: 提取上传的人物关系和前置章节内容
- **知识检索**: 检索指定的知识库
- **提示词转换（LLM节点）**: 将人物关系和前置章节内容转换成大语言模型更好理解的提示词
- **生成章节内容（LLM节点）**: 接收人物关系和前置章节内容及设置的小说参数，生成一章不小于2000-2500字的小说内容，字数不强求，但要符合逻辑和剧情发展
- **内容检查（LLM节点-深度思考模型）**: 这个节点和生成章节内容接受的参数是一致的，当然这个节点也收上个节点生成的小说内容，不过我们的要求是要对生成内容进行检查和优化
```
