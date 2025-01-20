Quiz Performance Analyzer and Recommendations
Project Overview
This project aims to analyze quiz performance and provide personalized recommendations to students to improve their preparation. The solution fetches data from multiple APIs, analyzes quiz submissions, identifies patterns in student performance, and generates actionable insights and recommendations.

Setup Instructions
Prerequisites
Python 3.x

Required Python libraries:
requests
pandas
numpy
matplotlib
seaborn
json

Installation
Clone the repository:

git clone https://github.com/RURD9915/Quiz_analyser.git
cd Quiz_analyser


Install the required libraries:

pip install requests pandas numpy matplotlib seaborn

Usage
Run the script:

python main.py

The script will fetch data from the APIs, analyze the data, generate insights, provide recommendations, and visualize the results.



Approach Description

Data Loading
The script starts by loading data from three APIs:
Current Quiz Data (QUIZ_ENDPOINT)
Quiz Submission Data (QUIZ_SUBMISSION_ENDPOINT)
Historical Data (API_ENDPOINT)

Data Analysis
Current Quiz Data:
Analyzes the latest quiz submission, including total questions, correct and incorrect answers, and accuracy.
Provides detailed feedback for each question, including the user's response, correct answer, and explanation.

Historical Data:
Analyzes performance data from the last five quizzes.
Calculates average accuracy for each topic.
Performs comparative analysis using fields like better_than and rank_text.

Generating Insights:
Identifies weak areas, strong areas, and improvement trends based on average accuracy by topic.
Highlights specific topics where the student excels or needs improvement.

Providing Recommendations:
Generates actionable recommendations based on insights and comparative analysis.
Suggests specific topics and strategies to focus on to improve performance.

Generating Student Labels:
Assigns labels to students based on their performance, such as "Balanced Learner," "Conceptual Learner," and "Needs Attention."
These labels help define the student's learning persona and provide additional insights.

Visualizing Data
Generates a plot of topic-wise average accuracy for visual representation.
This helps in visually understanding the student's performance across different topics.

Why Some Data Elements Are Not Used
Certain elements like difficulty_level are present but not utilized in our analysis because they are set to null in the data. Without meaningful values, these fields can't contribute to our analysis and recommendations.

Conclusion
This solution provides a comprehensive analysis of quiz performance, generates personalized insights, and offers actionable recommendations to help students improve their preparation effectively.
