# Bible Study App 📖

A comprehensive React Native application built with Expo for creating and managing Bible study sessions. This app integrates AWS Amplify for backend services, OpenAI for intelligent content generation, and provides both individual and community study features.

## 🚀 Features

- **Intelligent Session Generation**: AI-powered Bible study questions using OpenAI GPT-4
- **AWS Authentication**: Secure user management with AWS Cognito
- **Community Studies**: Collaborative Bible study sessions
- **Multiple Bible Versions**: Support for various Bible translations (NIV, ESV, etc.)
- **Cross-Platform**: Runs on iOS, Android, and Web
- **Offline Support**: Save and access sessions offline
- **Customizable Studies**: Tailored content for different group types (Family, Youth, etc.)

## 🛠 Tech Stack

- **Frontend**: React Native with Expo
- **Backend**: AWS Amplify (Cognito, Lambda, API Gateway)
- **AI Integration**: OpenAI GPT-4 API
- **Styling**: NativeWind (Tailwind CSS for React Native)
- **Navigation**: Expo Router with file-based routing
- **State Management**: React Hooks
- **Development**: TypeScript, ESLint

## 📋 Prerequisites

Ensure you have the following installed:

- **Node.js**: v22.1.0 (recommended)
- **npm**: Latest version
- **Expo CLI**: Global installation required
- **EAS CLI**: For building and deployment
- **AWS Account**: For Amplify services
- **OpenAI API Key**: For AI-powered content generation

## 🔧 Installation & Setup

### 1. Node.js Setup
```bash
# Using nvm (recommended)
nvm install 22.1.0
nvm use 22.1.0

# Verify installation
node --version
npm --version
```

### 2. Global Dependencies
```bash
npm install -g expo-cli@latest
npm install -g @aws-amplify/cli
npm install -g eas-cli
```

### 3. Project Setup
```bash
# Clone the repository
git clone <repository-url>
cd bible-study-app

# Install dependencies
npm install

# Configure AWS Amplify (if not already configured)
amplify configure
amplify pull --appId d2tpl0orcw9sl6 --envName dev
```

### 4. Environment Configuration
Create a `.env` file in the root directory:
```bash
OPENAI_API_KEY=your_openai_api_key_here
```

## 🚀 Development

### Start Development Server
```bash
# Start Expo development server
npm start
# or
expo start

# Platform-specific commands
npm run android    # Android emulator
npm run ios        # iOS simulator  
npm run web        # Web browser
```

### Development Workflow
1. **File-based Routing**: Add screens in the `app/` directory
2. **Components**: Reusable components in `app/components/`
3. **Screens**: Main application screens in `app/screens/`
4. **AWS Configuration**: Auto-generated in `app/aws-exports.js`

## 🏗 Building & Deployment

### Development Builds
```bash
# iOS Simulator
eas build --platform ios --profile ios-simulator

# Android Development
eas build --platform android --profile development
```

### Production Builds
```bash
# iOS Production
eas build --platform ios --profile production

# Android Production  
eas build --platform android --profile production
```

### Deployment
```bash
# Submit to app stores
eas submit --platform ios
eas submit --platform android
```

## 📱 Usage

### Authentication
- Users sign up/login using AWS Cognito
- Email verification required
- Profile management available in settings

### Creating Study Sessions
1. Navigate to "Create Session"
2. Configure study parameters:
   - Group type (Family, Youth, Adult, etc.)
   - Number of questions
   - Verses per question
   - Focus topic
   - Bible version preference
3. AI generates relevant questions and verses
4. Save for future use or share with community

### Community Features
- Browse community-created studies
- Join group sessions
- Share your own study materials

## 🔧 Configuration Files

- **`app.json`**: Expo configuration and build settings
- **`eas.json`**: EAS Build profiles and deployment settings
- **`amplify/`**: AWS Amplify backend configuration
- **`tailwind.config.js`**: Styling configuration
- **`package.json`**: Dependencies and scripts

## 🧪 Testing

```bash
# Run tests
npm test

# Run linting
npm run lint
```

## 📚 Project Structure

```
bible-study-app/
├── app/                    # Main application code
│   ├── (tabs)/            # Tab-based navigation screens
│   ├── screens/           # Application screens
│   ├── components/        # Reusable components
│   ├── config/           # Configuration files
│   └── aws-exports.js    # AWS configuration
├── amplify/              # AWS Amplify backend
├── assets/               # Static assets
├── scripts/              # Utility scripts
└── docs/                 # Documentation
```

## 🔐 Security

- AWS Cognito handles user authentication
- API endpoints secured with AWS IAM
- Environment variables for sensitive data
- HTTPS enforcement for all API calls

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support & Documentation

- **Expo Documentation**: [https://docs.expo.dev/](https://docs.expo.dev/)
- **AWS Amplify Docs**: [https://docs.amplify.aws/](https://docs.amplify.aws/)
- **React Native Docs**: [https://reactnative.dev/docs/getting-started](https://reactnative.dev/docs/getting-started)
- **OpenAI API Docs**: [https://platform.openai.com/docs](https://platform.openai.com/docs)

## 🐛 Troubleshooting

### Common Issues

**Build Failures**
- Ensure all dependencies are installed: `npm install`
- Clear Expo cache: `expo start --clear`
- Verify AWS credentials: `amplify status`

**Authentication Issues**
- Check AWS Cognito configuration
- Verify `aws-exports.js` is up to date
- Run `amplify pull` to sync backend changes

**API Errors**
- Verify OpenAI API key in environment variables
- Check AWS Lambda function logs in CloudWatch
- Ensure proper IAM permissions

---

**Package**: `bible@1.0.0`  
**Expo Project ID**: `bf0f9ddf-57ea-41ec-8f48-aea2dfbb72a1`  
**Bundle ID**: `com.testbible.bible`
