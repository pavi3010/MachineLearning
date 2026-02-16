# Email Spam Detector

This project is a computer program that can automatically tell the difference between "Spam" (junk emails) and "Ham" (real emails).

## What does this project do?
I used two different mathematical methods (models) to see which one is better at catching spam:

- **Logistic Regression**: A method that calculates the probability of an email being spam.
- **Support Vector Machine (SVM)**: A method that tries to draw a clear boundary between spam and real emails.

## The Data
I used a famous dataset called Spambase. It contains thousands of examples of emails that have already been labeled as spam or real. Each email is described by numbers, like how often specific words (like "free" or "win") appear.

## 🛠️ How I built it
- **Cleaned the Data**: I made sure there were no missing pieces.
- **Standardized everything**: I scaled all the numbers so the computer could compare them fairly.
- **Tuning**: I tested different settings (kernels) for the SVM to see which shape of boundary worked best.
- **Testing**: I split the data to make sure the program could handle "new" emails it hadn't seen before.

## What I discovered
- **Logistic Regression is better**. It was right about 94% of the time. It was very reliable and didn't get confused easily.
- **SVM is also good**, especially when using a specific setting called "RBF," but it was slightly less accurate than Logistic Regression.
- Some settings (like Polynomial) didn't work well for this specific problem and missed a lot of spam.
