# Project Files Inventory

## Deepfake Detection using Deep Learning

**Document Generated:** 2025-11-12  
**Purpose:** Complete catalog of all project files organized by directory with descriptions and ordering.

---

## Table of Contents

1. [Root Level Files](#root-level-files)
2. [Django Application](#django-application)
3. [Model Creation](#model-creation)
4. [Documentation](#documentation)
5. [File Statistics](#file-statistics)

---

## Root Level Files

### Configuration & Metadata (Ordered)

| #   | File Name                    | Type        | Purpose                                                    |
| --- | ---------------------------- | ----------- | ---------------------------------------------------------- |
| 1   | `.all-contributorsrc`        | JSON Config | Contributors configuration file for all-contributors bot   |
| 2   | `LICENSE`                    | License     | Project license file                                       |
| 3   | `README.md`                  | Markdown    | Main project README with overview and setup instructions   |
| 4   | `prd.md`                     | Markdown    | Product Requirements Document (comprehensive project spec) |
| 5   | `PROJECT_FILES_INVENTORY.md` | Markdown    | This file - complete inventory of all project files        |

### Directories at Root

- `Django Application/` - Main web application and inference backend
- `Model Creation/` - Jupyter notebooks and helpers for model training/preprocessing
- `Documentation/` - Additional documentation
- `github_assets/` - GitHub-related assets (images, etc.)

---

## Django Application

**Path:** `Django Application/`  
**Purpose:** Core Django web application for deepfake detection inference

### Application Root Configuration Files

| #   | File Name          | Type      | Purpose                                   |
| --- | ------------------ | --------- | ----------------------------------------- |
| 1   | `manage.py`        | Python    | Django management CLI entry point         |
| 2   | `requirements.txt` | Text      | Python package dependencies               |
| 3   | `db.sqlite3`       | SQLite DB | Django development database               |
| 4   | `Dockerfile`       | Docker    | Container image definition for Django app |
| 5   | `.dockerignore`    | Config    | Files to exclude from Docker build        |
| 6   | `.gitignore`       | Config    | Files to exclude from Git                 |
| 7   | `README.md`        | Markdown  | Django app specific README                |

### Directory: `project_settings/`

**Purpose:** Django project configuration and WSGI/ASGI entry points

| #   | File Name      | Type   | Purpose                                                        |
| --- | -------------- | ------ | -------------------------------------------------------------- |
| 1   | `__init__.py`  | Python | Package marker                                                 |
| 2   | `settings.py`  | Python | Main Django configuration (DB, apps, middleware, static files) |
| 3   | `urls.py`      | Python | Root URL routing configuration                                 |
| 4   | `wsgi.py`      | Python | WSGI application entry for production servers (Gunicorn)       |
| 5   | `asgi.py`      | Python | ASGI application entry for async servers                       |
| 6   | `__pycache__/` | Cache  | Python bytecode cache (auto-generated)                         |

### Directory: `ml_app/`

**Purpose:** Main ML app - models, views, forms, and templates for inference

#### Python Source Files

| #   | File Name      | Type   | Purpose                                                           |
| --- | -------------- | ------ | ----------------------------------------------------------------- |
| 1   | `__init__.py`  | Python | Package marker                                                    |
| 2   | `apps.py`      | Python | Django app configuration                                          |
| 3   | `models.py`    | Python | Django ORM models (database schemas)                              |
| 4   | `views.py`     | Python | **Core logic** - request handlers for upload/prediction endpoints |
| 5   | `urls.py`      | Python | URL routing for ml_app endpoints                                  |
| 6   | `forms.py`     | Python | Django forms for file upload validation                           |
| 7   | `admin.py`     | Python | Django admin interface configuration                              |
| 8   | `tests.py`     | Python | Unit tests for ml_app                                             |
| 9   | `__pycache__/` | Cache  | Python bytecode cache (auto-generated)                            |

#### Directory: `templates/`

**Purpose:** HTML templates for web UI

| #   | File Name        | Type | Purpose                                    |
| --- | ---------------- | ---- | ------------------------------------------ |
| 1   | `index.html`     | HTML | Landing/home page with file upload UI      |
| 2   | `predict.html`   | HTML | Prediction results display page            |
| 3   | `about.html`     | HTML | About/information page                     |
| 4   | `cuda_full.html` | HTML | CUDA availability/system info display page |
| 5   | `404.html`       | HTML | 404 error page                             |

### Directory: `models/`

**Purpose:** Pre-trained PyTorch models for inference (trained model artifacts)

| #   | File Name                                  | Type    | Purpose       | Accuracy | Frames | Dataset       |
| --- | ------------------------------------------ | ------- | ------------- | -------- | ------ | ------------- |
| 1   | `model_84_acc_10_frames_final_data.pt`     | PyTorch | Trained model | 84%      | 10     | Final Data    |
| 2   | `model_87_acc_20_frames_final_data.pt`     | PyTorch | Trained model | 87%      | 20     | Final Data    |
| 3   | `model_89_acc_40_frames_final_data.pt`     | PyTorch | Trained model | 89%      | 40     | Final Data    |
| 4   | `model_90_acc_20_frames_FF_data.pt`        | PyTorch | Trained model | 90%      | 20     | FaceForensics |
| 5   | `model_90_acc_60_frames_final_data.pt`     | PyTorch | Trained model | 90%      | 60     | Final Data    |
| 6   | `model_93_acc_100_frames_celeb_FF_data.pt` | PyTorch | Trained model | 93%      | 100    | Celeb + FF    |
| 7   | `model_95_acc_40_frames_FF_data.pt`        | PyTorch | Trained model | 95%      | 40     | FaceForensics |
| 8   | `model_97_acc_100_frames_FF_data.pt`       | PyTorch | Trained model | 97%      | 100    | FaceForensics |
| 9   | `model_97_acc_60_frames_FF_data.pt`        | PyTorch | Trained model | 97%      | 60     | FaceForensics |
| 10  | `model_97_acc_80_frames_FF_data.pt`        | PyTorch | Trained model | 97%      | 80     | FaceForensics |

**Note:** Model names encode: `model_[accuracy]_acc_[frame_count]_frames_[dataset].pt`

### Directory: `static/`

**Purpose:** Static assets (CSS, JS, images, JSON models for face-api)

#### Subdirectory: `css/`

| #   | File Name       | Type | Purpose                                                          |
| --- | --------------- | ---- | ---------------------------------------------------------------- |
| 1   | `jquery-ui.css` | CSS  | jQuery UI framework styles with custom dark theme overrides      |
| 2   | `styles.css`    | CSS  | **Main stylesheet** - project dark tech theme with CSS variables |

#### Subdirectory: `js/`

| #   | File Name             | Type       | Purpose                                                    |
| --- | --------------------- | ---------- | ---------------------------------------------------------- |
| 1   | `script.js`           | JavaScript | Main client-side logic for upload, preview, and prediction |
| 2   | `jquery-3.4.1.min.js` | JavaScript | jQuery library (minified)                                  |
| 3   | `jquery-3.5.0.min.js` | JavaScript | jQuery library (minified) - newer version                  |
| 4   | `jquery-ui.min.js`    | JavaScript | jQuery UI framework (minified)                             |
| 5   | `face-api.js`         | JavaScript | Face-api.js library for client-side face detection         |
| 6   | `face-api.min.js`     | JavaScript | Face-api.js library (minified)                             |
| 7   | `popper.min.js`       | JavaScript | Popper.js positioning library (minified)                   |

#### Subdirectory: `json/`

**Purpose:** Pre-trained face-api models (TensorFlow.js format with shards and manifests)

| #   | File Name                                           | Type        | Purpose                                                       |
| --- | --------------------------------------------------- | ----------- | ------------------------------------------------------------- |
| 1   | `age_gender_model-shard1`                           | Binary      | Age/Gender model weights shard                                |
| 2   | `age_gender_model-weights_manifest.json`            | JSON        | Age/Gender model manifest                                     |
| 3   | `face_expression_model-shard1`                      | Binary      | Face expression model weights shard                           |
| 4   | `face_expression_model-weights_manifest.json`       | JSON        | Face expression model manifest                                |
| 5   | `face_landmark_68_model-shard1`                     | Binary      | Face landmark 68-point model weights shard                    |
| 6   | `face_landmark_68_model-weights_manifest.json`      | JSON        | Face landmark 68-point model manifest                         |
| 7   | `face_landmark_68_tiny_model-shard1`                | Binary      | Face landmark tiny model weights shard                        |
| 8   | `face_landmark_68_tiny_model-weights_manifest.json` | JSON        | Face landmark tiny model manifest                             |
| 9   | `face_recognition_model-shard1`                     | Binary      | Face recognition model weights shard 1                        |
| 10  | `face_recognition_model-shard2`                     | Binary      | Face recognition model weights shard 2                        |
| 11  | ...                                                 | Binary/JSON | Additional model shards and manifests (truncated for brevity) |

#### Subdirectory: `bootstrap/`

| #   | File Name           | Type | Purpose                                   |
| --- | ------------------- | ---- | ----------------------------------------- |
| 1   | `bootstrap.min.css` | CSS  | Bootstrap framework stylesheet (minified) |

#### Subdirectory: `images/`

| #                           | File Name | Type   | Purpose                      |
| --------------------------- | --------- | ------ | ---------------------------- |
| (empty or project-specific) | (various) | Images | Project images, icons, logos |

### Directory: `templates/` (Base Templates)

**Purpose:** Base HTML templates shared across the Django app

| #   | File Name      | Type | Purpose                                            |
| --- | -------------- | ---- | -------------------------------------------------- |
| 1   | `base.html`    | HTML | Base template with header, footer, static includes |
| 2   | `nav-bar.html` | HTML | Navigation bar component                           |
| 3   | `footer.html`  | HTML | Footer component                                   |

### Directory: `bin/`

**Purpose:** Deployment and server startup scripts

| #   | File Name           | Type        | Purpose                                     |
| --- | ------------------- | ----------- | ------------------------------------------- |
| 1   | `gunicorn_start.sh` | Bash Script | Production server startup script (Gunicorn) |

### Directory: `nginx/`

**Purpose:** Nginx reverse proxy configuration and Docker setup

| #   | File Name    | Type   | Purpose                                        |
| --- | ------------ | ------ | ---------------------------------------------- |
| 1   | `Dockerfile` | Docker | Container image for Nginx reverse proxy        |
| 2   | `nginx.conf` | Config | Nginx configuration for proxying to Django app |

### Directory: `uploaded_images/`

**Purpose:** Storage for uploaded images during inference (runtime generated)

| #   | File Name    | Type | Purpose                        |
| --- | ------------ | ---- | ------------------------------ |
| 1   | `Readme.txt` | Text | Placeholder/documentation file |

### Directory: `uploaded_videos/`

**Purpose:** Storage for uploaded videos during inference (runtime generated)

| #   | File Name    | Type | Purpose                        |
| --- | ------------ | ---- | ------------------------------ |
| 1   | `Readme.txt` | Text | Placeholder/documentation file |

### Directory: `__pycache__/` (Auto-generated)

Python bytecode cache - regenerated on runtime, not part of source control.

---

## Model Creation

**Path:** `Model Creation/`  
**Purpose:** Jupyter notebooks and helper scripts for model training, preprocessing, and dataset creation

### Jupyter Notebooks

| #   | File Name                   | Type             | Purpose                                                      |
| --- | --------------------------- | ---------------- | ------------------------------------------------------------ |
| 1   | `preprocessing.ipynb`       | Jupyter Notebook | Data preprocessing pipeline (cleaning, normalization)        |
| 2   | `Model_and_train_csv.ipynb` | Jupyter Notebook | Model architecture definition and training with CSV metadata |
| 3   | `Predict.ipynb`             | Jupyter Notebook | Inference demo and prediction helper notebook                |
| 4   | `Readme.md`                 | Markdown         | Model creation documentation and usage guide                 |

### Directory: `Helpers/`

**Purpose:** Utility notebooks and scripts for data preparation

| #   | File Name                          | Type             | Purpose                                                   |
| --- | ---------------------------------- | ---------------- | --------------------------------------------------------- |
| 1   | `deepfake-starter-kit.ipynb`       | Jupyter Notebook | Starter template for deepfake detection workflows         |
| 2   | `Create_csv_from_glob.ipynb`       | Jupyter Notebook | Generate CSV metadata from file glob patterns             |
| 3   | `for_Balancing_data.ipynb`         | Jupyter Notebook | Dataset balancing utilities and analysis                  |
| 4   | `Remove_audio_altered_files.ipynb` | Jupyter Notebook | Audio removal/filtering for video files                   |
| 5   | `copy real and fake .ipynb`        | Jupyter Notebook | Script to copy real/fake samples into organized structure |
| 6   | `label_json_to_csv.py`             | Python           | Convert JSON labels/metadata to CSV format                |

### Directory: `labels/`

**Purpose:** Dataset metadata and labels

| #   | File Name            | Type | Purpose                                                   |
| --- | -------------------- | ---- | --------------------------------------------------------- |
| 1   | `Gobal_metadata.csv` | CSV  | Global metadata file with labels for all training samples |

---

## Documentation

**Path:** `Documentation/`  
**Purpose:** Additional project documentation

| #   | File Name   | Type     | Purpose                                          |
| --- | ----------- | -------- | ------------------------------------------------ |
| 1   | `README.md` | Markdown | Additional documentation and reference materials |

---

## GitHub Assets

**Path:** `github_assets/`  
**Purpose:** Assets for GitHub repository (badges, diagrams, screenshots)

| #         | File Name          | Type            | Purpose                  |
| --------- | ------------------ | --------------- | ------------------------ |
| (various) | (images, diagrams) | Images/Diagrams | GitHub repository assets |

---

## File Statistics

### File Count by Type

| File Type                 | Count    | Purpose                                                 |
| ------------------------- | -------- | ------------------------------------------------------- |
| Python (.py)              | 9        | Core application logic                                  |
| Jupyter Notebook (.ipynb) | 7        | Training/preprocessing/demo                             |
| HTML (.html)              | 8        | Web UI templates                                        |
| CSS (.css)                | 2        | Styling and theming                                     |
| JavaScript (.js)          | 7        | Client-side logic and libraries                         |
| JSON (.json)              | 11+      | Face-api model manifests and config                     |
| PyTorch Model (.pt)       | 10       | Pre-trained inference models                            |
| Docker (Dockerfile)       | 2        | Container definitions                                   |
| Configuration             | 6+       | .gitignore, .dockerignore, nginx.conf, requirements.txt |
| Markdown (.md)            | 4        | Documentation                                           |
| **Total Documented**      | **~65+** | Full project scope                                      |

### Directory Hierarchy Summary

```
Deepfake_detection_using_deep_learning-master/
├── Root Config & Docs (5 files)
├── Django Application/ (main app)
│   ├── project_settings/ (5 Python files)
│   ├── ml_app/ (9 Python files, 5 HTML templates)
│   ├── models/ (10 PyTorch .pt files)
│   ├── static/ (CSS, JS, JSON, Bootstrap)
│   ├── templates/ (3 base HTML files)
│   ├── nginx/ (2 files)
│   ├── bin/ (1 script)
│   ├── uploaded_images/ (1 placeholder)
│   └── uploaded_videos/ (1 placeholder)
├── Model Creation/ (7 notebooks + helpers)
│   ├── Helpers/ (6 notebook/script files)
│   └── labels/ (1 CSV metadata file)
├── Documentation/ (1 markdown file)
└── github_assets/ (various)
```

---

## File Access Order (Recommended for New Developers)

### Phase 1: Project Overview

1. `README.md` (root) - Project goals and quickstart
2. `prd.md` - Comprehensive project specification
3. `Django Application/README.md` - App-specific setup

### Phase 2: Setup & Environment

1. `requirements.txt` - Dependencies
2. `Django Application/Dockerfile` - Containerization
3. `nginx/nginx.conf` - Reverse proxy config

### Phase 3: Application Logic

1. `project_settings/settings.py` - Django config
2. `project_settings/urls.py` - URL routing
3. `ml_app/views.py` - **Core prediction logic**
4. `ml_app/forms.py` - Upload form handling
5. `ml_app/urls.py` - App-level routing

### Phase 4: Frontend

1. `ml_app/templates/base.html` - Base HTML structure
2. `ml_app/templates/index.html` - Upload UI
3. `ml_app/templates/predict.html` - Results display
4. `static/css/styles.css` - Main styling
5. `static/js/script.js` - Client-side logic

### Phase 5: Models & Inference

1. `models/` - Review available pre-trained models
2. `Model Creation/preprocessing.ipynb` - Data prep
3. `Model Creation/Model_and_train_csv.ipynb` - Training
4. `Model Creation/Predict.ipynb` - Inference examples

### Phase 6: Deployment

1. `bin/gunicorn_start.sh` - Production startup
2. `nginx/Dockerfile` - Nginx container
3. `Django Application/Dockerfile` - App container

---

## Notes

- **Python Environment:** Use `requirements.txt` to install dependencies into a virtual environment.
- **Models:** The `models/` directory contains pre-trained PyTorch .pt files; no training required for basic inference.
- **Static Assets:** Face-api JSON models in `static/json/` are used for client-side face detection/landmarking.
- **Database:** `db.sqlite3` is the development database; migrations are managed via `manage.py`.
- **GPU Support:** CUDA compatibility is detected at runtime; see `cuda_full.html` template.

---

**Document Version:** 1.0  
**Last Updated:** 2025-11-12  
**Total Files Documented:** 65+
