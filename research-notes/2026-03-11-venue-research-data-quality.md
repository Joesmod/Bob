# Venue Research Data Quality Issues - March 11, 2026

## Summary
Attempted to research 8 high-scoring venues (score: 60) that needed profiles. **All 8 turned out to be miscategorized or had incorrect website data.**

## Venues Investigated

### 1. Plaza Theatre (Row 529) - Garland, TX
- **Listed Website:** http://www.civicartsplaza.com/
- **Actual Redirect:** Bank of America Performing Arts Center, Thousand Oaks, CA
- **Issue:** Wrong venue entirely - website redirects to different state
- **Uses Ticketmaster**

### 2. Uptown Theater (Row 528) - Grand Prairie, TX  
- **Listed Website:** http://www.uptownbham.com/
- **Actual Redirect:** BJCC Birmingham-Jefferson Convention Complex, Birmingham, AL
- **Issue:** Wrong venue entirely - website redirects to different state

### 3-4. Alhambra Palace / Alhambra Palace Courtyard (Rows 448, 449) - Chicago, IL
- **Website:** https://alhambrapalacechicago.com
- **Issue:** Restaurant with belly dancing entertainment, NOT a ticketing venue
- **Details:** Fine dining + Friday/Saturday night shows (included with dinner), no ticket sales

### 5. Acres (Row 440) - Listed as UK, W10 5QZ
- **Website:** https://www.legacyacresar.com/
- **Actual Location:** Conway, Arkansas (not UK!)
- **Issue:** Wedding/corporate event venue rental, NOT a ticketing venue
- **Details:** Ballroom + pavilion rentals, no public ticketed shows

### 6. Mother Foucaults Bookshop (Row 383) - Portland, OR
- **Website:** https://www.motherfoucaultsbookshop.com
- **Issue:** Used bookstore with FREE reading events
- **Details:** Thursday-Saturday readings, no ticket sales

### 7. House Show (Row 345) - Seattle, WA
- **Website:** https://www.seattlehomeshow.com
- **Issue:** Home & Garden EXPO, not an entertainment venue
- **Details:** Annual trade show, admission tickets but not a music/entertainment venue

### 8. 3 Monkeys Richmond (Row 331) - Richmond, VA
- **Website:** https://3monkeysfan.com
- **Issue:** Bar & Grill, NOT a ticketing venue
- **Details:** Happy hour specials, food menu, no shows or events

## Root Causes

1. **Website scraping errors** - Some venues have completely wrong URLs pointing to different venues in different states
2. **Venue type misclassification** - Restaurants, bars, wedding venues, bookstores being flagged as ticketing venues
3. **Geographic data errors** - UK postcodes in Arkansas, wrong cities/states
4. **Scoring algorithm issues** - All miscategorized venues scored 60/100, suggesting the scoring doesn't effectively filter out non-venues

## Recommendations

1. **Improve venue type detection** - Add logic to filter out:
   - Restaurants (even with entertainment)
   - Wedding/event rental spaces
   - Trade shows/expos
   - Bars without regular ticketed shows
   - Bookstores, retail spaces

2. **Website validation** - Check that listed URL domain matches expected location before research
3. **Manual review threshold** - Consider flagging certain patterns (bars, grills, cafes) for manual review before research
4. **Scoring weights** - Adjust scoring to heavily penalize non-venue indicators

## Next Steps
- Report findings to Alex for pipeline improvement
- Focus research efforts on venues with more reliable indicators (capacity, existing ticketing providers, etc.)
