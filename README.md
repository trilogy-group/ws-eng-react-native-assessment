# Cross-platform Mobile Development: Real Work Assignment

## About this Assignment

In this assessment, you will design and implement a key feature of our "TeachTap" React Native application. We aim to gauge your expertise in creating user-friendly, robust, and efficient mobile applications, keeping in mind the expectations of today's dynamic user base. This repository contains the scaffolding for creating a React Native, Expo application for this assessment. For convenience, the icons required for this assessment are included in the `assets` folder.

## Assessment Steps

1. [Start the code in Gitpod](#running-in-gitpod), and take a look at [the feature requirements](#feature-for-you-section) and [the grading criteria](#evaluation-criteria) described below. 
   - Please do NOT fork this repository. You will share your code changes as a git diff at the end.
   - When writing code, make sure to be on the `rwa/cross-platform-mobile-v6` branch. Pull it regularly to ensure you have the latest changes from the remote.
2. Implement the feature described below, while following the quality bar listed below.
3. Record a demo video (maximum 1 minute) in which you show the acceptance test listed below. We recommend using [Loom](https://www.loom.com/) as it is free, easy to set up, and works on all platforms. 
4. [Submit your work](#submitting-your-work) by following the instructions below.

## Running in Gitpod

You can sign up for a free Gitpod account here: https://www.gitpod.io/ using your GitHub account. After you sign up, open the following link to launch a browser-based VSCode environment: https://www.gitpod.io/#https://github.com/trilogy-group/ws-eng-react-native-assessment/tree/rwa/cross-platform-mobile-v6 . You may refer to the [running in Gitpod](./GITPOD.md) doc for hints about using Gitpod.

This project can also be [run locally](./LOCAL.md); this will require up to 60 minutes of set-up time. We only recommend using this if you have technical impediments in using Gitpod.

Once Expo has spun up, it will display a QR code. Install the "Expo Go" app on your Android/iOS mobile device and scan the QR code to open your app. When you make changes, you can press "r" in the terminal to refresh the app on your device.

## Feature: For You Section

**Background**:

In the age of technology-driven education, platforms that merge entertainment with learning gain tremendous traction. TeachTap aims to be a pioneer in this space, offering users bite-sized educational content in an engaging format, reminiscent of TikTok. At the heart of the app's user experience is the "For You" section on the "Home" screen. This screen offers a seamless stream of fresh content at the fingertips of our users, encouraging continued exploration and engagement.

**Requirements**:

* Users should have a seamless experience when navigating and consuming content.
* The app must match our design, closely following the TikTok "formula".
* As a user, I want to get an endless stream of relevant multiple-choice questions, such that I can validate my knowledge in select areas.
* UX Design: [Figma prototype](https://www.figma.com/proto/yDodIJK3VIeO2Ax8V9RcNB/TeachTok-Assessment-(V2)?type=design&scaling=scale-down&page-id=0%3A1&node-id=1-3227&starting-point-node-id=1%3A3227).

**In scope**:

* Showing content for the "For you" section of the "Home" screen,
* Displaying the Multiple Choice Questions (MCQs) in this section,
* Revealing the correct answer when the user taps one choice of an MCQ,
* Showing the content’s author name (e.g., "AP US History"), playlist, avatar, and content description,
* Browsing through content in an infinite scroll fashion (like TikTok),
* Measuring the time the user spent in the app using a countdown timer at the top left.

**Not in scope**:

* Persisting state changes (e.g., the selected choice for MCQs) to an API,
* Clicking Like, Comment, Share, and Bookmark buttons (just show them as static icons),
* Clicking into User Profile, Search, or into the Playlist (just show as static icons/text),
* Any of the other sections of the app except Home (Discover, Activity, Bookmarks, Profile; just show some placeholder).

**API endpoints**:

* Retrieve MCQs: GET [https://cross-platform.rp.devfactory.com/for_you](https://cross-platform.rp.devfactory.com/for_you) \
Returns the next content item for the user’s For You section.
* Reveal answer: GET [https://cross-platform.rp.devfactory.com/reveal?id=X](https://cross-platform.rp.devfactory.com/reveal?id=X)  \
Reveals the correct answer for an MCQ question with id = X.

**Acceptance Test**:

* When you open the application,
* Then a counter which tracks the time spent in the app is visible and incremented periodically,
* When you press the Discover/Activity/Bookmarks/Profile icon,
* Then a placeholder is displayed,
* When you press the Home icon.
* Then a multiple-choice question is displayed together with playlist information and share, like, bookmark, and comment icons,
* When you scroll down,
* Then another MCQ is displayed,
* When you tap the correct answer,
* Then that answer is higlighted with green,
* When you scroll down,
* Then another MCQ is displayed,
* When you tap a wrong answer,
* Then that answer is higlighted with red,
* And the correct answer is higlighted with green.

## Submitting your Work

1. Record a demo video showing the acceptance test listed above.
1. Capture a single screenshot showing the application after "incorrect answer pressed" step and place it directly in the `submission` folder in your repository.
1. Do NOT create subfolders in the `submission` folder. Please add all of your files directly in the `submission` folder.
1. Run `yarn submit` and follow the instructions.

## Evaluation Criteria

Your submission will be evaluated based on the following quality bar.

* **Completeness**: Evaluate the functionality of the final code and its alignment with the desired output. High-quality submissions will include code that fully meets the functional requirements and evidence that the solution works as designed, provided through a demo video.
* **Consistency**: Asses adherence to the given UI/UX design and the overall user experience consistency. High-quality submissions will include a UI that closely follows the provided design and ensures a smooth and consistent user experience (e.g., scrolling is smooth and uninterrupted, and users can scroll back to content loaded previously in the same session and see their answers).
* **Technology**: Evaluate the adherence to the technical constraints (i.e., usage of React Native & TypeScript) and to the industry standards related to these technologies. High-quality submissions will use React Native and standard patterns for managing state, calling APIs, handling navigation, recovering from errors, etc.
* **Clean Code**: Gauge the code's cleanliness, efficiency, consistency, and adherence to best practices. High-quality submissions will respect clean coding standards, and SOLID/DRY principles, and will not include unused code and/or compilation errors/warnings.

