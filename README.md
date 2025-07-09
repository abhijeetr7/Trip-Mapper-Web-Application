# Trip-Mapper-Web-Application

How to Use and Test:

Save the code: Save the entire block above as index.html.

Open in Browser: Open the index.html file in your web browser.

Explore the UI:

You'll see three main panels: "Search & Saved Places" (left), "Your Itinerary" (middle), and "Map Preview, Budget, Weather, Recommendations" (right).

On smaller screens (e.g., mobile), the left and right panels will collapse into a draggable "bottom drawer".

Search & Add Places:

Type a place name (e.g., "Eiffel Tower", "Goa Beach", "Colosseum") into the "Search for places..." input and click "Search".

Mock results will appear. Click "Add to Saved" to move them to the "Saved Places" list.

Click on a saved place card to see mock details (image, rating, description).

Build Itinerary:

Drag and drop places from the "Saved Places" list into the "Day 1" timeline.

Click "Add New Day" to create more days.

Drag and drop itinerary items to reorder them within a day or move them between days.

Each itinerary item has fields to set "Cost" and "Category". Change these to see the "Day Budget" and "Total Estimated Cost" update, and the "Budget Pie Chart" change.

Map, Budget, Weather, Recommendations:

The "Map Preview" will update with markers and paths as you add places to your itinerary (requires Google Maps API to load correctly).

The "Budget Tracker" and "Weather Forecast" sections will automatically update based on your itinerary.

"Smart Recommendations" will suggest places from your "Saved Places" that are not yet in your itinerary.

Undo/Redo:

Use the "Undo" and "Redo" buttons to revert or re-apply itinerary changes.

AI Itinerary Suggestion:

Enter a city (e.g., "Goa") into the "AI Itinerary Suggestion" input and click "Auto-fill Trip". This will use a mocked Gemini API call to generate a 3-day itinerary and populate your plan.

Save/Load:

"Save Trip" will save your current plan to Firestore (if Firebase is configured and authenticated) and LocalStorage.

"Load Trip" will attempt to load from Firestore first, then LocalStorage.

Download/Share:

"Download PDF" will generate a PDF of your current view.

"Share Trip" will generate a unique URL and QR code that encodes your trip data. You can copy the link or scan the QR code to share. When someone opens this link, they'll be prompted to load your shared trip.

Key Features Implemented:

Day-wise Itinerary Timeline (Drag-and-Drop): Implemented with collapsible day panels, drag-and-drop for places from saved list, and reordering within/between days. Touch support included.

Distance & Time Estimation: Mocked Google Maps Distance Matrix API is used to show estimates between consecutive stops.

Search & Save Places: Mocked Google Places Autocomplete API for search, with functionality to add results to a saved list and view mock details.

Download & Share Plan: PDF export using html2pdf.js and shareable link/QR code generation using qrcode.js.

Sticky Map Preview Panel: Google Maps API integration (with placeholder key) to display itinerary paths and markers. Fullscreen toggle included.

Smart Recommendations Engine: Basic recommendations based on saved places not in the itinerary, with mock badges.

Budget & Activity Tracker: Input fields for cost/category per place, day-wise and total budget calculation, and a pie chart visualization using Canvas API.

Weather Integration: Mocked OpenWeatherMap API to display weather per day and show warnings.

Offline Sync (LocalStorage & Firestore): Automatic saving/loading to/from LocalStorage and Firestore (requires Firebase setup and authentication). beforeunload warning.

Mobile-First Responsive Design: CSS Grid/Flexbox for adaptive layouts, media queries for breakpoints, and a bottom drawer for mobile.

Undo/Redo for Itinerary Changes: History stack for up to 10 actions.

AI-Powered Itinerary Suggestions: Mocked Gemini API call to generate a 3-day itinerary for a given city.

This comprehensive index.html file provides a robust foundation for your Trip Mapper application, fulfilling all the requirements!
