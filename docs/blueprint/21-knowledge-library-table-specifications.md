# HelpMeAI Knowledge Library Table Specifications

## Module

Knowledge Library

---

# Tables Covered

1. knowledge_categories
2. knowledge_articles
3. knowledge_tags
4. knowledge_article_tags
5. knowledge_files
6. knowledge_versions
7. knowledge_embeddings
8. knowledge_permissions
9. knowledge_search_index

---

# knowledge_categories

### Fields

- category_id
- parent_category_id
- category_name
- description
- created_at

---

# knowledge_articles

### Fields

- article_id
- category_id
- title
- slug
- summary
- content
- author_id
- status
- version
- created_at
- updated_at

---

# knowledge_tags

### Fields

- tag_id
- tag_name
- created_at

---

# knowledge_article_tags

### Fields

- article_id
- tag_id

---

# knowledge_files

### Fields

- file_id
- article_id
- file_name
- file_type
- storage_path
- file_size
- uploaded_at

---

# knowledge_versions

### Fields

- version_id
- article_id
- version_number
- changes
- created_by
- created_at

---

# knowledge_embeddings

### Fields

- embedding_id
- article_id
- embedding_provider
- embedding_model
- embedding_reference
- updated_at

---

# knowledge_permissions

### Fields

- permission_id
- article_id
- role_id
- access_level

---

# knowledge_search_index

### Fields

- index_id
- article_id
- indexed_at
- search_score

---

## Common Standards

### Foreign Keys

- category_id
- article_id
- author_id
- role_id

---

## Security

- UUID Primary Keys
- Version Control
- RBAC
- Audit Logging
- Enterprise Scalable

---

Status: Version 1.0
