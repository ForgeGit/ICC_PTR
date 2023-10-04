# ICC_PTR

PTR data for the raid "The Icecrown Citadel" (ICC) - World of Warcraft: Wrath of the Lich King Classic (2023) 

# Table of Contents 📜

1. [3rd Round of PTR](#3rd-round-of-ptr-testing)<br>
    1.1. [Additional Class Data](#3rd-round-class-data-25-man-heroic-only)<br>
2. [2nd Round of PTR](#2nd-round-of-ptr-testing)<br>
3. [1st Round of PTR](#1st-round-of-ptr-testing)<br>
4. [Methodology and Data](#methodology)<br>
5. [Limitations](#limitations)<br>

## 3rd round of PTR testing

### 25 man HEROIC
<img src="_img/ICCPTR_3rdSession_v3_25mH.png"/>

### 10 man HEROIC
<img src="_img/ICCPTR_3rdSession_v3_10mH.png"/>

### 25 man NORMAL
<img src="_img/ICCPTR_3rdSession_v3_25mN.png"/>

### 10 man NORMAL
<img src="_img/ICCPTR_3rdSession_v3_10mN.png"/>

## 3rd round class data (25-man Heroic only)

The graphics above show the "overall distribution" for each CLASS.<br>
While the data is interesting, it is extremely limited. For this reason, I am adding the following graphics by spec to complement the previous ones.

<img src="_img/transition/plot1_tank_class.png"/><br>
<img src="_img/transition/plot1_heal_class.png"/><br>
<img src="_img/transition/plot3_DPS_class.png"/><br>
<img src="_img/transition/plot2_DPS_class.png"/>

If you want to see additional metrics for 25-man (and 10-man) heroic raid compositions, `D.A.R` has made a sheet where you can explore further:  

- 10-man heroic: https://docs.google.com/spreadsheets/d/1r7BOYqfgSsSLKJ3gaPwlqH4fpXG0t2Qr83BsVEl9QYg
- 25-man heroic: https://docs.google.com/spreadsheets/d/1ZEZnAQJECkhzISK1P1pfjIPBx6ssmomOwfBai3-PSN0

## 2nd round of PTR testing

<img src="_img/ICCPTR_2ndSession_v2_25m.png"/>

<img src="_img/ICCPTR_2ndSession_v2_10m.png"/>

## 1st round of PTR testing

<img src="_img/ICCPTR_1stSession.png"/>

## Methodology

All the data was collected using the Warcraft Logs Classic API v2 and processed with R v.4.2 (R Development Core Team).

Icecrown Citadel (ICC) raids were located in this zone: https://classic.warcraftlogs.com/zone/reports?zone=1020

All wipes with Lich King at 10% or less HP were considered as kills; wipes at 0% were excluded.

Duplicated encounters were excluded based on: "Encounter Name", "Difficulty", "Size", "Kill/Wipe", "Boss %", "Fight Length", and "Avg. ilvl"

<img src="_img/data_pipeline_3.jpg"/>

The raw data file in data table ("Excel") format can be found in this repo: 

- Round 1: https://github.com/ForgeGit/ICC_PTR/blob/main/raw_data/ICC_PTR_clean_Data_1stround_2023_09_21_h16_m11.csv
- Round 2: https://github.com/ForgeGit/ICC_PTR/blob/main/raw_data/ICC_PTR_clean_Data_2ndround_2023_09_21_h20_m04.csv
- Round 3: https://github.com/ForgeGit/ICC_PTR/blob/main/raw_data/ICC_PTR_clean_Data_3rdround_2023_09_30_h08_m13.csv

The file used for the graphics (which contains the same data as the links above), can be found in: https://github.com/ForgeGit/ICC_PTR/tree/main/raw_data/viz

## Limitations

a.k.a. Things to consider when interpreting this as "information"

- For the 1st round of PTR, Putricide was missing key mechanics from the encounter; as a result the number of wipes and kills are potentially off by a lot. 

- Similarly, Gunship has a couple kills wrongly flagged as "kills", which I haven't manually filtered.

- Heroic Lich King had some bugs which made it impossible to kill, allegedly.

General PTR limitations to consider:

- Not all logs are public. Given it is on the interest of some guilds to make their logs private on PTR due to the competitive nature of "progression" rewards (lumberjack rankings, in-game title, larping), this statistics are more biased towards a more casual playerbase. (I.E. less kills, more wipes, longer kill times).

- Not everyone has logs of their runs. Probably a minority, if you think most players are in a somewhat well-informed communities. Or it could be a great majority of players not logging their runs if you think most of the playerbase is "casual" and doesn't care about logging.

- PTR  means a portion of the players have either incomplete or scuffed UIs/macros/addons, making the overrall performance of the average player worse than what it actually is in live servers. Another group of the PTR players could also be testing specs and gear.

- Raids in general are mostly testing the content, sometimes wiping on purpose or doing quick pulls "just to see the boss". 

## Others

- The image used for the Open Graph Card comes from: https://www.zerochan.net/230963

## Other analysis and random stuff

- If you have questions, you can contact me on discord: https://discord.gg/wp55kqmyYG (Discord: Discfordge)

- Consider buying me a coffee? :) https://ko-fi.com/forge

- Check other things I have done here: https://github.com/ForgeGit?tab=repositories

## Changelog

- The data for the 1st round of PTR had some duplicated logs that were not "filtered" as explained in the Methodology section. I have adjusted the filter and this has resulted in less # of encounters. The change does not impact the overall results or interpretations of the graphic. The old version (Version 1) can now be found at: https://github.com/ForgeGit/ICC_PTR/tree/main/_img/old_v

## Others 2?

These are some Youtube videos/media in which the PTR data has been used, that I am aware of.

I do not necessarily support or agree with the statement in the videos or their authors. However, I appreciate them mentioning and giving it an use.

- Will Heroic Lich King be Cleared on Launch?
    - Shindigg
    - https://www.youtube.com/watch?v=9rC5LF-etoY

- Discover the Best Healers in Wotlk Phase 4 - Healers Tier List
    - NOHITJEROME
    - https://www.youtube.com/watch?v=MIO2kJxZ4Jo
    
If you know of any other platform/website/media in which my graphics have been used, let me know to spotlight them in here. 
