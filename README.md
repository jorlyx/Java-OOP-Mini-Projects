# Java-OOP-Mini-Projects
Overview
A compact portfolio of Java exercises demonstrating solid OOP, collections & arrays, enums, validation & exceptions, file I/O, interfaces & polymorphism, and numeric/business logic.
Each mini-project models a small, realistic domain (grades, payroll, timetables, billing, rainfall, pizza orders, colour mixing, student tracking, hotel charges) and is designed to pass strict JUnit tests with exact output formatting.

This was a solo university coursework project completed in my First Year

 
Features

• Clean object models & composition with purposeful constructors and minimal getters/setters.
• Exact, human-readable outputs via toString()/display methods (reports, receipts, summaries).
• Validation & error handling
o Regex/format checks (module codes, account numbers, service codes).
o Defensive array bounds; duplicate prevention in lists.
o Input sanitisation and exceptions (IllegalArgumentException) where required.
• Enums as first-class design tools (ingredient types, primary colours, VAT rates).
• Collections used appropriately
o Fixed arrays for capacity-bound data.
o ArrayList and Map for dynamic aggregates and lookups.
• Business rules implemented
o Weighted assessment averages.
o Progressive income tax (simplified).
o Tiered pizza pricing.
o Colour mixing logic (primary → secondary; all three → black).
o VAT totals by rate (ZERO/LOW/STANDARD).
• Test-friendly design aligned to pre-defined JUnit assertions and exact string comparisons.
 
How It Works

• Academic Progress & Timetabling: assessments roll up to module averages; students hold fixed-size module arrays; daily timetables store sessions and print "NAME: start - end".
• Payroll & HR: salary objects compute tax with constants and brackets; employees compose positions and salaries, include bonus eligibility checks.
• Classroom Roster: capacity-limited arrays with add/summary/count operations and safe indexing.
• Billing & Utilities: gas bills validate account format (Gdddd-dddd-dddd); display routines print exact multi-line statements.
• Analytics: rainfall year stores 12 months, calculates mean and max.
• Food Ordering: pizzas accept up to 10 toppings; tiered pricing (with 10-topping special); orders total receipts.
• Suppliers & Ingredients: enum-typed ingredients with cooked weight = 80% of raw; supplier phone validation.
• Colours & Palettes: primary colours enum; palette prevents duplicates/over-capacity; mixing yields secondary or black; formatted with StringBuilder.
• Student Tracking: modules validated (COM + 4 digits or "Error"), students store unique module lists; tracker maintains list + map (URN → modules) for printing enrolled modules.
• Input Validation & Exceptions: customer names enforced (Capitalised letters only); invalid inputs throw and block object creation.
• File I/O: read text files, format lines with counters, parse to Person objects, and display lists.
• Hotel Charges System: services with VAT rates, charges per guest, IGuest interface with concrete Guest implementation; compute totals without/with VAT and VAT by rate; hotel prints guest list.
 
Project Structure

/src
 ├─ ProblemSet_2c/
 │   Assessment.java
 │   Module.java
 │   Test.java

 ├─ ProblemSet_3a/
 │   Position.java
 │   Test.java

 ├─ ProblemSet_3b/
 │   AnnualSalary.java
 │   Test.java

 ├─ ProblemSet_3c/
 │   Position.java
 │   AnnualSalary.java
 │   Employee.java
 │   Test.java

 ├─ ProblemSet_4a/
 │   Session.java
 │   Day.java
 │   Test.java

 ├─ ProblemSet_4b/
 │   Student.java
 │   Classroom.java
 │   Test.java

 ├─ ProblemSet_4c/
 │   Module.java
 │   Student.java
 │   Test.java

 ├─ ProblemSet_5a/
 │   RainfallYear.java
 │   Test.java

 ├─ ProblemSet_5b/
 │   Customer.java
 │   GasBill.java
 │   Test.java

 ├─ ProblemSet_5c/
 │   Customer.java
 │   Pizza.java
 │   Order.java
 │   Test.java

 ├─ ProblemSet_6a/
 │   IngredientType.java
 │   Supplier.java
 │   Ingredient.java
 │   Test.java

 ├─ ProblemSet_6b/
 │   P_COLOUR.java
 │   Palette.java
 │   Test.java

 ├─ ProblemSet_6c/
 │   P_COLOUR.java
 │   Palette.java     // with mixColours() & display()
 │   Test.java

 ├─ ProblemSet_7a/
 │   Module.java      // validates code or sets "Error"
 │   Test.java

 ├─ ProblemSet_7b/
 │   Module.java
 │   Student.java     // list of unique modules
 │   Test.java

 ├─ ProblemSet_7c/
 │   Module.java
 │   Student.java
 │   StudentTracker.java  // list + map (URN → modules)
 │   Test.java

 ├─ ProblemSet_8a/
 │   Customer.java    // validation + IllegalArgumentException
 │   Test.java

 ├─ ProblemSet_8b/
 │   Counting.java    // file I/O + line counters
 │   words.txt (example, if provided)
 │   Test.java

 ├─ ProblemSet_8c/
 │   Person.java
 │   PersonTracker.java  // read → parse → list
 │   people.txt (example, if provided)
 │   Test.java

 ├─ ProblemSet_9a/
 │   VATRate.java
 │   Service.java     // code validation (AAAA#####)
 │   Charge.java      // positive charges; VAT calc helper
 │   Test.java

 ├─ ProblemSet_9b/
 │   VATRate.java
 │   Service.java
 │   Charge.java
 │   IGuest.java
 │   Guest.java
 │   Test.java

 └─ ProblemSet_9c/
     Hotel.java
     Guest.java
     Service.java
     Charge.java
     VATRate.java
     Test.java

 
Skills Demonstrated

• OOP & Design: composition, encapsulation, purposeful constructors, readable toString().
• Collections & Arrays: fixed arrays with bounds checks; ArrayList & Map for dynamic data.
• Enums & Polymorphism: domain modelling with enums; interfaces (IGuest) and concrete implementations.
• Validation & Exceptions: regex/format checks; fail-fast object construction with clear exceptions.
• File I/O: reading, parsing, line-by-line formatting, and object population from text.
• Numeric/Business Logic: weighted means, progressive tax, VAT by rate, tiered pricing, colour mixing rules.
• Formatting & Style: exact string outputs; Java style guidelines (names, spacing, braces, comments).
• Testing Mindset: designing to pass strict JUnit assertions and edge cases.
 
Possible Improvements

• Money & Precision: use BigDecimal and locale-aware currency formatting end-to-end.
• Config over constants: move weights, tax/VAT rates, and pricing tiers to config/enums or strategy classes.
• Error reporting: richer exception messages and domain-specific exceptions.
• Time handling: replace integer times with LocalTime and validate overlaps.
• Persistence / I/O: JSON/CSV import-export; JDBC layer for realistic datasets.
• CLI/GUI: small command-line or JavaFX/Swing demos to interact with each mini-app.
• CI & Docs: GitHub Actions for test runs on push; Javadoc; embedded UML diagrams.
• Testing depth: parameterised tests, boundary tests, and property-based checks (e.g., palette dedup/capacity).
