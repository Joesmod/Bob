# Venue Research Run - Feb 28, 2026

## Summary
Researched 8 venues from pipeline (score >= 50, no existing research). **Only 1 of 8 was actually a viable ticketed venue.**

## Results

### ✅ Successfully Researched (1/8)

1. **Cannery Hall (The Mil)** - Row 71
   - ✅ Real multi-venue complex in Nashville
   - ✅ Uses AXS ticketing
   - ✅ Active show calendar
   - Profile: `venues/us/tn/nashville/mil-cannery-hall.md`
   - Score: 75/100 (Strong Prospect)

### ❌ Data Quality Issues (7/8)

2. **The Marquee Ballroom** - Row 110 (Halifax, NS, CA)
   - Website doesn't exist (themarqueeclub.ca)
   - Cannot research

3. **Ccads Canzani Center** - Row 89 (Columbus, OH)
   - NOT A VENUE - Columbus College of Art & Design (art school)
   - Bad data

4. **Dirty Dungarees** - Row 87 (Columbus, OH)
   - Laundromat/dive bar combo
   - Has live shows BUT no cover charge (free shows)
   - Not a ticketed venue
   - Not a fit for Opendate

5. **Ohio Christian University Ministry And Performing Arts Center** - Row 75
   - Website doesn't exist (osugiving.com/mcknightcenter)
   - Cannot research

6. **Ivy Hall Studio** - Row 74 (Nashville, TN)
   - NOT A VENUE - Recording studio
   - Does day rentals for recording sessions, not ticketed shows
   - Bad data

7. **Wits End** - Row 72 (Nashville, TN)
   - NOT A VENUE - Tavern/restaurant
   - Wrong location (phone 845 = New York, not Nashville)
   - Bad data

8. **Ashley Mcbrydes** - Row 70 (Nashville, TN)
   - NOT A VENUE - Artist website (Ashley McBryde, country singer)
   - Bad data

## Data Quality Observations

- **87.5% failure rate** (7 of 8 not viable)
- Common issues:
  - Non-venue businesses classified as venues
  - Artist/band websites mistaken for venue websites
  - Dead/non-existent websites
  - Wrong location data
  - Venues with free shows (no ticketing) included

## Recommendations

1. **Pre-filter pipeline**: Check if website actually exists before scoring
2. **Venue validation**: Cross-reference website content to confirm it's actually a performance venue
3. **Ticketing requirement**: Add filter for venues that actually sell tickets (not free entry)
4. **Data source review**: Examine where this data came from and improve initial collection

## Next Steps

- Need to find more REAL venues to research
- Consider pulling from different data sources
- May need manual venue discovery/validation before bulk scoring
