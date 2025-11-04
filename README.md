# Screenshot Generator Web Application

A Python Flask-based web application that captures screenshots of any website using the ScreenshotBase API.

## Features

- 📸 Capture screenshots of any publicly accessible website
- 🖼️ Multiple format support (PNG, JPEG, WebP)
- 📄 Full page screenshot option
- 🎨 Clean and responsive user interface
- ⚡ Fast and reliable screenshot generation

## Project Structure

```
screenshot-generator/
├── .venv/              # Virtual environment
├── static/             # Static files (generated screenshots)
├── templates/          # HTML & CSS templates
│   └── index.html      # Main page template
│   └── style.css       # Stylesheet
├── .env                # Environment variables (API key)
├── .gitignore          # Git ignore file
└── app.py              # Main Flask application
```

## Prerequisites

- Python 3.7 or higher
- pip (Python package installer)
- ScreenshotBase API key

## Installation

1. **Clone the repository** (or download the files)
   ```bash
   git clone <your-repository-url>
   cd screenshot-generator
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv .venv
   ```

3. **Activate the virtual environment**
   - Windows:
     ```bash
     .venv\Scripts\activate
     ```
   - macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```

4. **Install required packages**
   ```bash
   pip install flask requests
   ```

5. **Set up your API key**
   - Create a `.env` file in the root directory
   - Add your ScreenshotBase API key:
     ```
     SCREENSHOTBASE_API_KEY=your_api_key_here
     ```
   - Or set it as an environment variable in your system

## Usage

1. **Start the Flask application**
   ```bash
   python app.py
   ```

2. **Open your browser**
   Navigate to `http://localhost:5000`

3. **Generate screenshots**
   - Enter the URL of the website you want to capture
   - Select your preferred format (PNG, JPEG, or WebP)
   - Toggle "Full Page" if you want to capture the entire page
   - Click "Capture Screenshot"

## Configuration

### API Key

The application uses the ScreenshotBase API. You can configure the API key in two ways:

1. **Environment variable** (recommended for production):
   ```bash
   export SCREENSHOTBASE_API_KEY="your_api_key_here"
   ```

2. **Direct in code** (for testing only):
   Edit `app.py` and replace the default API key

### Screenshot Formats

Supported formats:
- **PNG** - Lossless compression, best quality
- **JPEG** - Compressed, smaller file size
- **WebP** - Modern format, good balance

## API Information

This application uses the [ScreenshotBase API](https://api.screenshotbase.com/):
- Endpoint: `https://api.screenshotbase.com/v1/take`
- Authentication: API key via header
- Timeout: 30 seconds

## File Structure Details

- **app.py** - Main Flask application with route handlers and API integration
- **templates/index.html** - Frontend HTML template
- **static/** - Directory for CSS files and generated screenshots
- **.env** - Environment variables (not tracked in git)
- **.gitignore** - Specifies files to ignore in version control
- **.venv/** - Python virtual environment

## Error Handling

The application includes basic error handling for:
- Network timeouts
- Invalid URLs
- API errors
- Failed screenshot generation

Errors are logged to the console for debugging.

## Security Notes

⚠️ **Important:**
- Never commit your `.env` file or API keys to version control
- The `.gitignore` file is configured to exclude sensitive files
- Consider using environment variables in production
- The default API key in the code should be replaced with your own

## Development

To run in development mode:
```bash
python app.py
```

The application runs with `debug=True` by default, which enables:
- Auto-reload on code changes
- Detailed error messages
- Interactive debugger

**Note:** Disable debug mode in production!

## Troubleshooting

**Screenshot not generating?**
- Check your API key is valid
- Ensure the target URL is publicly accessible
- Verify internet connectivity
- Check console for error messages

**Module not found errors?**
- Ensure virtual environment is activated
- Install all required packages: `pip install flask requests`

## Dependencies

- **Flask** - Web framework
- **requests** - HTTP library for API calls

## License

This project is open source and available for personal and commercial use.

## Support

For issues with:
- The application: Check console logs and error messages
- ScreenshotBase API: Visit [ScreenshotBase Documentation](https://screenshotbase.com/docs)

---

Made with ❤️ using Flask and ScreenshotBase API