# 📊 Excel Data Analytics Revision Journey

A structured Excel revision project focused on building analytical thinking through real-world business scenarios using the Sample Superstore Dataset.

---

# 🚀 Learning Roadmap

* ✅ Week 1 – Text Functions
* ✅ Week 2 – Logical Functions
* ✅ Week 3 – Lookup Functions
* ⏳ Week 4 – Aggregation Functions
* ⏳ Week 5 – Pivot Tables
* ⏳ Week 6 – Statistical Analysis
* ⏳ Week 7 – Dashboard Development

---

# 📝 Week 1 Summary – Excel Text Functions Revision

This week was fully focused on mastering Excel Text Functions and developing deeper logical understanding behind text manipulation and parsing.

Instead of only memorizing formulas, the focus was on:

* understanding how formulas work internally
* learning delimiter traversal
* dynamic extraction logic
* parsing text structures
* handling inconsistent data patterns

---

## Functions Practiced

* LEFT
* RIGHT
* MID
* LEN
* FIND
* SEARCH
* SUBSTITUTE
* REPLACE
* TRIM
* CLEAN
* REPT
* EXACT
* UPPER
* LOWER
* PROPER

---

## Advanced Concepts Learned

### 🔹 Delimiter Traversal

Learned how to:

* find first, second, third delimiters
* extract text between delimiters
* extract text after nth delimiter
* dynamically handle variable text structures

### 🔹 Dynamic Text Parsing

Built formulas for:

* extracting first/middle/last names
* extracting initials dynamically
* extracting second-last words
* handling names with varying word counts
* masking names using REPT

### 🔹 Logical Formula Building

Practiced:

* nested FIND structures
* IF + ISNUMBER + SEARCH logic
* IFERROR handling
* AND / OR based conditions
* scalable parsing approaches

### 🔹 Data Cleaning Concepts

Worked on:

* removing extra spaces
* detecting double spaces
* CLEAN vs TRIM understanding
* hidden vs printable characters
* text normalization

---

## 🎯 Most Important Learning

The biggest realization from this week:

**Excel formulas are not just functions — they are logical systems used to parse, structure, and manipulate data dynamically.**

---

# 🧠 Week 2 Summary – Logical Functions

After completing the logical functions phase, I realized that logical functions are not really about formulas—they are about decision making.

At first, I saw functions like IF, AND, OR, NOT, IFERROR, and ISNUMBER as separate Excel tools. But while solving logical scenarios on the Superstore dataset, I started understanding how they work together to validate data, classify records, detect patterns, handle exceptions, and translate business rules into formulas.

### Some of the problems I worked on involved:

* identifying products based on keywords
* validating customer and product information
* detecting missing or inconsistent patterns
* classifying sales, profit, quantity, and discount levels
* checking multiple conditions simultaneously
* building business-style decision rules
* creating dynamic classifications using dataset benchmarks
* comparing records against category, regional, and overall averages
* handling edge cases and validating business assumptions
* designing multi-level business classifications
* evaluating data distributions before creating classification rules

### Key Function Learnings

* AND checks whether all conditions are satisfied
* OR checks whether at least one condition is satisfied
* NOT reverses existing logic
* IFERROR makes formulas more robust
* ISNUMBER combined with SEARCH becomes a powerful pattern-detection technique

### Questions That Changed My Thinking

* Should a customer be compared against the overall average or a regional average?
* What makes a discount "High"?
* How should Profit = 0 be classified?
* Should classifications be based on fixed ranges or dynamic benchmarks?
* How wide should an "Average" range be?
* When does a threshold come from business rules versus data behavior?

Working through these questions taught me that analytical thinking starts before the formula is written.

---

## 📈 Key Insights Discovered

* Average Sales (299) was much larger than Median Sales (54.5), indicating a heavily right-skewed sales distribution.
* Several high-sales orders generated significant losses.
* Heavy discounts frequently appeared in loss-making high-sales transactions.
* Correlation alone was insufficient to explain profitability patterns.

---

## 🎯 Biggest Takeaway

Writing a formula is often the easy part.

**Designing logic that works across different scenarios, edge cases, data distributions, and business situations is where the actual analytical thinking begins.**

### Skills Strengthened

* Logical Reasoning
* Conditional Thinking
* Data Validation
* Problem Decomposition
* Formula Debugging
* Business Rule Design
* Benchmark Analysis
* Classification Design
* Distribution Analysis
* Analytical Thinking

---

# 🔍 Week 3 Summary – Lookup Functions

This week started with learning lookup functions.

Initially, I thought lookup functions were simply Excel formulas used to retrieve values from tables.

However, while solving increasingly complex lookup scenarios, I realized that lookup functions are not primarily about formulas—they are about understanding relationships within data.

---

## Functions Covered

* VLOOKUP ✅
* HLOOKUP ⚠️ (Deferred)
* XLOOKUP ✅
* MATCH ✅
* INDEX ✅
* INDEX + MATCH ✅

---

## Key Concepts Learned

### 🔹 Lookup Table Design

Instead of performing lookups directly on the transaction dataset, I created dedicated lookup tables for products and customers.

#### Product Lookup Table

* Product ID
* Product Name
* Category
* Sub-Category

#### Customer Lookup Table

* Customer ID
* Customer Name
* Segment
* Region

This helped me understand how lookup tables are built from transactional data and why reference tables are important for scalable analysis.

---

### 🔹 Reference Data vs Transaction Data

One of the biggest lessons from this week was understanding that not every column belongs inside a lookup table.

#### Reference Data

Examples:

* Product ID → Product Name
* Product ID → Category
* Product ID → Sub-Category
* Customer ID → Segment
* Customer ID → Region

These relationships remain stable and are suitable for lookup operations.

#### Transaction Data

Examples:

* Sales
* Profit
* Discount
* Quantity

These values change from transaction to transaction and therefore cannot always be treated as lookup attributes.

---

### 🔹 Lookup Key Reliability

A formula can be technically correct while the relationship itself is unreliable.

For example:

```text
Customer ID → Segment
```

is a reliable relationship.

However:

```text
Customer Name → State
```

can become ambiguous.

While working through lookup questions, I discovered that Aaron Bergman appeared across multiple states, which raised an important question:

> Which state should the lookup return?

This taught me that validating relationships is often more important than writing formulas.

---

### 🔹 Composite Keys

As the questions became more advanced, I encountered situations where a single field could not uniquely identify a record.

This led to experimenting with composite keys such as:

* Customer ID + Product ID
* Order ID + Product ID

While investigating duplicates, I learned that reducing duplicates does not automatically make a field a valid business key.

A field can help distinguish records without actually being the true identifier of a business event.

---

### 🔹 Duplicate Investigation

One of the most valuable lessons came from investigating duplicate records.

Instead of immediately adding more columns to remove duplicates, I learned to ask:

* Why do duplicates exist?
* Are they true duplicates?
* Are they separate business events?
* Is the relationship actually one-to-one?

I discovered situations where:

```text
Order ID + Product ID
```

was nearly unique but still contained a small number of duplicate combinations.

Rather than blindly forcing uniqueness, I investigated the data and documented the limitation.

This shifted my focus from formula writing to data investigation.

---

### 🔹 Lookup Dashboard Development

To complete the lookup module, I built a mini lookup dashboard.

The dashboard allows users to:

* Select an Order ID
* Select a Product ID

and dynamically retrieve:

* Customer Name
* Customer ID
* Segment
* Region
* Product Name
* Category
* Sub-Category
* Sales
* Profit
* Discount
* Quantity

using lookup functions and composite-key logic.

This exercise connected all lookup concepts into a practical business scenario.

---

### 🔹 Data Modeling Mindset

A major change in my thinking occurred during this week.

Earlier I approached problems as:

```text
Question → Formula → Answer
```

Now I approach them as:

```text
Question
↓
What data is available?
↓
What relationship exists?
↓
Is the relationship reliable?
↓
What key should be used?
↓
Then choose the formula
```

This feels much closer to how databases, SQL joins, and Power BI relationships work.

---

## 🎯 Biggest Takeaway

Lookup functions are not primarily about retrieving values.

They are about understanding relationships.

Before writing a lookup formula, I should first ask:

* Is the lookup key reliable?
* Is the relationship one-to-one or one-to-many?
* Does the data support the conclusion?
* Am I retrieving reference data or transaction data?

Only then does the formula become meaningful.

---

### Skills Strengthened

* Lookup Table Design
* Relationship Validation
* Composite Key Creation
* Duplicate Investigation
* Data Modeling
* Dashboard Construction
* Formula Debugging
* Analytical Thinking
* Business Logic Evaluation

The most important lesson from this week was:

> A correct formula cannot fix an unreliable relationship.

Understanding the structure of the data is often more important than writing the formula itself.

---

# 🔜 Next Phase

* Aggregation Functions
* Pivot Tables
* Statistical Analysis
* Business Dashboards

---

# 🎯 Final Goal

Build a complete Excel Analytics Project that demonstrates:

* Data Cleaning
* Text Processing
* Logical Analysis
* Lookup Functions
* Aggregation Functions
* Pivot Tables
* Statistical Analysis
* Interactive Dashboards

while documenting the entire learning journey publicly through GitHub.
