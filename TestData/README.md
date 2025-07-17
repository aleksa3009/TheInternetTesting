# Test Data Description

This folder contains test files used in the project for various types of testing.

| File Name           | Type       | Purpose                                  |
|---------------------|------------|------------------------------------------|
| small.txt           | valid      | Positive test                           |
| image.jpg           | valid      | Test image upload                       |
| sample.pdf          | valid      | Verification of non-text file upload   |
| 5MB.zip             | boundary   | Valid size limit file                   |
| 6MB.zip             | negative   | Exceeds size limit   |
| 10MB.zip            | negative   | Exceeds size limit   |
| dangerous.exe       | negative   | Test antivirus / unsafe file extension |
| čćžšđ!.txt          | edge case  | Test special characters in file name   |
| aaa...a.txt         | edge case  | Test extreme length of file name        |
