# Will the Customer Accept the Coupon?

## Project Overview

This project analyzes survey data to understand what factors influence whether drivers accept coupons delivered to their mobile devices while driving. The analysis explores customer behavior patterns, contextual factors, and demographic characteristics to identify what makes someone more likely to accept or reject different types of coupons.

## Dataset

The data comes from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. The dataset includes:

- **12,684 driving scenarios** covering different destinations, times, weather conditions, and passenger situations
- **Five types of coupons**: Less expensive restaurants (under $20), coffee houses, carry out & take away, bars, and more expensive restaurants ($20-$50)
- **Driver characteristics**: Age, gender, income, education, occupation, and frequency of visits to various establishments
- **Contextual information**: Destination, time of day, weather, temperature, passenger type, and coupon expiration time

## Key Findings

### Overall Acceptance Rate

Across all coupon types, **approximately 57% of coupons are accepted**. This means that more than half of the time, drivers find coupons useful enough to accept them for immediate or later use.

### What Makes Customers Accept Coupons?

The analysis reveals several important patterns:

#### 1. **Frequent Visitors Are More Likely to Accept**

The strongest predictor of coupon acceptance is how often someone already visits similar establishments:
- Drivers who visit bars more than 3 times per month are significantly more likely to accept bar coupons than those who rarely or never visit bars
- The same pattern holds true for coffee houses and restaurants - habitual visitors are the best targets

**Why this matters**: People who already frequent these types of places are more receptive to coupons for them. It's easier to get someone to use a coupon for a place they already go.

#### 2. **Context Is Critical**

The situation matters just as much as the person:

**Bar Coupons:**
- Rarely accepted when children are passengers (makes sense - bars are adult-oriented)
- More likely accepted during evening hours (6PM)
- Best for drivers under age 30 who frequently visit bars

**Coffee House Coupons:**
- Highest acceptance rate when drivers are heading to work in the morning
- Most effective during commute hours (7AM-10AM)
- People who visit coffee houses regularly and are commuting to work show the strongest acceptance patterns

**Why this matters**: Timing and situation determine whether a coupon feels relevant. A coffee coupon when heading to work feels natural; a bar coupon with kids in the car does not.

#### 3. **Demographics Play a Role**

- **Age**: Younger drivers (under 30) show higher acceptance rates for bar coupons
- **Lifestyle patterns**: Drivers whose behavior patterns align with the coupon type (e.g., frequent bar-goers for bar coupons) are much more likely to accept

### Differences Between Acceptors and Non-Acceptors

#### Customers Who ACCEPT Coupons:
- Already visit similar establishments regularly (habitual customers)
- Are in appropriate contexts (e.g., no children when receiving bar coupons)
- Match the demographic profile for the coupon type
- Receive coupons that fit naturally into their current travel pattern

#### Customers Who REJECT Coupons:
- Rarely or never visit the type of establishment featured
- Are in inappropriate contexts (e.g., bar coupon with children present)
- Don't match the typical customer profile for that business type
- Receive coupons that don't align with their current destination or travel purpose

## Business Recommendations

### 1. **Target the Right People**

Focus coupon distribution on drivers who already visit similar establishments frequently. These habitual customers are much more likely to accept and use coupons.

### 2. **Consider the Context**

- **Bar coupons**: Only send when drivers don't have children as passengers, preferably in the evening
- **Coffee house coupons**: Target morning commute hours when drivers are heading to work
- **Restaurant coupons**: Consider meal times and destination patterns

### 3. **Time Your Distribution**

Match coupon delivery to when it makes sense:
- Coffee coupons during morning commutes
- Bar coupons during evening hours
- Restaurant coupons around typical meal times

### 4. **Avoid Obvious Mismatches**

Don't send bar coupons to drivers with children in the car - this is almost always rejected and creates a poor customer experience.

## Technical Details

### Tools Used
- Python (pandas, numpy)
- Data visualization (matplotlib, seaborn)
- Jupyter Notebook for interactive analysis

### Data Cleaning
- Removed the 'car' column (99% missing values, not informative)
- Replaced missing values in frequency columns with 'never' (indicating no visits to those establishments)
- All analysis performed on cleaned dataset of 12,684 observations

## Files in This Repository

- `prompt.ipynb` - Complete Jupyter notebook with data analysis, visualizations, and findings
- `data/coupons.csv` - Original dataset from UCI Machine Learning Repository
- `README.md` - This file (non-technical summary)

## Conclusion

The analysis shows that coupon acceptance isn't random - it follows clear patterns based on customer behavior, context, and demographics. By targeting the right customers at the right time in the right situation, businesses can significantly improve coupon acceptance rates. The key is understanding that people are most receptive to coupons for places they already visit, when those coupons fit naturally into their current situation.

---

*This project was completed as part of the UC Berkeley Data Science program, demonstrating skills in data cleaning, exploratory data analysis, statistical summaries, and data visualization.*

