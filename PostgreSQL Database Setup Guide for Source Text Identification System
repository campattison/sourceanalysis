PostgreSQL Database Setup Guide for Source Text Identification System

# Database Setup Guide
## For the Source Text Identification System in Medieval Philosophy

### Non-Technical Overview
This guide explains how to set up the database that will store and organize all our philosophical texts and their relationships. Think of it as creating a highly organized digital library with special features that allow us to track connections between texts.

### Prerequisites
- PostgreSQL 13 or higher
- Admin access to your computer
- Terminal/Command Prompt access
- At least 100GB free disk space

### Step-by-Step Installation

#### 1. Install PostgreSQL
##### For Windows:
1. Download PostgreSQL installer from: https://www.postgresql.org/download/windows/
2. Run the installer
3. Choose default options when prompted
4. Remember the password you set for the postgres user

##### For Mac:
```bash
brew install postgresql@13
brew services start postgresql@13
```

##### For Linux (Ubuntu/Debian):
```bash
sudo apt update
sudo apt install postgresql-13 postgresql-contrib
```

#### 2. Install Vector Extensions
This allows our database to handle the special numerical representations of texts that AI systems use.

```bash
# For Ubuntu/Debian
sudo apt install postgresql-13-pgvector

# For Mac
brew install pgvector

# For Windows
# Run the included Stack Builder application and select pgvector
```

#### 3. Create the Database

```sql
-- Connect to PostgreSQL
psql -U postgres

-- Create database
CREATE DATABASE philosophical_corpus;

-- Connect to new database
\c philosophical_corpus

-- Enable vector extension
CREATE EXTENSION vector;
```

#### 4. Create Tables
Copy and paste this into your PostgreSQL terminal:

```sql
-- Main texts table
CREATE TABLE philosophical_texts (
    id SERIAL PRIMARY KEY,
    title TEXT NOT NULL,
    author TEXT,
    date_period TEXT,
    language TEXT CHECK (language IN ('Greek', 'Arabic')),
    text_content TEXT NOT NULL,
    word_count INTEGER,
    embedding vector(1536),
    metadata JSONB,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Relationships between texts
CREATE TABLE text_relationships (
    id SERIAL PRIMARY KEY,
    source_text_id INTEGER REFERENCES philosophical_texts(id),
    target_text_id INTEGER REFERENCES philosophical_texts(id),
    relationship_type TEXT,
    confidence_score FLOAT CHECK (confidence_score >= 0 AND confidence_score <= 1),
    evidence TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Analysis results
CREATE TABLE analysis_results (
    id SERIAL PRIMARY KEY,
    text_id INTEGER REFERENCES philosophical_texts(id),
    analysis_type TEXT,
    results JSONB,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Create indexes for better performance
CREATE INDEX idx_text_language ON philosophical_texts(language);
CREATE INDEX idx_text_author ON philosophical_texts(author);
CREATE INDEX idx_text_date ON philosophical_texts(date_period);
CREATE INDEX embedding_idx ON philosophical_texts USING ivfflat (embedding vector_cosine_ops);
```

#### 5. Create User and Set Permissions

```sql
-- Create application user
CREATE USER philosophy_app WITH PASSWORD 'your_secure_password';

-- Grant necessary permissions
GRANT CONNECT ON DATABASE philosophical_corpus TO philosophy_app;
GRANT USAGE ON SCHEMA public TO philosophy_app;
GRANT SELECT, INSERT, UPDATE ON ALL TABLES IN SCHEMA public TO philosophy_app;
GRANT USAGE ON ALL SEQUENCES IN SCHEMA public TO philosophy_app;
```

### Verification Steps
Run these commands to verify your setup:

```sql
-- Connect to database
\c philosophical_corpus

-- List tables
\dt

-- Check vector extension
SELECT * FROM pg_extension WHERE extname = 'vector';
```

### Common Issues and Solutions

#### Permission Denied
If you see "permission denied" errors:
```sql
-- Run as postgres user
ALTER USER philosophy_app WITH SUPERUSER;
```

#### Can't Connect to Server
1. Check if PostgreSQL is running:
```bash
# On Linux/Mac
sudo service postgresql status

# On Windows
services.msc  # Look for PostgreSQL service
```

2. Verify port availability:
```bash
sudo netstat -plnt | grep 5432
```

### Database Structure Explanation

For Classical Scholars:
- The database organizes texts like a library catalog but with special features
- Each text has:
  - Basic information (title, author, date)
  - Full content
  - Special numerical representation for AI analysis
  - Connections to other texts
- We can track:
  - Direct translations
  - Similar arguments
  - Related concepts
  - Citation patterns

### Next Steps
After setting up the database:
1. Test the connection using our Python script
2. Begin importing texts
3. Start running analyses

### Support
If you encounter issues:
1. Check the PostgreSQL logs:
```bash
# Linux/Mac
tail -f /var/log/postgresql/postgresql-13-main.log

# Windows
Check Event Viewer > Applications and Services > PostgreSQL
```

2. Contact the technical team with:
   - Error messages
   - Steps to reproduce
   - Your operating system
   - PostgreSQL version
