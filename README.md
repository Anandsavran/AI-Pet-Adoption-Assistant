# Paws & Hearts - AI-Pet-Adoption-Assistant
**Project Overview**

The goal of this project is to make pet adoption easier, friendlier and smarter using artificial intelligence. It stimulates a virtual assistant that can: 

(a) Understand user queries about pets. 

(b) Suggest pets based on preference like breed, size, energy level. 

(c) Provide care tips, adoption process guidance and connect users with shellters.

(d) Help user fill out adoption form - all within one conversational interface.

H uses HTML, CSS and JavaScript for the frontent and Gemini API for intelligent chatbot responses.

**System Architecture**

*Components:*
1. User Interface (Frontent)
   a) Built user HTML and CSS
   b) The UI includes
   
        1) A chat bubble layout
        2) Animations (fade-in, typing indicator)
        3) Responsive quick reply buttons for actions like "Find a dog", "Adoption tips".
        4) Pet cards with images , breed, age, energy level and shelter information
   c) Decorative elements and a background image make the interface feel warm and welcoming.
         
  2. chatbot Interaction Layer (JavaScript)
     a) Manages all user input/output
     b) Detects keywords like  "dogs", "cats", "apartment".
     c) Handle quick replies, form submission and message rendering.
     d) Stores and uses chat history for context-aware replies.
     
3. Static Pet Database
   (a) A small mock dataset stored locally within javaScript.
   (b) Includes pet details like: name, breed, age, image, shelter.
   (c) Helps simulate real API data for testing and demo.

4. Gemini API Integration
   (a) Used for dynamic, AI-generated respones.
   (b) Handle queries not covered by the static database.
   (c) Example : "What dog breeds are good for kids ?" the AI answers based on context.
   (d) Gemini's responses feel humon like and supportive.

**Data Flow Diagram**

   +------------+
   |    User    |
   +------------+
          |
   +-----------------+               +-----------------------+
   | Chat Interface  |     <----->   |  Gemini AI Response   |
   +-----------------+               +-----------------------+
          |
   +----------------------------+
   |  Pet Recommendation Logic  |
   +----------------------------+
          |
   +----------------------------+
   |  Pet Data (MOck DB)        |
   +----------------------------+


User -> Chat interface : input preferences

Interface <--> Gemini AI: If not found in DB, gets response form Gemini.

Interface -> Pet recommendation logic: Matches query to pets.

Logic -> Mock DB: Retrieves cord details.

Final response : Cards are shown back to the user.

**Feature Breakdown**

(1) Quick replies : Buttons like, Find a dog, Find a cat, Adoption Tips.
(2) Pet cards : Visually attractive cards display :
               (a) Pet name, image, age, breed etc.
               (b) shelter and adoption link.
(3) Adoption Form : Simple form inside chat interface: Name, Email, Phone, Reason for adopting.
(4) Footer Menu : Mini navigations like for shelter info, adoption process, contact details.

**AI Assistant Logic**
**Gemini API Prompt Design:**
     (a) Instructs the modle to be informative, helpful.
     (b) Ensures replies format: Pet info core tips.

**Chat context Maintenance**
     (a) Saves past questions as follow-ups make sense (like "tell me more about luna")
**Fallback Handking**
     (a) If unsure, the AI asks clarying questions.

