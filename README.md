# Web Watch - Website Time Tracker & Exam Mode

## Overview
Web Watch is a Chrome extension that combines website usage tracking with a secure online examination system. It helps users monitor their daily website activity and provides a robust platform for conducting online examinations with anti-cheating measures.

## Features

### Website Time Tracking
- Real-time tracking of time spent on different websites
- Daily activity visualization with website favicons
- 30-day data retention
- Easy-to-read time format display

### Exam Mode
#### For Invigilators
- Create and manage online exams
- Set exam duration and URL
- Generate unique exam codes
- Track student participation
- View student roll numbers who attempted the exam

#### For Students
- Access exams using unique codes
- Secure exam environment with:
  - Forced fullscreen mode
  - Tab switching prevention
  - Keyboard shortcut blocking
  - Right-click disable
  - Auto-submission on time completion or rule violation

## Technology Stack
- **Frontend**: HTML, CSS, JavaScript, Chrome Extensions API
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: Custom exam code verification

## Installation

### Prerequisites
- Node.js and npm installed
- MongoDB account
- Google Chrome browser

### Backend Setup
1. Clone the repository
```bash
git clone <repository-url>
cd web-watch
```

2. Install dependencies
```bash
npm install
```

3. Configure environment variables
- Create a `.env` file
- Add MongoDB connection string:
```
MONGODB_URI=your_mongodb_connection_string
PORT=4000
```

4. Start the server
```bash
node server.js
```

### Extension Setup
1. Open Google Chrome
2. Navigate to `chrome://extensions/`
3. Enable "Developer mode"
4. Click "Load unpacked"
5. Select the extension directory

## Usage

### Normal Mode
1. Click on the extension icon
2. View your daily website usage statistics
3. Monitor time spent on different websites

### Exam Mode (Invigilator)
1. Click "Exam Mode"
2. Select "Invigilator"
3. Fill in exam details:
   - Exam name
   - Exam URL
   - Exam code
   - Duration
4. Click "Save" to create the exam

### Exam Mode (Student)
1. Click "Exam Mode"
2. Select "Student"
3. Enter the exam code
4. Enter roll number
5. Click "Start Exam"

## Security Features
- Secure exam environment
- Anti-tab switching measures
- Fullscreen enforcement
- Keyboard shortcut blocking
- Auto-submission on violation
- Unique exam codes
- Roll number verification

## API Endpoints
- `POST /addexam`: Create new exam
- `POST /getexam`: Retrieve exam details
- `POST /addrollno`: Add student roll number to exam

## Database Schema
```javascript
Exam Schema:
{
  name: String,
  url: String,
  code: String,
  duration: Number,
  rollnos: Array
}
```

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push to the branch
5. Create a Pull Request

## Future Enhancements
- Student authentication system
- Exam analytics dashboard
- Multiple question formats
- Result generation
- Exam session recovery
- Real-time monitoring dashboard
