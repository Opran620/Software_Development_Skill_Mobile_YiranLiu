**Piano Trainer 🎹**

Piano Trainer is an Android app designed to help piano learners practice more efficiently, track their progress, and explore interactive tools like a virtual piano and metronome. It combines structured practice sessions, statistics tracking, and learning resources in a single mobile app.

**🧠 Project Concept**

The idea behind Piano Trainer is to provide a digital companion for piano learners. Practicing an instrument requires discipline, repetition, and monitoring progress. Many beginners struggle to maintain consistent practice and track improvement. This app solves these problems by:

	Providing a practice timer with automatic record saving.

	Logging practice sessions and calculating statistics (total time and unique pieces).

	Offering interactive tools like a virtual piano and metronome.

	Including learning resources, such as curated finger tutorials.

The app is lightweight, intuitive, and designed to make practice sessions both productive and enjoyable. Users can add their own sheet music, resume previous sessions, and see their improvement over time.

**📦 Features**

Practice Menu

	Select existing pieces or add new ones.

	Start timed practice sessions.

	Resume recent sessions easily.
**	Practice Sub-Menu**

The Practice sub-menu is designed to organize all the practice-related functionality in one place, improving workflow and user experience. It serves as a gateway to the core practice features, including:

	Add Piece

		Allows the user to add new sheet music or select from existing pieces.

		Users can search and filter the list for quick selection.

	Start Practice

		Opens the practice session activity for the selected piece.

		Displays the sheet music and starts a timer.

	View Statistics

		Opens a summary of practice history: total time spent, number of unique pieces, and recent sessions.

	Recent Practice

		Shows the most recent practice sessions for quick access.

		Clicking a recent session opens that piece in a new practice session.

	Back Button

		Returns to the main menu.

This submenu ensures all practice functions are grouped logically, making navigation smooth and consistent.


**Virtual Piano**

	Play notes using on-screen buttons.

	Simulates real piano keys for practice without a physical instrument.

**Metronome**

	Choose time signatures (4/4, 3/4, 2/4).

	Play click sounds to maintain rhythm.

**Statistics & Progress Tracking**

	View total practice time.

	See the number of unique pieces practiced.

	Maintain a history of recent sessions.

**Finger Tutorial**

	Links to curated YouTube videos to improve piano technique.

**🛠 Installation & Running**


	Open the project in Android Studio.

	Sync Gradle and ensure your minSdkVersion matches your device (default 21+).

	Place any additional sheet music images in res/drawable/.

	Build and run the app on a physical device or emulator.

**🎥 Demo Video**

	Watch a live demo of the app in action: https://drive.google.com/file/d/1sjvpM3D4mGx1Y1Bb80qpOPmcrOv1P27s/view?usp=sharing


**💡 Future Improvements**

	Implement customizable practice schedules and reminders.

	Add multi-octave virtual piano keys.

	Include difficulty levels for pieces and exercises.

	Add offline tutorial videos to reduce internet dependency.

**📂 Project Structure**

	MainActivity.kt: Main menu navigation.

	PracticeMenuActivity.kt: Submenu for practice-related features.

	PracticeActivity.kt: Handles timed practice sessions and sheet music display.

	VirtualPianoActivity.kt: Interactive on-screen piano.

	MetronomeActivity.kt: Time signature and click playback.

	FingerTutorialActivity.kt: Opens online piano tutorial videos.

	DataManager.kt: Saves and retrieves practice records locally.
	
**Key Methods & Functions**

Below are the main methods used in the app and their purpose:

	PracticeActivity

		startPractice()
		Starts the practice timer and disables the Start button while enabling the Stop button.

		stopPractice()
		Stops the timer, calculates elapsed minutes, saves a practice record using DataManager, and re-enables the Start button.

		updateTimer (Runnable)
		Updates the on-screen timer every second while a session is running.

		updateScoreImage()
		Loads the sheet music image for the selected piece. If the image is missing, a default placeholder is displayed.

	DataManager

		savePracticeRecord(ctx, record)
		Saves a practice session (piece name, timestamp, duration) locally using SharedPreferences.

		getPracticeRecords(ctx)
		Retrieves all saved practice sessions and converts them into a list of PracticeRecord objects.

		saveLastPiece(ctx, name) / getLastPiece(ctx)
		Stores and retrieves the most recently practiced piece.

	PracticeMenuActivity

		btnAddPiece.setOnClickListener
		Navigates to AddPieceActivity to select or add a new piece.

		btnStartPractice.setOnClickListener
		Opens PracticeActivity to start a practice session for the chosen piece.

		btnStats.setOnClickListener / btnRecent.setOnClickListener
		Opens StatsActivity or RecentActivity respectively to view user statistics or recent practice sessions.

**The details for code is explained in the Annotation.
Thank you for your reading.**

Yiran Liu
28.9.2025
