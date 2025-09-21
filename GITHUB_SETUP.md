# GitHub Repository Setup Instructions

Follow these steps to publish the legal documents repository on GitHub with GitHub Pages:

## 1. Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Repository settings:
   - **Repository name**: `subscription-manager-legal`
   - **Description**: "Legal documents for Subscription Manager iOS app"
   - **Public**: Yes (required for GitHub Pages)
   - **Initialize README**: No (we already have one)
   - **Add .gitignore**: No
   - **Choose a license**: No (we'll add later if needed)
5. Click "Create repository"

## 2. Push Local Repository to GitHub

After creating the repository, run these commands in Terminal:

```bash
cd /Users/gordon/Documents/subscription-manager-legal

# Add the remote repository
git remote add origin https://github.com/YOUR_USERNAME/subscription-manager-legal.git

# Push the code
git branch -M main
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

## 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" section in the left sidebar
4. Under "Source", select:
   - **Source**: Deploy from a branch
   - **Branch**: main
   - **Folder**: / (root)
5. Click "Save"
6. Wait a few minutes for the site to deploy

## 4. Access Your Legal Documents

Once deployed, your documents will be available at:

- **Main page**: `https://YOUR_USERNAME.github.io/subscription-manager-legal/`
- **Privacy Policy**: `https://YOUR_USERNAME.github.io/subscription-manager-legal/PRIVACY_POLICY`
- **Terms of Service**: `https://YOUR_USERNAME.github.io/subscription-manager-legal/TERMS_OF_SERVICE`

## 5. Update the iOS App

Once your GitHub Pages site is live, update the URLs in your iOS app:

1. Open `/Users/gordon/Documents/subscription-manager/ios/Sources/SubscriptionManagerUI/Views/SettingsView.swift`
2. Replace the placeholder URLs with your actual GitHub Pages URLs
3. Rebuild and test the app

## 6. Custom Domain (Optional)

If you want to use a custom domain like `legal.subscriptionmanager.app`:

1. In repository Settings > Pages
2. Under "Custom domain", enter your domain
3. Click "Save"
4. Add a CNAME record in your DNS settings pointing to `YOUR_USERNAME.github.io`

## 7. Keep Documents Updated

To update the legal documents:

```bash
cd /Users/gordon/Documents/subscription-manager-legal

# Make your changes to the .md files
git add -A
git commit -m "Update privacy policy / terms of service"
git push
```

Changes will automatically deploy to GitHub Pages within a few minutes.

## Repository Structure

```
subscription-manager-legal/
├── README.md              # Repository overview
├── index.html            # Landing page for GitHub Pages
├── PRIVACY_POLICY.md     # Privacy policy document
├── TERMS_OF_SERVICE.md   # Terms of service document
└── GITHUB_SETUP.md       # This setup guide
```

## Important Notes

- Keep the repository PUBLIC for GitHub Pages to work
- The documents are written in Markdown for easy editing
- The index.html provides a professional landing page
- Updates are automatically deployed when pushed to main branch
- Consider adding a CNAME file if using a custom domain

## Professional Touch

The legal documents are written to be:
- **Comprehensive**: Covering all major legal requirements
- **Global**: Includes GDPR (EU) and CCPA (California) compliance
- **User-friendly**: Clear language, well-organized sections
- **Professional**: Suitable for a global brand
- **Mobile-optimized**: The HTML page works well on all devices

## Support

For any questions about the legal documents or setup:
- Email: legal@subscriptionmanager.app
- GitHub Issues: Create an issue in the repository