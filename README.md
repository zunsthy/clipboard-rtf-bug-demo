# `ClipboardData.getData('text/rtf')` bug


## Introduction

Paste selection from Office Word to web page, and JS `ClipboardEvent` will be triggered. If the selection contains "Heading" styles, like "Heading 1", "Heading 2", etc, `ClipboardEvent` rtf data will be empty.

## Reproduce

### Step1

Create Word document and type line1 and line2.

![Step1](pics/step1.png)

### Step2

Apply line2 with 'Heading 1' style.

![Step2](pics/step2.png)

### Step3

Copy all docuemnt content.

![Step3](pics/step3.png)

### Step4

Paste to [the demo page](https://zunsthy.github.io/clipboard-rtf-bug-demo).

![Step4](pics/step4.png)

## Result

It print "Empty Content", but expect RTF text.

![Result](pics/bug_result.png)
