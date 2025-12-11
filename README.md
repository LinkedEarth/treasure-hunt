# 🏴‍☠️ Treasure Hunt Website

A mysterious interactive treasure hunt website designed for conferences or events. Participants must answer riddles correctly to reveal the URL of the next page!

## 🎯 How It Works

This treasure hunt features **interactive answer validation**:

1. Landing page provides a "Begin Your Quest" button to start
2. Each clue page presents a riddle and a question
3. Participants enter their answer in a text box
4. If correct, the next page's filename is revealed
5. They navigate to that page by typing it into their browser
6. Wrong answers provide helpful hints to guide them

**The Journey:**
- **index.html** - Introduction and start button
- **Clue 1 (meridian.html)** - Answer "compass" → reveals compass.html
- **Clue 2 (compass.html)** - Answer "anchor" → reveals anchor.html  
- **Clue 3 (anchor.html)** - Final treasure reveal!

## ✨ Interactive Features

- **Real-time answer checking** - JavaScript validates answers instantly
- **Multiple answer formats** - Accepts "compass", "a compass", "the compass"
- **Enter key support** - Press Enter to submit answers
- **Error messages** - Helpful feedback for incorrect answers
- **Hint system** - Expandable hints if participants get stuck
- **Visual feedback** - Success animations when answers are correct

## 🗺️ Pages

- **index.html** - Landing page that introduces the treasure hunt
- **meridian.html** - First clue page
- **compass.html** - Second clue page
- **anchor.html** - Final clue page with treasure reveal

## 🚀 Quick Setup with GitHub Pages

### 1. Create a New Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right and select "New repository"
3. Name your repository (e.g., `treasure-hunt`)
4. Choose "Public" (required for free GitHub Pages)
5. Click "Create repository"

### 2. Upload Your Files

**Option A: Using GitHub Web Interface**

1. On your new repository page, click "uploading an existing file"
2. Drag and drop all files from this folder:
   - `index.html`
   - `meridian.html`
   - `compass.html`
   - `anchor.html`
   - `styles.css`
   - `README.md`
3. Click "Commit changes"

**Option B: Using Git Command Line**

```bash
# Navigate to this folder in your terminal
cd /path/to/treasure-hunt-folder

# Initialize git repository
git init

# Add your remote repository
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Add all files
git add .

# Commit the files
git commit -m "Initial commit: Treasure hunt website"

# Push to GitHub
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" (top right of repository page)
3. Click "Pages" in the left sidebar
4. Under "Source", select "Deploy from a branch"
5. Under "Branch", select `main` and `/ (root)`
6. Click "Save"

### 4. Access Your Website

After a few minutes, your site will be live at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

For example: `https://johndoe.github.io/treasure-hunt/`

## 🎨 Customization

### Change the Questions and Answers

Each clue page has a riddle and question. To customize:

1. **Edit the riddle** - Change the poem/verse in the `riddle-line` sections
2. **Edit the question** - Modify the text in `riddle-question` class
3. **Change the answer** - Update the JavaScript `correctAnswers` array:
   ```javascript
   const correctAnswers = ['compass', 'a compass', 'the compass'];
   ```
4. **Update the revealed page** - Change the filename shown when correct:
   ```html
   <p class="next-page-name"><strong>compass.html</strong></p>
   ```

### Modify the Treasure

In `anchor.html`, update the treasure reveal section:
- Change the treasure name in `<p class="treasure-name">`
- Replace the emoji in `<div class="treasure-chest">`
- Customize the congratulations message

### Make It Harder

**Option 1: Obscure Filenames**
- Rename pages to make them harder to guess
- Example: `compass.html` → `navigator.html` or `direction.html`
- Update all links and revealed filenames accordingly

**Option 2: More Complex Questions**
- Make riddles more cryptic
- Require multi-step reasoning
- Add red herrings in the poetry

**Option 3: Case-Sensitive or Exact Matching**
In the JavaScript, change:
```javascript
const input = document.getElementById('answer-input').value.trim().toLowerCase();
```
To:
```javascript
const input = document.getElementById('answer-input').value.trim(); // case-sensitive!
```

### Adjust Colors

Edit `styles.css` and modify the CSS variables at the top:
```css
:root {
    --parchment: #f4e8d0;
    --ink-dark: #2c1810;
    --gold: #d4af37;
    /* etc. */
}
```

## 📱 Features

- **Interactive Answer Validation** - JavaScript checks answers in real-time
- **Smart Input Handling** - Accepts multiple answer formats, case-insensitive
- **Visual Feedback** - Error messages and success animations
- **Keyboard Support** - Press Enter to submit answers
- **Responsive Design** - Works on desktop, tablet, and mobile
- **Vintage Aesthetic** - Aged parchment with maritime theme
- **Smooth Animations** - Fade-ins, slides, and hover effects
- **Hint System** - Expandable hints for each clue
- **Conference Ready** - Share a single URL to get started

## 🛠️ Technologies

- Pure HTML5
- CSS3 with custom animations
- Vanilla JavaScript for answer validation
- Google Fonts (Cinzel + Crimson Text)
- No frameworks or dependencies required!

## 📝 License

Feel free to use and modify this treasure hunt for your own purposes!

## 🎯 Tips for Your Treasure Hunt

### For Conference Distribution

**How to Share:**
1. **Simple Start** - Just share the base URL (e.g., `yoursite.github.io/treasure-hunt`)
2. **QR Code** - Generate a QR code for the landing page
3. **Email/Slack** - Send the link to attendees
4. **Booth/Signage** - Display the URL on conference materials

**The Flow:**
- Participants visit the URL and click "Begin Your Quest"
- They answer each riddle to reveal the next page
- No need for physical clue distribution - it's all in the website!
- Track completion by seeing who reaches the final treasure page

**Making It More Challenging:**
- Use obscure page names instead of "meridian/compass/anchor"
- Make questions require domain knowledge from your conference
- Create riddles that reference conference locations or sessions
- Add more clue pages (copy and modify existing ones)
- Require case-sensitive answers or exact phrasing

**For Physical/Hybrid Hunts:**
- Print the starting URL with a QR code
- Hide QR codes around the venue that link to different pages
- Require finding physical objects before being able to answer
- Combine digital riddles with real-world scavenger hunt elements

### General Tips

- **Difficulty**: Adjust riddle complexity based on your audience
- **Hints**: The expandable hints help without giving away the answer
- **Testing**: Try it with a friend before the conference
- **Prizes**: Offer rewards for the first completers or everyone who finishes
- **Analytics**: Use Google Analytics or similar to track page visits

Happy treasure hunting! 🏴‍☠️💎
