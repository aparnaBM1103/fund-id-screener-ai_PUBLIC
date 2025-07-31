# Fund ID Screener.ai

An AI-powered application that automates the extraction and analysis of fund manager information from documents, generating comprehensive reports with AI scoring and summaries.

## 🚀 Quick Start Guide

### Prerequisites
- A Google account (bluemark.co domain) with access to Google Drive and Google Sheets
- Access to BlueMark's Humata.ai with documents organized in folders
- Client documents uploaded onto Humata.ai in the following manner:
    - Overall folder (named after client) that contains all documents
    - A sub-folder within this overall folder that contains ONLY impact reports

### Step-by-Step Instructions

#### 1. 🔐 Google Authentication
**This is the first and most important step!**
A 10-second Loom video of this process is here: https://www.loom.com/share/6f3812bc220d4b78a3d681b2482c0d6f?sid=e6568a76-13fa-46cb-ae69-ea03306bbd72

1. **Access the App**: Open the Fund ID Screener.ai application in your web browser
2. **Authentication Required**: You'll see a "Google Authentication Required" message
3. **Click the Authentication Link**: Click the "🔗 Authenticate with Google" link
4. **Grant Permissions**: 
   - Sign in to your Google account if prompted
   - Click "Allow" to grant the app permission to access your Google Drive and Sheets
5. **Copy the Authorization Code**: 
   - After granting permissions, you'll be redirected to a URL
   - Copy the ENTIRE AUTHORIZATION CODE from the URL [everything after the phrase 'code=' in the URL].
6. **Paste and Submit**: 
   - Return to the app
   - Paste the authorization code in the "Authorization Code" field
   - Click "Submit Authorization Code"
7. **Success**: You should see "✅ Authentication successful!" and it will automatically navigate you to the next portal.

> **⚠️ Important**: If you see an error during authentication, make sure you copied the entire authorization code from the URL.

#### 2. 📋 Configure Your Analysis

Once authenticated, you'll see the main configuration panel in the sidebar:

##### Required Fields (Must be filled):
- **Humata Overall Folder URL**: The URL of your main Humata folder containing documents for Strategy, Governance, and Management analysis
  - Format: `https://app.humata.ai/folder/your-folder-id`
- **Humata Reporting Folder URL**: The URL of your Humata sub-folder containing ONLY impact reports
  - Format: `https://app.humata.ai/folder/your-reporting-folder-id`
- **Client Name**: The name of the fund/client being analyzed (e.g., "Greenacre Ventures")

##### Optional Fields:
- **Google Drive Folder URL**: Where you want the results saved (if left empty, saves to your Drive root).
  - Format: `https://drive.google.com/drive/folders/your-folder-id`
  - Even while testing, please try to create your specific sub-folder (for your test client) within this folder: https://drive.google.com/drive/u/0/folders/1iq7oL9_Q8Le4c1G5zWJmYL4ceroyN0EL. This is just to make sure we store everything in one place. 

##### Template Configuration:
The app comes pre-configured with the latest Fund ID templates. Please reach out to Aparna for any modifications:
- **Strategy Template**: `Run Fund ID 2.0_Strategy (Last Edited: June 24, 2025 at 9:55:45pm EDT)`
- **Governance Template**: `Run Fund ID 2.0_Governance (Last Edited: June 24, 2025 at 9:56:57pm EDT)`
- **ManagementA Template**: `Run Fund ID 2.0_ManagementA (Last Edited: June 24, 2025 at 10:24:46pm EDT)`
- **ManagementB Template**: `Run Fund ID 2.0_ManagementB (Last Edited: June 24, 2025 at 10:25:43pm EDT)`
- **Reporting Template**: `Run Fund ID 2.0_Reporting (Last Edited: June 24, 2025 at 10:27:36pm EDT)`

##### Custom Templates (Optional):
- Add up to 2 custom template names for additional analysis

#### 3. 🚀 Run the Analysis

1. **Review Configuration**: Ensure all required fields are filled
2. **Click "Run Fund ID Extraction"**: The main button in the sidebar
3. **Wait for Processing**: 
   - **Total Time**: 15-20 minutes
   - **DO NOT close the browser tab** during processing
   - The app will appear frozen - this is normal. Don't quit it.
   - Processing continues in the background

#### 4. 📊 Access Your Results

When processing completes, you'll see:

##### Success Indicators:
- ✅ "Fund ID extraction completed!"
- Metrics showing files created, sheets updated, and summaries generated
- Direct links to your Google Sheet

##### Access Your Google Sheet:
- **If you specified a folder**: The sheet is saved in your chosen Google Drive folder
- **If you left folder empty**: The sheet is saved in your Google Drive root
- **Direct Link**: Click the "Open Generated Sheet" link provided
- **Sheet Name**: Format: `[Client Name] - Fund ID Analysis - [Date]`

## 📋 What the App Does

### Processing Steps:
1. **Google Sheet Creation** (1-2 minutes)
   - Creates a new Google Sheet with the Fund ID template structure
   - Organizes data into Strategy, Governance, Management, and Reporting tabs

2. **Humata API Setup** (30-60 seconds)
   - Connects to your Humata workspace
   - Identifies documents in your specified folders

3. **PDF Analysis** (10-15 minutes)
   - Runs each Fund ID template against your documents
   - Extracts structured data and responses

4. **AI Scoring** (2-3 minutes)
   - Uses Google Gemini AI to score responses
   - Generates numerical ratings for each question

5. **Summary Generation** (1-2 minutes)
   - Uses Claude AI to create qualitative summaries
   - Provides insights and recommendations

### Output Structure:
- **Strategy Tab**: Investment strategy analysis and scoring
- **Governance Tab**: Fund governance structure and compliance
- **Management Tab**: Management team analysis and capabilities
- **Reporting Tab**: Reporting structure and transparency
- **Summary Tab**: Overall fund assessment and recommendations

## 🔧 Troubleshooting & FAQs

### Authentication Issues
**Q: I get an error during Google authentication**
- Make sure you copied the entire authorization code from the URL
- Try refreshing the page and starting the authentication process again
- Ensure you're using a supported browser (Chrome, Firefox, Safari, Edge)

**Q: The authentication link doesn't work**
- Check your internet connection
- Try opening the link in a new tab
- Ensure you're not blocked by corporate firewalls

### Processing Issues
**Q: The app seems frozen during processing**
- This is normal! The app processes in the background
- **DO NOT close the browser tab** - this will interrupt the process
- Processing takes 15-20 minutes total
- You'll see results when it completes

**Q: I get an error about missing required fields**
- Ensure you've filled in:
  - Humata Overall Folder URL
  - Humata Reporting Folder URL
  - Client Name
  - All 5 Fund ID template names

**Q: The process fails after starting**
- Check that your Humata folder URLs are correct and accessible
- Ensure your documents are properly uploaded to Humata
- Verify that the Fund ID templates exist in your Humata workspace

### Google Sheets Issues
**Q: I can't find my generated sheet**
- Check your Google Drive root folder first
- If you specified a folder, check that specific folder
- Look for files named: `[Client Name] - Fund ID Analysis - [Date]`

**Q: The sheet is created but empty**
- This usually means there was an issue with some of the APIs - reach out to Aparna to refresh APi credentials (this is a quick fix but she will have to do it directly)
- Ensure your documents are accessible in the specified folders

### General Issues
**Q: The app fails to load or crashes**
- Refresh the page and try again
- Clear your browser cache and cookies
- Try using a different browser

**Q: I get a timeout error**
- The app has a 20-minute processing limit - which means that for extremely large document sets, the process may timeout
- Try with fewer documents or contact support

### Need Help?
**If the app fails or you encounter any issues:**
- **Slack Aparna** for a quick fix
- Include the error message and what you were trying to do
- Provide your client name and Humata folder URLs for faster resolution

## 📞 Support

For technical support or questions:
- **Primary Contact**: Slack Aparna
- **Include**: Error messages, client name, and steps you were following

## 🔒 Security & Privacy

- Your Google authentication is handled securely through OAuth 2.0
- No passwords or sensitive data are stored by the app
- All processing is done in memory and not permanently/locally stored
- The app is restricted access only to select team members. There is dual access control as follows:
- a) The streamlit web app is only accesible to select team members (added individually)
- b) Even after getting access to the streamlit web app, only team members with a bluemark.co domain are allowed to self-authenticate using their Google domain

## 📝 Version Information

- **Current Fund ID Version**: Fund ID 2.0
- **Last Updated**: July 30, 2025
- **Supported Platforms**: Web browsers (Chrome, Firefox, Safari, Edge)
- **Processing Time**: <20 minutes per analysis

---

**Happy Analyzing! 🎉**
