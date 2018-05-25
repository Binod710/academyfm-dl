# [academy.fm](https://academy.fm) Video Downloader


## REQUIREMENTS

- node +8
- [youtube-dl](https://rg3.github.io/youtube-dl/download.html)

### Install requirements
	yarn install

## USAGE

**Step1:** Edit `.env.example` and replace `YOUR_USERNAME_HERE` and `YOUR_PASSWORD_HERE` with your own.

**Step2:** Rename `.env.example` to `.env`.

**Step3:** Excute the command below.

	node spider.mjs

## OPTIONS

	--category		category name

	--slug			course/tutorial slug
			  	it'll be shown as its url.

	--course		download videos in a course with specific slug
				(you need this flag with --slug)
					  
	--tutorial		download videos in a tutorial with specific slug
				(you need this flag with --slug)

	--output		output directory where videos will be added
				e.g. ~/Desktop/academyfm

## EXAMPLES

Download all courses in academy.fm

	node spider.mjs

Download videos in a specific course

	node spider.mjs --slug ableton-live-10-essential-training --course

Download videos in a specific tutorial

	node spider.mjs --slug frequency-masking-izotope-neutron --tutorial

Download all courses in a specific category and put them to `~/Desktop/videos/ableton/*`

	node spider.mjs --category ableton --output ~/Desktop

## OUTPUT

Downloaded videos will be stored in
 `./videos/CATEGORY_NAME/COURSE_NAME/INDEX-LESSON_NAME.[ext]`

e.g. `./videos/ableton/ableton-live-10-essential-training/0001-Intro&Highlights.mp4`
