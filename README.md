# digi4school-pdf

Welcome to digi4school-pdf!
This script let's you download your books from digi4school.

## Requirements

1. [Node.JS](https://nodejs.org/en/) (test with `node --version`)
2. [NPM](https://nodejs.org/en/) (test with `npm --version`)
3. [Java 8+](https://www.java.com/en/download/) (test with `java --version`)

## Installation

1. Clone this repository using HTTPS or Git.
2. Run `npm install` in the root directory of the project.

## Usage

### Automatic Download (recommended)

1. Go to D4S, log-in and open the book you want to download.
2. Open the JavaScript console of your browser and run the following code:

```
console.log('hi');
```

3. Copy the output of the script.
4. Create a file called `.env` in the root directory of the project.
5. Paste the previously copied text in this file, save and close it.
6. Done! Move on to 'Start Downloading' to download your book.

### Manual Download

1. Create a file called `.env` in the root directory.
2. Create the following 4 keys in the `.env`-file:

```
BOOK_ID=
BOOK_PAGES=
BOOK_PDFSIZE_W=
BOOK_PDFSIZE_H=
COOKIE_SESSION=
COOKIE_DIGI4B=
COOKIE_DIGI4S=
```

The key `BOOK_NAME` is optional - this name will be used to generate the PDF-file.

1. Go to D4S, log-in and open the book you want to download.
2. In the URL bar, you can find the current book id, copy and paste it in the `.env`-file as `BOOK_ID`.
3. Click on the fast-forward button of the book-viewer and copy-paste the count of pages in the `.env`-file as `BOOK_PAGES`.
4. If the book doesn't seem to use the A4 format, you can specify `BOOK_PDFSIZE_W` and `BOOK_PDFSIZE_H` for each page.
5. Open the cookies tab of your browsers debug window and copy the values of the following cookies into the `.env` file:

   ```
   Value of 'ad_session_id' as 'COOKIE_SESSION'
   Value of 'digi4b' as 'COOKIE_DIGI4B'
   Value of 'digi4s' as 'COOKIE_DIGI4S'
   ```

6. Done!

## Start Downloading

After you've created and set up your `.env`-file, you can start downloading!
Open a new terminal window in the root directory of the project and execute `npm start`.

You should see the progress of the download in the console and if the PDF-file has been generated, you can use a file explorer to navigate into the subdirectory book/ to find your generated PDF-file.

Note: After the download has finished, the images under book/book_images aren't needed anymore. You can safely delete them.

## Disclaimer

This project is for educational purposes only and it's illegal to download and/or use the generated PDF-files.
