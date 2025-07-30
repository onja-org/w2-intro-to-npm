# NPM Practice Exercises - 30 Minutes (Hands-On)

## 🎯 Welcome to Practice Time!

You just spent 30 minutes learning about npm theory. Now it's time to **put it into action**!

**Remember from the lesson:**
- Don't worry about what Express, Moment, or Jest actually do
- Focus on mastering the npm commands
- You're learning the toolbox, not every individual tool

---

## 📋 What You'll Build Today

By the end, you'll have:
- ✅ A complete Node.js project with package.json
- ✅ Installed packages (dependencies and dev dependencies)
- ✅ Custom scripts that actually work
- ✅ Experience with version control and .gitignore
- ✅ Hands-on practice with package management

---

## 🚀 Exercise 1: Project Foundation *(5 minutes)*


### Step 1: Initialize Your Project
```bash
npm init -y
```

**🔍 Check Your Work:**
- Look in your folder - you should see a `package.json` file
- Open `package.json` and look at the content
- Notice the default values npm created for you

**💡 What happened:** npm created your project's "ID card" with default settings.

### Step 2: Create Project Structure
```bash
mkdir src
touch app.js
```

**What you just did:** Created a `src` folder and an empty `app.js` file (your main application file).

---

## 📦 Exercise 2: Installing Dependencies *(10 minutes)*

### Step 3: Install Your First Package (Express)
```bash
npm install express
```

**🔍 Check Your Work:**
1. Open `package.json` - look for a new `"dependencies"` section
2. Notice the `node_modules` folder appeared
3. Notice the `package-lock.json` file appeared

**💡 What happened:** 
- Express was downloaded to `node_modules`
- Your `package.json` now "remembers" you need Express
- `package-lock.json` recorded the exact version details

### Step 4: Install Another Package (Moment)
```bash
npm install moment
```

**🔍 Check Your Work:**
- Look at `package.json` again - moment should be added to dependencies
- Both express and moment should be listed

### Step 5: Install Development Dependencies
```bash
npm install --save-dev jest
npm install --save-dev nodemon
```

**🔍 Check Your Work:**
- Open `package.json`
- You should now see TWO sections:
  - `"dependencies"` (express, moment)
  - `"devDependencies"` (jest, nodemon)

**💡 Remember:** Dependencies = needed by users, DevDependencies = needed only by developers

### Step 6: Version Control Setup
Create a `.gitignore` file:

```bash
touch .gitignore
```

Open `.gitignore` and add this line:
```
/node_modules
```

**💡 Why:** We don't want to save the huge `node_modules` folder in version control - it can be recreated anytime.

---

## ⚙️ Exercise 3: Creating Useful Scripts *(8 minutes)*

### Step 7: Add Basic Scripts
Open your `package.json` file and replace the `"scripts"` section with this:

```json
"scripts": {
  "start": "node app.js",
  "dev": "nodemon app.js",
  "test": "jest",
  "hello": "echo 'Hello from npm script!'"
}
```

**💡 What each script does:**
- `start`: Runs your app normally
- `dev`: Runs your app with auto-restart (using nodemon)
- `test`: Runs your tests (using jest)
- `hello`: Just says hello (custom script example)

### Step 8: Test Your Scripts
Try running each script:

```bash
npm run hello
```

**🔍 Expected result:** Should print "Hello from npm script!"

```bash
npm start
```

**🔍 Expected result:** Will try to run `app.js` (might give an error since it's empty - that's okay!)

### Step 9: Create a Simple App File
Add some content to `app.js`:

```javascript
console.log('My npm project is working!');
console.log('Express version:', require('express/package.json').version);
console.log('Current time:', new Date().toString());
```

Now test your start script again:
```bash
npm start
```

**🔍 Expected result:** Should print your messages and show the Express version.

---

## 🔧 Exercise 4: Package Management Practice *(5 minutes)*

### Step 10: Check What You've Installed
```bash
npm list --depth=0
```

**🔍 Check Your Work:** Should show your installed packages in a tree format.

### Step 11: Experiment with Versions
Install a specific version of a package:

```bash
npm install lodash@4.17.20
```

**🔍 Check Your Work:** 
- Look at `package.json` - lodash should appear with version `4.17.20`
- Notice it's an exact version (no `^` symbol)

### Step 12: Update to Latest Version
```bash
npm install lodash@latest
```

**🔍 Check Your Work:** The lodash version in `package.json` should have changed to the latest version.

### Step 13: Remove a Package
```bash
npm uninstall lodash
```

**🔍 Check Your Work:** Lodash should disappear from your `package.json`.

---

## 🧪 Exercise 5: Advanced Scripts & Testing *(2 minutes)*

### Step 14: Add More Useful Scripts
Update your `package.json` scripts section:

```json
"scripts": {
  "start": "node app.js",
  "dev": "nodemon app.js",
  "test": "jest",
  "hello": "echo 'Hello from npm script!'",
  "clean": "rm -rf dist/",
  "list": "npm list --depth=0",
  "info": "npm info express"
}
```

### Step 15: Test Your New Scripts
```bash
npm run list
```

**🔍 Expected result:** Shows all your installed packages.

```bash
npm run info
```

**🔍 Expected result:** Shows detailed information about the Express package.

---

## ✅ Final Verification *(Mini Quiz - No time limit)*

**Check that you've successfully completed everything:**

1. **Project Structure Check:**
   - [ ] `package.json` exists
   - [ ] `node_modules` folder exists  
   - [ ] `package-lock.json` exists
   - [ ] `.gitignore` exists with `/node_modules`
   - [ ] `app.js` exists

2. **Dependencies Check:**
   - [ ] Express is in `"dependencies"`
   - [ ] Moment is in `"dependencies"`
   - [ ] Jest is in `"devDependencies"`
   - [ ] Nodemon is in `"devDependencies"`

3. **Scripts Check:**
   - [ ] `npm start` runs without major errors
   - [ ] `npm run hello` prints a message
   - [ ] `npm run list` shows your packages

4. **Commands Mastered:**
   - [ ] You know how to install packages: `npm install package-name`
   - [ ] You know how to install dev dependencies: `npm install --save-dev package-name`
   - [ ] You know how to uninstall packages: `npm uninstall package-name`
   - [ ] You know how to run scripts: `npm run script-name`

---

## 🎉 Congratulations!

**You did it!** In just 30 minutes of practice, you:

✅ **Created** a complete npm project from scratch  
✅ **Installed** both regular and development dependencies  
✅ **Managed** package versions  
✅ **Created** custom scripts that work  
✅ **Set up** proper version control with .gitignore  
✅ **Practiced** all the essential npm commands  

## 🚀 What's Next?

Now that you've mastered npm basics, you're ready to:
- **Learn what Express actually does** (building web servers)
- **Learn what Moment actually does** (handling dates and times)  
- **Build real applications** using the packages you can now manage
- **Explore more packages** on [npmjs.com](https://npmjs.com)

## 💡 Quick Reference for Future Projects

**Essential commands you now know:**
```bash
# Project setup
npm init -y

# Installing packages  
npm install package-name              # Regular dependency
npm install --save-dev package-name   # Dev dependency

# Running scripts
npm start                            # Special script
npm run script-name                  # Any custom script

# Package management
npm list --depth=0                   # See installed packages
npm uninstall package-name           # Remove package
npm install package-name@latest      # Get latest version
```

**Remember:** You're now equipped with the fundamental skills every Node.js developer uses daily!