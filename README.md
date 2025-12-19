# Ex09 Event Registration Web Application
## Date:19.12.25

## AIM:
To design, develop and deploy a web application for event registration.

## DESIGN STEPS:

### Step 1:
Create a new frame.

### Step 2:
Select any one preset size of your choice.

### Step 3:
Select the shapes you need.

### Step 4:
Import images as needed.

### Step 5:
Create pages based on your need and link them.

### Step 6:

Validate the HTML and CSS code.

### Step 6:

Publish the website in the given URL.

## DESIGN TOOL:
Figma

## CODE:
```
import React from "react";
import rectangle2 from "./rectangle-2.svg";
import rectangle3 from "./rectangle-3.svg";
import screenshot202512121130271 from "./screenshot-2025-12-12-113027-1.png";
import textOnAPath from "./text-on-a-path.svg";

const eventData = {
  name: "Drestein 2026",
  type: "Technical & Cultural Fest",
  organizedBy: "Department of Engineering / Student Council",
  institution: "Saveetha Engineering College",
  academicYear: "2025–2026",
  date: "15th & 16th February 2026",
  time: "9:00 AM – 5:00 PM",
  venue: "Saveetha Engineering College Campus",
};

const eventDetails = [
  { label: "Event Name", value: eventData.name },
  { label: "Type of Event", value: eventData.type },
  { label: "Organized By", value: eventData.organizedBy },
  { label: "Institution", value: eventData.institution },
  { label: "Academic Year", value: eventData.academicYear },
  { label: "Date", value: eventData.date },
  { label: "Time", value: eventData.time },
  { label: "Venue", value: eventData.venue },
];

export const IphonePlus = (): JSX.Element => {
  return (
    <main
      className="bg-[#9b373c] overflow-hidden w-full min-w-[428px] min-h-[926px] relative"
      role="main"
      aria-label="Event Details Page"
    >
      <img
        className="absolute top-[138px] left-0 w-[428px] h-[397px] aspect-[1.14] object-cover"
        alt="Saveetha Engineering College temple architecture"
        src={screenshot202512121130271}
      />

      <section
        className="absolute top-[131px] left-0 w-[1763px] [font-family:'Inter-Regular',Helvetica] font-normal text-white text-2xl tracking-[0] leading-[normal]"
        aria-label="Event Information"
      >
        {eventDetails.map((detail, index) => (
          <React.Fragment key={index}>
            {detail.label}: {detail.value}
            {index < eventDetails.length - 1 && <br />}
          </React.Fragment>
        ))}
      </section>

      <img
        className="absolute top-[652px] left-[-540px] w-[281px] h-[124px]"
        alt=""
        role="presentation"
        src={rectangle2}
      />

      <img
        className="absolute top-[776px] left-[-576px] w-[330px] h-[138px]"
        alt=""
        role="presentation"
        src={textOnAPath}
      />

      <img
        className="absolute top-[70px] left-10 w-[348px] h-[52px]"
        alt=""
        role="presentation"
        src={rectangle3}
      />

      <header className="absolute top-16 left-[52px] w-[425px] [font-family:'Inter-Regular',Helvetica] font-normal text-black text-5xl tracking-[0] leading-[normal]">
        <h1>EVENT DETAIL</h1>
      </header>
    </main>
  );
};
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  button,
  input,
  select,
  textarea {
    @apply appearance-none bg-transparent border-0 outline-none;
  }
}

@tailwind components;
@tailwind utilities;

@layer components {
  .all-\[unset\] {
    all: unset;
  }
}

:root {
  --animate-spin: spin 1s linear infinite;
}

.animate-fade-in {
  animation: fade-in 1s var(--animation-delay, 0s) ease forwards;
}

.animate-fade-up {
  animation: fade-up 1s var(--animation-delay, 0s) ease forwards;
}

.animate-marquee {
  animation: marquee var(--duration) infinite linear;
}

.animate-marquee-vertical {
  animation: marquee-vertical var(--duration) linear infinite;
}

.animate-shimmer {
  animation: shimmer 8s infinite;
}

.animate-spin {
  animation: var(--animate-spin);
}

@keyframes spin {
  to {
    transform: rotate(1turn);
  }
}

@keyframes image-glow {
  0% {
    opacity: 0;
    animation-timing-function: cubic-bezier(0.74, 0.25, 0.76, 1);
  }

  10% {
    opacity: 0.7;
    animation-timing-function: cubic-bezier(0.12, 0.01, 0.08, 0.99);
  }

  to {
    opacity: 0.4;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(-10px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes fade-up {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes shimmer {
  0%,
  90%,
  to {
    background-position: calc(-100% - var(--shimmer-width)) 0;
  }

  30%,
  60% {
    background-position: calc(100% + var(--shimmer-width)) 0;
  }
}

@keyframes marquee {
  0% {
    transform: translate(0);
  }

  to {
    transform: translateX(calc(-100% - var(--gap)));
  }
}

@keyframes marquee-vertical {
  0% {
    transform: translateY(0);
  }

  to {
    transform: translateY(calc(-100% - var(--gap)));
  }
}
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  button,
  input,
  select,
  textarea {
    @apply appearance-none bg-transparent border-0 outline-none;
  }
}

@tailwind components;
@tailwind utilities;

@layer components {
  .all-\[unset\] {
    all: unset;
  }
}

:root {
  --animate-spin: spin 1s linear infinite;
}

.animate-fade-in {
  animation: fade-in 1s var(--animation-delay, 0s) ease forwards;
}

.animate-fade-up {
  animation: fade-up 1s var(--animation-delay, 0s) ease forwards;
}

.animate-marquee {
  animation: marquee var(--duration) infinite linear;
}

.animate-marquee-vertical {
  animation: marquee-vertical var(--duration) linear infinite;
}

.animate-shimmer {
  animation: shimmer 8s infinite;
}

.animate-spin {
  animation: var(--animate-spin);
}

@keyframes spin {
  to {
    transform: rotate(1turn);
  }
}

@keyframes image-glow {
  0% {
    opacity: 0;
    animation-timing-function: cubic-bezier(0.74, 0.25, 0.76, 1);
  }

  10% {
    opacity: 0.7;
    animation-timing-function: cubic-bezier(0.12, 0.01, 0.08, 0.99);
  }

  to {
    opacity: 0.4;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(-10px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes fade-up {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes shimmer {
  0%,
  90%,
  to {
    background-position: calc(-100% - var(--shimmer-width)) 0;
  }

  30%,
  60% {
    background-position: calc(100% + var(--shimmer-width)) 0;
  }
}

@keyframes marquee {
  0% {
    transform: translate(0);
  }

  to {
    transform: translateX(calc(-100% - var(--gap)));
  }
}

@keyframes marquee-vertical {
  0% {
    transform: translateY(0);
  }

  to {
    transform: translateY(calc(-100% - var(--gap)));
  }
}
```
## OUTPUT:
![alt text](<Screenshot 2025-12-19 142527-1.png>)


## RESULT:
The program to design, develop and deploy a web application for event registration is completed successfully.
