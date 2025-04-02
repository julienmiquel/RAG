# Image Metadata Generation and Search System

This project provides functionality for generating and managing image metadata using Google Cloud services. It includes tools for image search, metadata generation, and cloud storage integration.

## Project Structure

The project is organized into several directories, each serving a specific purpose:

- **1_create_datastore/**: Contains scripts and notebooks for creating and managing the data store.
- **2_generate_image_caption_batch/**: Scripts for generating image captions in batch mode.
- **2_generate_image_caption_colab/**: Notebooks for generating image captions using Google Colab.
- **3_front/**: Frontend components and interfaces for the system.
- **4_finetuning/**: Contains notebooks and scripts for fine-tuning image search models.

## Overview

The system consists of several Jupyter notebooks that provide the following main functionalities:

1. **Image Search and Retrieval**
   - Integration with Google Cloud Discovery Engine
   - Advanced search capabilities with natural language understanding
   - Support for multiple regions (US and Europe)

2. **Metadata Generation**
   - Uses Gemini Pro model for image analysis
   - Generates detailed metadata for images
   - Supports batch processing

3. **Cloud Storage Integration**
   - Works with Google Cloud Storage buckets
   - Manages image content and training data

## Setup Requirements

### Prerequisites

- Google Cloud Project with appropriate permissions
- Python environment with required packages

### Required Python Packages

```bash
google-cloud-discoveryengine
google-cloud-aiplatform
vertexai
langchain
```

## Configuration

The system uses the following configuration variables:

```python
PROJECT_ID = "your-project-id"
LOCATION = "us-central1"  # or other supported regions
VERTEX_AI_SEARCH_APP_ID = "your-search-app-id"
VERTEX_AI_SEARCH_DATASTORE_ID = "your-datastore-id"
MODEL = "gemini-1.5-pro-002"
```

## Main Components

### Search Engine

The `search_engine()` function provides advanced search capabilities:

- Natural language query understanding
- Custom fine-tuning
- Support for pagination
- Relevance threshold filtering
- Spell correction

### Metadata Generation

The system uses Gemini Pro model to:

- Analyze image content
- Generate detailed metadata
- Process images in batch mode

### Cloud Storage Integration

- Manages image content in specified buckets
- Handles training data storage
- Supports batch processing operations

## Usage

1. Install required packages:

```bash
pip install --upgrade google-cloud-discoveryengine google-cloud-aiplatform
```

2. Configure your project settings in the notebook

3. Run the desired functions:
   - For search: Use the `search_engine()` function
   - For metadata generation: Use the appropriate metadata generation functions
   - For batch processing: Use the batch processing functions

## Documentation

Detailed documentation for each notebook is available:

- [Train Notebook Documentation](4_finetuning/train_documentation.md)
- [Train V2 Notebook Documentation](4_finetuning/train_v2_documentation.md)
- [Import Generate Image Metadatas Documentation](2_generate_image_caption_colab/import_generate_image_metadatas_documentation.md)
- [Image Metadata System Documentation](2_generate_image_caption_colab/image_metadata_system_documentation.md)

## Error Handling

The system includes error handling for:

- Invalid queries
- Missing or incorrect configurations
- API errors
- Storage access issues

## Security Considerations

- API keys and credentials should be managed securely
- Access to cloud resources should be properly configured
- Data privacy and compliance requirements should be followed

## Support

For issues or questions, please refer to:

- Google Cloud documentation
- Project maintainers
- Internal documentation
