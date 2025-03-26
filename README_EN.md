# A Simple Novel Generation Workflow  
**Platform**: Dify  
Use `novel.yml`  

Download the YML file and import it into Dify:  
<img width="378" alt="image" src="https://github.com/user-attachments/assets/b755366f-d493-48bb-9490-0c252f30ccc8" />  

## Introduction  
- **basic_info**: Basic novel information, including title, outline, and genre.  
- **current_chapter_overview**: Overview of the current chapter.  
- **precondition_chapter_list**: List of prerequisite chapters.  
- **character_relation_file**: Character relationship file (TXT or MD format).  
- **knowledge_query**: Required knowledge for generation.  

## Workflow Node Descriptions  
- **Document Content Extraction**: Extracts uploaded character relationships and prerequisite chapter content.  
- **Knowledge Retrieval**: Queries specified knowledge bases.  
- **Prompt Transformation (LLM Node)**: Converts character relationships and chapter content into prompts optimized for large language models.  
- **Generate Chapter Content (LLM Node)**: Generates a chapter (minimum 2000-2500 words) based on character relationships, prerequisite content, and novel parameters. Word count is flexible but must align with logical plot progression.  
- **Content Review (LLM Node - Deep Thinking Model)**: Reviews and optimizes generated content. This node uses the same input parameters as the generation node, plus the newly created chapter content.  
