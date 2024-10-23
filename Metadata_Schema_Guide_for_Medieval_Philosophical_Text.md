# Metadata Schema Guide
## For Greek and Arabic Philosophical Texts in the Source Text Identification System

### Non-Technical Overview
This guide explains how to organize information about each philosophical text in a consistent way. Think of it as creating a detailed catalog card for each text, but in a format that computers can easily process. Having well-structured metadata is crucial for finding connections between texts and tracking the transmission of ideas.

### Basic Metadata Structure
```json
{
    "text_id": "unique_identifier",
    "bibliographic_info": {
        "title": {
            "original": "Original language title",
            "transliterated": "Transliterated title",
            "english": "English title"
        },
        "author": {
            "name": {
                "standard": "Standard name form",
                "variants": ["Alternative spellings", "Other names"]
            },
            "dates": {
                "birth": "Year or century",
                "death": "Year or century",
                "flourished": "Active period"
            }
        },
        "language": {
            "primary": "Greek or Arabic",
            "dialects": ["Specific dialect if applicable"],
            "script": "Script type used"
        }
    },
    "composition_details": {
        "date": {
            "year": "Specific year if known",
            "century": "Century",
            "period": "Historical period",
            "certainty": "confirmed/estimated/unknown"
        },
        "place": {
            "city": "City of composition",
            "region": "Historical region",
            "modern_country": "Modern country"
        }
    },
    "transmission_history": {
        "manuscript_tradition": {
            "earliest_manuscript": "Date",
            "key_manuscripts": ["List of important manuscripts"],
            "transmission_route": ["Geographic path of transmission"]
        },
        "translation_details": {
            "translator": "Name if known",
            "translation_date": "Date",
            "translation_place": "Location",
            "source_text": "Original text identifier if this is a translation"
        }
    },
    "content_classification": {
        "genres": ["Philosophy", "Commentary", "Letter", etc.],
        "subjects": ["Logic", "Metaphysics", "Ethics", etc.],
        "schools": ["Peripatetic", "Neoplatonic", etc.],
        "key_concepts": ["List of major philosophical concepts"],
        "related_texts": ["IDs of related texts"]
    },
    "editorial_info": {
        "modern_editions": [{
            "editor": "Editor name",
            "year": "Publication year",
            "publisher": "Publisher",
            "standard_reference": "Standard reference system"
        }],
        "digital_source": {
            "source": "Digital source of text",
            "preparation_date": "Date of digital preparation",
            "encoding": "UTF-8",
            "preprocessing": ["List of preprocessing steps"]
        }
    }
}
```

### Practical Examples

#### 1. Greek Example: Aristotle's De Anima
```json
{
    "text_id": "aristotle_de_anima_gr",
    "bibliographic_info": {
        "title": {
            "original": "Περὶ Ψυχῆς",
            "transliterated": "Peri Psychēs",
            "english": "On the Soul"
        },
        "author": {
            "name": {
                "standard": "Aristotle",
                "variants": ["Aristoteles", "Aristū"]
            },
            "dates": {
                "birth": "384 BCE",
                "death": "322 BCE",
                "flourished": "4th century BCE"
            }
        },
        "language": {
            "primary": "Greek",
            "dialects": ["Attic"],
            "script": "Classical Greek"
        }
    },
    "composition_details": {
        "date": {
            "century": "4th century BCE",
            "period": "Classical",
            "certainty": "confirmed"
        },
        "place": {
            "city": "Athens",
            "region": "Attica",
            "modern_country": "Greece"
        }
    }
}
```

#### 2. Arabic Example: Al-Fārābī's Commentary
```json
{
    "text_id": "farabi_de_anima_comm_ar",
    "bibliographic_info": {
        "title": {
            "original": "شرح كتاب النفس لأرسطو",
            "transliterated": "Sharḥ Kitāb al-Nafs li-Arisṭū",
            "english": "Commentary on Aristotle's De Anima"
        },
        "author": {
            "name": {
                "standard": "Al-Fārābī",
                "variants": ["Alfarabius", "Abū Naṣr al-Fārābī"]
            },
            "dates": {
                "birth": "c. 870 CE",
                "death": "950 CE",
                "flourished": "10th century CE"
            }
        },
        "language": {
            "primary": "Arabic",
            "dialects": ["Classical Arabic"],
            "script": "Naskh"
        }
    }
}
```

### Implementation Guidelines

1. **File Naming Convention**
```
[author]_[work]_[language]_[version].json
```
Example: `aristotle_de_anima_gr_v1.json`

2. **Required Fields**
The following fields must be present for all texts:
- text_id
- bibliographic_info.title
- bibliographic_info.author.name.standard
- bibliographic_info.language.primary
- composition_details.date.century
- content_classification.genres
- content_classification.subjects

3. **Character Encoding**
- All files must use UTF-8 encoding
- Greek text should use Unicode Greek ranges
- Arabic text should use Unicode Arabic ranges
- Include appropriate right-to-left markers for Arabic

4. **Dates and Periods**
- Use negative numbers for BCE dates
- Use ranges when exact dates unknown: "c. 870-950 CE"
- Use standard period names:
  - Classical (5th-4th c. BCE)
  - Hellenistic (3rd-1st c. BCE)
  - Imperial (1st-3rd c. CE)
  - Late Antique (4th-6th c. CE)
  - Early Islamic (7th-9th c. CE)
  - Classical Islamic (10th-12th c. CE)

5. **Relationships and Cross-References**
```json
"relationships": {
    "translations": ["List of translation IDs"],
    "commentaries": ["List of commentary IDs"],
    "responses": ["List of response text IDs"],
    "influences": ["List of influenced text IDs"]
}
```

### Quality Control Checklist

- [ ] All required fields present
- [ ] UTF-8 encoding confirmed
- [ ] Dates in standard format
- [ ] Languages properly specified
- [ ] Cross-references validated
- [ ] Special characters properly encoded
- [ ] Relationship links verified

### Integration with Database

The metadata will be stored in the `metadata` JSONB field of the `philosophical_texts` table. To query specific metadata:

```sql
-- Find all texts from a specific period
SELECT title FROM philosophical_texts
WHERE metadata->>'period' = 'Classical';

-- Find all Arabic translations of Greek texts
SELECT title FROM philosophical_texts
WHERE metadata->'translation_details'->>'source_language' = 'Greek'
AND metadata->'bibliographic_info'->'language'->>'primary' = 'Arabic';
```

### Tools for Metadata Creation

1. **Python Script for Metadata Generation**
```python
def create_metadata_template(
    title: str,
    author: str,
    language: str,
    date: str
) -> dict:
    """Creates a basic metadata template with required fields."""
    return {
        "text_id": f"{author.lower()}_{title.lower()}_{language.lower()}",
        "bibliographic_info": {
            "title": {
                "original": "",
                "transliterated": "",
                "english": title
            },
            "author": {
                "name": {
                    "standard": author,
                    "variants": []
                }
            },
            "language": {
                "primary": language
            }
        },
        "composition_details": {
            "date": {
                "century": date
            }
        }
    }
```

### Common Issues and Solutions

1. **Character Encoding Problems**
   - Use a UTF-8 capable editor (VS Code, Sublime Text)
   - Verify encoding with:
     ```python
     with open('metadata.json', encoding='utf-8') as f:
         content = f.read()
     ```

2. **Date Standardization**
   - Use ISO format where possible
   - Include certainty markers
   - Document assumptions about dates

3. **Name Variants**
   - Include all known variants
   - Use standard transliteration
   - Cross-reference with standard authorities

### Next Steps

1. Create metadata templates for your existing corpus
2. Validate all metadata files
3. Import into database
4. Begin relationship mapping

Would you like me to proceed with creating the additional analysis methods next, or would you like to discuss any aspects of the metadata schema in more detail?
