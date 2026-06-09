# 📊 Excel Data Analytics Revision Journey

A structured Excel revision project focused on building analytical thinking through real-world business scenarios using the Sample Superstore Dataset.

---

# 🚀 Learning Roadmap

* ✅ Week 1 – Text Functions
* ✅ Week 2 – Logical Functions
* 🔄 Week 3 – Lookup Functions (In Progress)
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

One important lesson was understanding the difference between checking values and checking structure. Instead of extracting text unnecessarily, many problems could be solved by validating the underlying structure of the data itself.

### Key Function Learnings

* AND checks whether all conditions are satisfied
* OR checks whether at least one condition is satisfied
* NOT reverses existing logic
* IFERROR makes formulas more robust
* ISNUMBER combined with SEARCH becomes a powerful pattern-detection technique

As the questions became more complex, I noticed that the challenge was no longer writing formulas. The real challenge was defining the business rule behind the formula.

### Questions That Changed My Thinking

* Should a customer be compared against the overall average or a regional average?
* What makes a discount "High"?
* How should Profit = 0 be classified?
* Should classifications be based on fixed ranges or dynamic benchmarks?
* How wide should an "Average" range be?
* When does a threshold come from business rules versus data behavior?

Working through these questions taught me that analytical thinking starts before the formula is written.

Another important lesson came from exploring relationships within the data. While analyzing Sales, Profit, and Discount, I learned that correlation alone is not enough. A high-sales order can still generate a large loss if other factors, such as heavy discounts, are involved. This reinforced the importance of investigating outliers, understanding context, and looking beyond summary metrics.

I also learned that a formula returning no results does not automatically mean the formula is wrong. In one scenario, the condition itself became mathematically impossible because a regional benchmark was lower than the overall benchmark. This showed me the importance of validating assumptions and benchmark relationships before debugging formulas.

One of the most valuable lessons came from profit classification. Rather than choosing arbitrary thresholds, I explored the profit distribution and identified points where the pattern of profits changed significantly. This helped me understand that good classifications should be supported by data behavior whenever possible.

A threshold is more meaningful when it reflects a visible change in the distribution rather than a random multiple of an average.

As I progressed through advanced logical scenarios, I started thinking more like an analyst than an Excel user.

Instead of asking:

> Which formula should I use?

I increasingly found myself asking:

* What benchmark should be used?
* What classification makes business sense?
* What does the data distribution suggest?
* Is this threshold justified by the data?
* Am I analyzing orders, customers, categories, or regions?
* Is this actually a logical-function problem, or does it belong to aggregation or lookup functions?

I also realized that an average is often better treated as a range rather than a single value. The width of that range can dramatically change the classification results, which means business definitions have a direct impact on analytical outcomes.

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

* logical reasoning
* conditional thinking
* data validation skills
* problem decomposition
* formula debugging
* business rule design
* benchmark analysis
* classification design
* distribution analysis
* analytical thinking

More importantly, it changed how I view Excel. Instead of seeing formulas as isolated functions, I now see them as tools for building logical systems that help make decisions from data.

I also discovered that many advanced business questions require more than logical functions alone. Some problems naturally lead into aggregation, lookup functions, Pivot Tables, and statistical thinking.

This helped me understand how different Excel concepts connect together in real-world analysis and why choosing the right analytical tool is just as important as writing the correct formula.

---

# 🔍 Week 3 Summary – Lookup Functions (In Progress)

This week introduced the concept of data retrieval and lookup design.

While learning VLOOKUP, I discovered that lookup functions are not primarily about formulas. They are about retrieving the correct information from the correct source.

### Functions Covered

* VLOOKUP ✅
* HLOOKUP ⚠️ (Deferred)
* XLOOKUP 🔄 (Upcoming)
* MATCH ⏳
* INDEX ⏳
* INDEX + MATCH ⏳

---

## Key Concepts Learned

### 🔹 Lookup Table Design

Created dedicated lookup tables from the Superstore dataset instead of performing lookups directly on transactional data.

#### Product Lookup Table

* Product Name
* Category
* Sub-Category

Approximately 9,995 transaction records were reduced to around 1,850 unique product records suitable for lookup operations.

#### Customer Lookup Table

* Customer Name
* Segment
* Region

Approximately 793 unique customers were identified for customer-based lookup operations.

---

### 🔹 Reference Data vs Transaction Data

One of the most important discoveries during this phase.

#### Reference Data

Attributes that remain stable for a given key:

* Product → Category
* Product → Sub-Category
* Customer → Segment
* Customer → Region

These relationships are suitable for lookup tables because each key maps to a consistent set of attributes.

#### Transaction Data

Attributes that vary between transactions:

* Sales
* Profit
* Discount
* Quantity

I learned that transaction-based values cannot simply be converted into lookup tables because they vary from one record to another.

If such metrics need to be retrieved through lookups, they must first be summarized using aggregation techniques such as Pivot Tables, SUMIFS, AVERAGEIFS, or COUNTIFS.

---

### 🔹 Data Modeling Mindset

A lookup table should contain:

**One Unique Key → One Stable Set of Attributes**

This simple idea connects directly to:

* SQL Joins
* Power BI Relationships
* Data Modeling
* Database Design

---

## 🎯 Biggest Takeaway

Lookup functions are not primarily about formulas.

**They are about designing the correct relationship between data sources.**

The most important lesson was learning that before retrieving information, I must first determine whether the data represents a stable attribute or a transactional metric.

---

# 🔜 Next Phase

* XLOOKUP
* MATCH
* INDEX
* INDEX + MATCH
* Aggregation Functions
* Pivot Tables
* Statistical Analysis
* Business Dashboards

---

# 📂 Dataset Used

**Sample Superstore Dataset**

Used throughout the project for:

* Text Parsing
* Data Cleaning
* Business Rule Design
* Classification Analysis
* Lookup Table Design
* Data Retrieval
* Analytical Problem Solving

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

while documenting the complete learning journey publicly through GitHub.
