# Group-Project-3
---
## GROUP 1 PROJECT 3 TEAM MEMBERS
 Project 2 presented on June 2, 2025 by Group 1 Team Members

 *Michael Hnidash*  
 *Alexander Lin*  
 *Nan Shi*   
 *Kevin Rivera*  
 *Sofia Frrokaj*  

### **Project Overview**

# Smart Recipe App

This is a Streamlit-based web application that generates weekly meal plans and provides nutrition tips using Google Gemini AI.

## Features

- **Customizable Recipe Search:**  
  Users can select diet preferences, specify ingredients to include/exclude, set maximum cooking time, and choose the number of servings.

- **AI-Powered Nutrition Tips:**  
  The app uses Google Gemini AI to generate healthy cooking or nutrition tips based on the provided ingredients.

- **Weekly Meal Plan:**  
  Generates a 7-day meal plan with recipes, images, and links to full instructions.

- **Downloadable Plan:**  
  Users can download their weekly meal plan as a `.txt` file.

## How It Works

1. **User Input:**  
   Fill out the form to specify dietary preferences and ingredients.

2. **Nutrition Tip:**  
   The app displays a nutrition tip generated by Gemini AI.

3. **Recipe Generation:**  
   On form submission, the app fetches 7 recipes matching the criteria using the [`get_recipes`](../services/api_utils.py) function.

4. **Weekly Plan:**  
   Recipes are assigned to days of the week and displayed. The plan can be downloaded.

## Key Dependencies

- [Streamlit](https://streamlit.io/)
- [google-generativeai](https://pypi.org/project/google-generativeai/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)

## Environment Variables

- `GEMINI_API_KEY`: API key for Google Gemini AI.

## File Structure

- `frontend/app_full_fixed.py`: Main Streamlit app.
- `services/api_utils.py`: Contains the [`get_recipes`](../services/api_utils.py) function for fetching recipes.

## Usage

1. Install dependencies:
   ```sh
   pip install streamlit google-generativeai python-dotenv
   ```

2. Set up your `.env` file with your Gemini API key:
   ```
   GEMINI_API_KEY=your_api_key_here
   ```

3. Run the app:
   ```sh
   streamlit run frontend/app_full_fixed.py
   ```
