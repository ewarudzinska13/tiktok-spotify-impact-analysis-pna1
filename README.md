# tiktok-spotify-impact-analysis-pna1
Analyzing the impact of TikTok platform on music popularity in streaming services (Spotify) using Method of Moments estimation

# TikTok's Impact on Spotify Streaming Numbers

Thesis examining the relationship between TikTok activity and music popularity on Spotify streaming platform. Conducted at the University of Warsaw, Faculty of Economic Sciences (2023).

## Research Overview

This study investigates whether and how the TikTok platform influences music consumption in streaming services, focusing on Spotify. As TikTok is a relatively new and rapidly evolving phenomenon, limited research exists on this topic. This thesis fills that gap through empirical analysis using econometric methods.

## Research Questions & Hypotheses

### Hypothesis 1
**There is a positive relationship between the number of TikTok posts featuring a song and its streaming numbers on Spotify.**

TikTok, as a platform built on User Generated Content (UGC) with music accompaniment, creates massive exposure for songs. Following Kretschmer & Peukert (2020), who found that YouTube's promotional effect works regardless of whether content is official or user-generated, TikTok's UGC model should similarly drive music popularity.

### Hypothesis 2  
**There is a positive relationship between an artist's TikTok follower count and their song streams on Spotify.**

Following Mourelatos & Mourelatos (2022), who demonstrated that DJs with TikTok accounts experienced increased Spotify streams, this hypothesis examines whether user migration between platforms occurs more broadly across music genres.

## Methodology

### Data
- **Source**: Chartmetric platform statistics
- **Collection date**: January 11, 2023
- **Sample size**: 3,183 observations
- **Variables**:
  - Spotify streams (dependent variable)
  - TikTok posts featuring the song
  - Artist followers on TikTok and Spotify
  - Weeks since release
  - Song duration (seconds)

### Statistical Approach
**Method of Moments (MM) estimation** was employed to analyze the relationship between TikTok activity and Spotify popularity. Natural logarithm transformation was applied to variables with large value dispersions.

**Model specification**:
```
ln(Spotify_Streams) = β₀ + β₁(Weeks) + β₂(Duration) + β₃ln(TikTok_Posts) + β₄ln(TikTok_Followers) + β₅ln(Spotify_Followers)
```

**System of equations solved**:
```
R1: Σ[y - β₀ - β₁x₁ - β₂x₂ - β₃x₃ - β₄x₄ - β₅x₅] = 0
R2: Σ[x₁(y - β₀ - β₁x₁ - β₂x₂ - β₃x₃ - β₄x₄ - β₅x₅)] = 0
...
R6: Σ[x₅(y - β₀ - β₁x₁ - β₂x₂ - β₃x₃ - β₄x₄ - β₅x₅)] = 0
```

## Key Findings

### Hypothesis 1: ✅ CONFIRMED
- **1% increase in TikTok posts → 0.16% increase in Spotify streams**
- User Generated Content serves as an effective promotional channel, comparable to official content
- Statistical significance: p < 0.05

### Hypothesis 2: ✅ CONFIRMED  
- **1% increase in TikTok followers → 0.022% increase in Spotify streams**
- Effect is smaller than expected, possibly due to:
  - TikTok's relatively recent emergence in music promotion
  - Many artists lacking official TikTok presence
  - TikTok's unique algorithm structure differs from traditional social media
- Statistical significance: p < 0.05

### Additional Findings
- **Negative relationship between song duration and Spotify streams**
- Tested whether β₂ = -1 (perfect inverse relationship)
- Result: β₂ ≠ -1 (test statistic = 2102.911)
- Suggests the "attention economy" effect is present but not as severe as hypothesized

## Implications

1. **Platform Migration**: Evidence suggests users do migrate between platforms based on music discovery
2. **Promotional Value**: TikTok serves as a powerful promotional channel for music
3. **Marketing Strategy**: Artists and labels should consider TikTok as part of integrated digital marketing
4. **Future Research**: As TikTok matures, these effects may strengthen significantly

## Tools & Technologies

- **R** for statistical analysis
- **Method of Moments** for parameter estimation  
- Comparison with **OLS (Ordinary Least Squares)** for validation
- Libraries: `rootSolve` for solving system of equations

## Academic Context

- **Institution**: University of Warsaw, Faculty of Economic Sciences
- **Program**: IT & Econometrics / Economics & Informatics (dual degree)
- **Thesis Advisor**: Dr. Rafał Woźniak, Department of Statistics and Econometrics
- **Completion**: December 2023


