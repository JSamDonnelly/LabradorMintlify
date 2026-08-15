# Source: https://www.testwithlabrador.com/Labrador_VPAT.docx

# Labrador Accessibility Conformance Report

# WCAG Edition

**(Based on VPAT® Version 2.5)**

## Name of Product:

Labrador website ([https://www.testwithlabrador.com/](https://www.testwithlabrador.com/))

## Report Date:

December 11th, 2025

## Product Description:

A web app for manual accessibility testing workflows.

## Contact information:

[sam@testwithlabrador.com](mailto:sam@testwithlabrador.com)

## Evaluation Methods Used:

Accessibility testing as per WCAG 2.2 AA guidelines.

The evaluation was performed using below tools/ tests:

- Screen readers:
 - NVDA on Win11/ Chrome
 - VoiceOver on iPhone/ Safari
- WAVE automated tool
- Color contrast testing using Color Contrast Analyzer
- Browser zoom
- Keyboard-only
- Text-spacing testing using bookmarklets

## Notes:

The VPAT has been prepared based on the accessibility evaluation of the following pages/ flows:

| [https://www.testwithlabrador.com/login](https://www.testwithlabrador.com/login) |
| --- |
| [https://www.testwithlabrador.com/forgot-password](https://www.testwithlabrador.com/forgot-password) |
| [https://www.testwithlabrador.com/beta-signup](https://www.testwithlabrador.com/beta-signup) |
| [https://www.testwithlabrador.com/projects](https://www.testwithlabrador.com/projects) |
| [https://www.testwithlabrador.com/projects/1092](https://www.testwithlabrador.com/projects/1092) |
| [https://www.testwithlabrador.com/projects/1092/pages/1103/overview](https://www.testwithlabrador.com/projects/1092/pages/1103/overview) |
| [https://www.testwithlabrador.com/projects/1092/pages/1103/audit?criterion=1.1.1](https://www.testwithlabrador.com/projects/1092/pages/1103/audit?criterion=1.1.1) |
| [https://www.testwithlabrador.com/billing](https://www.testwithlabrador.com/billing) |
| [https://www.testwithlabrador.com/notifications](https://www.testwithlabrador.com/notifications) |

## Applicable Standards/Guidelines

This report covers the degree of conformance for the following accessibility standards/guidelines:

| 
## Standard/Guideline

 | 

## Included in Report

 |
| --- | --- |
| Web Content Accessibility Guidelines 2.2 at [_https://www.w3.org/TR/WCAG22/_](https://www.w3.org/TR/WCAG22/) | Level A (Yes)<br>Level AA (Yes)<br>Level AAA (No) |

## Terms

The terms used in the Conformance Level information are defined as follows:

- **Supports**: The functionality of the product has at least one method that meets the criterion without known defects or meets with equivalent facilitation.
- **Partially Supports**: Some functionality of the product does not meet the criterion.
- **Does Not Support**: The majority of product functionality does not meet the criterion.
- **Not Applicable**: The criterion is not relevant to the product.
- **Not Evaluated**: The product has not been evaluated against the criterion.

## WCAG 2.x Report

Note: When reporting on conformance with the WCAG 2.x Success Criteria, they are scoped for full pages, complete processes, and accessibility-supported ways of using technology as documented in the [WCAG 2.0 Conformance Requirements](https://www.w3.org/TR/WCAG20/#conformance-reqs).

### **Table 1: Success Criteria, Level A**

| **Criteria** | **Conformance Level** | **Remarks and Explanations** |
| --- | --- | --- |
| [**1.1.1 Non-text Content**](http://www.w3.org/TR/WCAG20/#text-equiv-all)<br>(Level A) | Supports | All images on the website contain<br>relevant alternative text. |
| [**1.2.1 Audio-only and Video-only (Prerecorded)**](http://www.w3.org/TR/WCAG20/#media-equiv-av-only-alt) (Level A) | Not Applicable | No audio-only or video-only content is present on the website. |
| [**1.2.2 Captions (Prerecorded)**](http://www.w3.org/TR/WCAG20/#media-equiv-captions) (Level A) | Not Applicable | No multimedia content is present on the website. |
| [**1.2.3 Audio Description or Media Alternative (Prerecorded)**](http://www.w3.org/TR/WCAG20/#media-equiv-audio-desc) (Level A) | Not Applicable | No multimedia content is present on the website. |
| [**1.3.1 Info and Relationships**](http://www.w3.org/TR/WCAG20/#content-structure-separation-programmatic) (Level A) | Partially Supports | The website has consistent headers and global heading and list structures to establish clear information and relationships within most parts of the website. Screen readers properly identify most of the information available on the website. Visually impaired users are easily able to perceive the relationships between a particular element and its role.<br>**Exceptions include:**
- The screen reader announces unnecessary information like 'Start recording Intercom' while navigating through the chatbot

<br>\[This is specific to a third-party plugin: Intercom app\]. |
| [**1.3.2 Meaningful Sequence**](http://www.w3.org/TR/WCAG20/#content-structure-separation-sequence) (Level A) | Supports | The sequence of the content present on the website is meaningful and appropriate, and does not affect the meaning of the provided content. |
| [**1.3.3 Sensory Characteristics**](http://www.w3.org/TR/WCAG20/#content-structure-separation-understanding) (Level A) | Supports | No information is present on the website, which is based on sensory characteristics such as shape, size, location, sound, etc. |
| [**1.4.1 Use of Color**](http://www.w3.org/TR/WCAG20/#visual-audio-contrast-without-color) (Level A) | Supports | Color is not used as the only visual means of conveying most of the information, indicating an action, prompting a response, or distinguishing a visual element. |
| [**1.4.2 Audio Control**](http://www.w3.org/TR/WCAG20/#visual-audio-contrast-dis-audio) (Level A) | Not Applicable | No audio content is present on the website that plays automatically for more than 3 seconds. |
| [**2.1.1 Keyboard**](http://www.w3.org/TR/WCAG20/#keyboard-operation-keyboard-operable) (Level A) | Supports | Elements of the website support standard keyboard navigation and input functions (including swiping to move between input fields and pressing \[Double tap\] to make selections). |
| [**2.1.2 No Keyboard Trap**](http://www.w3.org/TR/WCAG20/#keyboard-operation-trapping)<br>(Level A) | Supports | Keyboard focus is moving sequentially throughout the website without the focus getting trapped in any section and it is convenient to access the functionality. |
| [**2.1.4 Character Key Shortcuts**](https://www.w3.org/TR/WCAG21/#character-key-shortcuts) (Level A 2.1 and 2.2) | Not Applicable | No functionalities are dependent on or controlled by character key shortcuts. |
| [**2.2.1 Timing Adjustable**](http://www.w3.org/TR/WCAG20/#time-limits-required-behaviors)<br>(Level A) | Not Applicable | There is no such activity present on the website where time needs to be adjusted or extended. |
| [**2.2.2 Pause, Stop, Hide**](http://www.w3.org/TR/WCAG20/#time-limits-pause)<br>(Level A) | Not Applicable | There is no auto moving/ scrolling content is available on the website. |
| [**2.3.1 Three Flashes or Below Threshold**](http://www.w3.org/TR/WCAG20/#seizure-does-not-violate) (Level A) | Not Applicable | There is no flashing content present on the website. |
| [**2.4.1 Bypass Blocks**](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-skip)<br>(Level A) | Supports | A bypass mechanism for skipping to the main content is implemented. |
| [**2.4.2 Page Titled**](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-title) (Level A) | Supports | Descriptive and accurate page titles are present for all pages on the website. |
| [**2.4.3 Focus Order**](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-focus-order) (Level A) | Partially Supports | The focus moves in a correct sequence order for most elements on the website from left to right and top to bottom.<br>**Exceptions include:**

- The focus does not get trapped inside the 'Chatbot' modal and moves to background elements using keyboard.

<br>\[This is specific to a third-party plugin: Intercom app\]. |
| [**2.4.4 Link Purpose (In Context)**](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-refs) (Level A) | Supports | All links are provided with appropriate link text and the user would be able to understand the purpose of the link from its link text. |
| [**2.5.1 Pointer Gestures**](https://www.w3.org/TR/WCAG21/#pointer-gestures) (Level A 2.1 and 2.2) | Not Applicable | The success criterion is not applicable. |
| [**2.5.2 Pointer Cancellation**](https://www.w3.org/TR/WCAG21/#pointer-cancellation) (Level A 2.1 and 2.2) | Supports | No down-event of the pointer is used in the website to execute any part of the action. |
| [**2.5.3 Label in Name**](https://www.w3.org/TR/WCAG21/#label-in-name) (Level A 2.1 and 2.2) | Supports | Labels on the website include text and the same text is defined in the code as well to assist speech recognition technologies. |
| [**2.5.4 Motion Actuation**](https://www.w3.org/TR/WCAG21/#motion-actuation) (Level A 2.1 and 2.2) | Not Applicable | No functionality is present on the website that is operable only by device motion. |
| [**3.1.1 Language of Page**](http://www.w3.org/TR/WCAG20/#meaning-doc-lang-id) (Level A) | Supports | The language attribute is correctly defined for the webpages. |
| [**3.2.1 On Focus**](http://www.w3.org/TR/WCAG20/#consistent-behavior-receive-focus) (Level A) | Supports | No interactive element is triggered automatically on receiving the focus. |
| [**3.2.2 On Input**](http://www.w3.org/TR/WCAG20/#consistent-behavior-unpredictable-change) (Level A) | Supports | Change of context does not happen when the user changes the setting of any input controls. |
| [**3.2.6 Consistent Help**](https://www.w3.org/TR/WCAG22/#consistent-help) (Level A 2.2 only) | Supports | A sufficient help mechanism is provided in a consistent place on multiple webpages. |
| [**3.3.1 Error Identification**](http://www.w3.org/TR/WCAG20/#minimize-error-identified) (Level A) | Supports | Errors present on the website are notified to the users correctly. |
| [**3.3.2 Labels or Instructions**](http://www.w3.org/TR/WCAG20/#minimize-error-cues) (Level A) | Supports | The website provides support for motor-impaired and cognitive users, as most of the labels and instructions are provided for the form fields, which are clearly visible and readable to such users. |
| [**3.3.7 Redundant Entry**](https://www.w3.org/TR/WCAG22/#redundant-entry) (Level A 2.2 only) | Not Applicable | No such user input is required on the website. |
| [**4.1.2 Name, Role, Value**](http://www.w3.org/TR/WCAG20/#ensure-compat-rsv)<br>(Level A) | Partially Supports | Most of the website elements have a proper label associated with their role and the screen reader is recognizing them correctly with updated values as well.<br>**Exceptions include:**

- Role and Label not announced for the 'Intercom Messenger' Dialog.
- The screen reader does not announce the state as 'Expanded' when the 'Emoji Picker' button is triggered.

<br>\[This is specific to a third-party plugin: Intercom app\] |

### **Table 2: Success Criteria, Level AA**

| **Criteria** | **Conformance Level** | **Remarks and Explanations** |
| --- | --- | --- |
| [**1.2.4 Captions (Live)**](http://www.w3.org/TR/WCAG20/#media-equiv-real-time-captions)<br>(Level AA) | Not Applicable | No live multimedia content is present on the website. |
| [**1.2.5 Audio Description (Prerecorded)**](http://www.w3.org/TR/WCAG20/#media-equiv-audio-desc-only) (Level AA) | Not Applicable | Audio description is not required for the multimedia content present on the website. |
| [**1.3.4 Orientation**](https://www.w3.org/TR/WCAG21/#orientation)<br>(Level AA 2.1 and 2.2) | Supports | The website does not restrict its view and operation to a single display orientation. |
| [**1.3.5 Identify Input Purpose**](https://www.w3.org/TR/WCAG21/#identify-input-purpose) (Level AA 2.1 and 2.2) | Supports | Interactive fields on the website are clearly labeled to direct the user to enter the data expected in the fields. |
| [**1.4.3 Contrast (Minimum)**](http://www.w3.org/TR/WCAG20/#visual-audio-contrast-contrast) (Level AA) | Supports | The website adheres to minimum<br>contrast standards. |
| [**1.4.4 Resize text**](http://www.w3.org/TR/WCAG20/#visual-audio-contrast-scale) (Level AA) | Supports | The website is fully responsive. At a zoom of 200%, no loss of content or functionality is observed. |
| [**1.4.5 Images of Text**](http://www.w3.org/TR/WCAG20/#visual-audio-contrast-text-presentation)<br>(Level AA) | Supports | No information is conveyed to the<br>user via an image of the text. |
| [**1.4.10 Reflow**](https://www.w3.org/TR/WCAG21/#reflow)<br>(Level AA 2.1 and 2.2) | Partially Supports | The website does not require scrolling in two dimensions to present content without loss of information in 400% zoom.<br>**Exceptions include:**
- The 'Minimize' icon disappears on the viewport of 320px X 256px
- The placeholder like 'Search emoji' in 'Chatbot' modal disappears on the 400% enlarged view of 1280 X 1024.

<br>\[This is specific to a third-party plugin: Intercom app\] |
| [**1.4.11 Non-text Contrast**](https://www.w3.org/TR/WCAG21/#non-text-contrast) (Level AA 2.1 and 2.2) | Supports | The website user interface components have a contrast ratio of at least 3:1 against adjacent color(s). |
| [**1.4.12 Text Spacing**](https://www.w3.org/TR/WCAG21/#text-spacing)<br>(Level AA 2.1 and 2.2) | Supports | The website is compliant with WCAG text spacing requirements. |
| [**1.4.13 Content on Hover or Focus**](https://www.w3.org/TR/WCAG21/#content-on-hover-or-focus) (Level AA 2.1 and 2.2) | Supports | The content that is triggered by hover or focus is dismissible, hoverable, and persistent. |
| [**2.4.5 Multiple Ways**](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-mult-loc)<br>(Level AA) | Not Applicable | The success criterion is not<br>applicable. |
| [**2.4.6 Headings and Labels**](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-descriptive) (Level AA) | Supports | Headings and Labels on the website<br>provide sufficient detail of the content they are describing. |
| [**2.4.7 Focus Visible**](http://www.w3.org/TR/WCAG20/#navigation-mechanisms-focus-visible) (Level AA) | Supports | Interactive elements present on the website have focus visibility. |
| [**2.4.11 Focus Not Obscured (Minimum)**](https://www.w3.org/TR/WCAG22/#focus-not-obscured-minimum) (Level AA 2.2 only) | Supports | All elements that receive keyboard focus are at least partially visible upon receiving the focus. |
| [**2.5.7 Dragging Movements**](https://www.w3.org/TR/WCAG22/#dragging-movements) (Level AA 2.2 only) | Not Applicable | The success criterion is not applicable. |
| [**2.5.8 Target Size (Minimum)**](https://www.w3.org/TR/WCAG22/#target-size-minimum) (Level AA 2.2 only) | Supports | All the interactive pointer targets are at least 24 by 24 CSS pixels or have sufficient spacing around them. |
| [**3.1.2 Language of Parts**](http://www.w3.org/TR/WCAG20/#meaning-other-lang-id)<br>(Level AA) | Not Applicable | English is the primary and only language of the website. There are no phrases or sentences written in any other language, that need to be defined separately. |
| [**3.2.3 Consistent Navigation**](http://www.w3.org/TR/WCAG20/#consistent-behavior-consistent-locations) (Level AA) | Supports | Navigational mechanisms are repeated on the website and occur in the same relative order each time they are repeated. Hence, consistent navigation is provided to the user. |
| [**3.2.4 Consistent Identification**](http://www.w3.org/TR/WCAG20/#consistent-behavior-consistent-functionality) (Level AA) | Supports | Components that provide the same functionality throughout the website can be easily identified by the user. |
| [**3.3.3 Error Suggestion**](http://www.w3.org/TR/WCAG20/#minimize-error-suggestions)<br>(Level AA) | Supports | Error messages are descriptive enough to understand the error and identify the location where they occur. |
| [**3.3.4 Error Prevention (Legal, Financial, Data)**](http://www.w3.org/TR/WCAG20/#minimize-error-reversible) (Level AA) | Not Applicable | There are no critical forms available where error prevention is required. Error suggestions are enough to<br>fill out the form and correct the errors. |
| [**3.3.8 Accessible Authentication (Minimum)**](https://www.w3.org/TR/WCAG22/#accessible-authentication-minimum) (Level AA 2.2 only) | Not Applicable | No such authentication is required<br>on the website. |
| [**4.1.3 Status Messages**](https://www.w3.org/TR/WCAG21/#status-messages)(Level AA 2.1 and 2.2) | Partially Supports | Most of the updated content automatically notifies the visually impaired users via a screen reader.<br>**Exceptions include:**

- The loading notification is not announced automatically as it appears on the screen.
- The screen reader does not announce the 'Generating response' notification automatically.

<br>\[This is specific to a third-party plugin: Intercom app\] |