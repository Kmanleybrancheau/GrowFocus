Core Technical Risks
Highest Risk Feature: Tab Checking
The Hazard: Web browsers deliberately limit how much a website can see or control. A web page cannot truly "lock" the browser or see other windows on the screen. It can only detect that its own tab was hidden or lost focus, and a student can use a second monitor or a phone without triggering anything. Fullscreen mode can also be exited easily, and behavior differs between Chrome, Safari, and mobile browsers.
The Pivot Strategy

If our primary implementation for this feature fails or takes too long, our backup plan is to:

Simplify the detection method. Rely only on the Page Visibility API and window blur events (detecting "the student left this tab"), and drop strict fullscreen enforcement. This works consistently across browsers.
Fall back to a self-report mode. If detection proves unreliable on a platform, let students tap an "I got distracted" button that adds time, and log the distractions locally so the Adaptive Study Times feature still works.
