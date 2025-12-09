# Plum_Ass - Employee Benefits Assistant

A React-based web application that helps employees understand and access their health benefits using AI-powered classification and personalized action plans.

## Features

- **Health Need Classification**: Uses Google Gemini AI to classify employee health needs into categories:
  - Dental
  - OPD (Out-Patient Department)
  - Vision
  - Mental Health

- **Benefit Information**: Displays relevant benefits based on classification
- **Personalized Action Plans**: Generates step-by-step action plans to avail benefits
- **Responsive Design**: Built with Tailwind CSS for mobile-friendly interface

## Tech Stack

- **Frontend**: React 18
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **AI Integration**: Google Gemini API (gemini-2.5-flash)
- **Package Manager**: npm
- **Routing**: React Router v6

## Project Structure

```
src/
├── components/
│   ├── Screen1Input.jsx          # User input screen
│   ├── Screen2Classification.jsx # Health need classification
│   ├── Screen3Benefits.jsx       # Benefits display
│   └── Screen4ActionPlan.jsx     # Action plan generation
├── services/
│   └── aiService.js             # Google Gemini API integration
├── data/
│   └── benefits.json            # Benefits data
├── App.jsx                       # Main app component
├── main.jsx                      # Entry point
└── index.css                     # Global styles
```

## Setup & Installation

### Prerequisites
- Node.js (v16+)
- npm or yarn
- Google Gemini API Key

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/falak-n/Plum_Ass.git
   cd Plum_Ass
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   VITE_GEMINI_API_KEY=your_api_key_here
   ```

   To get an API key:
   - Visit [Google AI Studio](https://aistudio.google.com/apikey)
   - Click "Create API Key"
   - Copy and paste it into `.env`

4. **Start the development server**
   ```bash
   npm run dev
   ```
   The app will be available at `http://localhost:5173`

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## Usage

1. **Screen 1**: Enter your health concern/question
2. **Screen 2**: The app classifies your need using AI
3. **Screen 3**: View relevant benefits for your category
4. **Screen 4**: Get a personalized action plan to access the benefit

## API Integration

The app uses the **Google Generative AI (Gemini) API** for:
- Classifying health needs into benefit categories
- Generating personalized 3-step action plans

### API Configuration

- **Base URL**: `https://generativelanguage.googleapis.com/v1/models/`
- **Model**: `gemini-2.5-flash` (optimized for speed and intelligence)
- **Authentication**: API key in header and query parameter

## Environment Variables

| Variable | Description |
|----------|-------------|
| `VITE_GEMINI_API_KEY` | Google Gemini API key for authentication |

## Important Security Notes

⚠️ **Never commit your `.env` file to version control!**

The `.gitignore` file already excludes:
- `.env`
- `.env.local`
- `node_modules/`
- `dist/`

## Browser Compatibility

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)

## Architecture & Code Structure

### Component Structure
- **`App.jsx`**: Main navigation and state management for multi-screen flow
- **`Screen1Input.jsx`**: Free-text input screen for health concerns
- **`Screen2Classification.jsx`**: AI classification with loading indicator
- **`Screen3Benefits.jsx`**: Benefit cards display based on category
- **`Screen4ActionPlan.jsx`**: AI-generated action plan screen with regenerate option

### Services
- **`services/aiService.js`**: Gemini API integration with error handling and fallbacks

### Data
- **`data/benefits.json`**: Mock benefits data organized by categories

### Key Features of Architecture
- ✅ Multi-screen flow with smooth navigation
- ✅ AI-powered classification using Google Gemini 2.5 Flash
- ✅ Loading indicators during AI processing
- ✅ Benefit cards with coverage and descriptions
- ✅ AI-generated 3-step action plans
- ✅ Regenerate option for action plans
- ✅ Error handling and fallback responses
- ✅ Clean, formal UI with Tailwind CSS

## How It Works

### Classification Process
1. User enters their health concern
2. AI analyzes the text and classifies it into one of four categories
3. If classification fails, defaults to OPD

### Benefit Display
1. Based on the category, relevant benefits are displayed
2. Each benefit shows title, description, and eligibility

### Action Plan Generation
1. User selects a benefit
2. AI generates a personalized 3-step action plan
3. Steps are specific to the benefit and category

## Known Issues & Future Improvements

- Occasionally misclassifies when input is vague
- Next improvement: Add clarifying question fallback for ambiguous inputs

## Contributing

Feel free to submit issues and enhancement requests!

## License

This project is open source and available under the MIT License.

## Support

For issues or questions:
1. Check existing GitHub issues
2. Create a new issue with detailed description
3. Include error messages and screenshots if applicable

---

**Made with ❤️ for better employee benefits access**

