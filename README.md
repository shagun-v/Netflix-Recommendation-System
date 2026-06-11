Netflix Recommendation System
Project Overview

This project develops a personalized movie recommendation system using the Netflix Prize Dataset.

Three recommendation approaches were evaluated:

Popularity-Based Recommendation
Item-Based Collaborative Filtering
Matrix Factorization (SVD)

The objective was to predict user preferences and generate personalized movie recommendations while evaluating recommendation quality using RMSE, MAP@10, and Precision@10.

Dataset

Original Dataset:

Metric	Value
Ratings	100,480,507
Users	480,189
Movies	17,770

Filtered Dataset:

Metric	Value
Ratings	18,687,764
Users	148,083
Movies	4,491
Data Processing Pipeline

The following preprocessing steps were performed:

Parsed Netflix Prize text files
Converted data types to memory-efficient formats
Merged movie metadata
Converted dates to datetime format
Filtered inactive users
Filtered unpopular movies
Generated a clean user-item interaction dataset
Recommendation Models
Popularity-Based Recommendation

Recommends movies using average ratings and rating counts.

Item-Based Collaborative Filtering

Uses movie similarity relationships derived from user ratings.

Matrix Factorization (SVD)

Learns latent user and movie factors to predict unseen ratings and generate recommendations.

Evaluation Metrics
RMSE

Measures rating prediction accuracy.

MAP@10

Measures recommendation ranking quality.

Relevant movie:

Rating ≥ 3.5
Precision@10

Measures relevance of recommended movies.

Results
Model	RMSE	MAP@10	Precision@10
Item-Based CF	1.0429	0.8307	0.1698
SVD	0.9631	0.8792	0.1703
Best Model

SVD achieved the best performance across all evaluation metrics.

Recommendation Example

Selected User:

User ID: 305344

Top Recommendations:

Doctor Zhivago
Nuremberg
Ray
The Incredibles: Bonus Material
Hackers
Repository Structure
Netflix-Recommendation-System/
│
├── notebooks/
├── report/
├── presentation/
├── images/
├── README.md
├── requirements.txt
└── LICENSE
Reproducing Results
Install dependencies
pip install -r requirements.txt
Open notebook
jupyter notebook

Open:

notebooks/NETFLIX_FINAL.ipynb
Run notebook

Execute all cells sequentially.

Future Improvements
Neural Collaborative Filtering
Hybrid Recommendation Systems
Explainable Recommendations
Real-Time Recommendation Pipelines
