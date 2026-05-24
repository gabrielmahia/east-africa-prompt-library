# Environment Prompts — Drought, Water, Flood Risk

> Adapted from 1337 Use Cases for ChatGPT (Section 6.17: Environmental Studies, Section 11: Environmental Science)
> East African context: Kenya drought monitoring (NDMA), water stress (WRMA), flood risk mapping

---

## 6.17.1 Environmental Impact Assessment

**General prompt:**
"What is the environmental impact of [activity] on [ecosystem]?"

**Formula:**
"Assess the environmental impact of [human activity] on [specific ecosystem/resource] in [location], focusing on [water/soil/biodiversity/climate] effects over [timeframe]."

**East Africa examples:**
- "Assess the environmental impact of artisanal gold mining on the Migori River ecosystem in Western Kenya, focusing on water quality and fish populations over the next 5 years."
- "What is the environmental impact of charcoal burning on the Mau Forest in Kenya? Focus on water catchment effects and how this relates to drought risk in the Rift Valley."
- "Analyze the downstream effects of sand harvesting from the Tana River on delta ecosystems and fishing communities."

---

## 11.1.3 Drought Monitoring and Early Warning

**General prompt:**
"What are the early warning signs of drought in [region]?"

**Formula:**
"Analyze [rainfall/NDVI/water level] data for [county/region] in Kenya over the past [timeframe]. Identify [drought onset indicators/water stress trends/pasture conditions] and recommend [early warning actions/coping strategies]."

**East Africa examples:**
- "Analyze rainfall anomalies for Turkana County over the past 6 months. Identify drought onset indicators and recommend immediate humanitarian response priorities."
- "The water level at Masinga Dam has dropped 15% in 3 weeks. What does this mean for downstream agricultural water allocation in Tana River County?"
- "Classify water stress severity for each of Kenya's 47 counties based on NDMA drought phase data. Return results as a ranked table."

**wapimaji-mcp integration:**
```
Get current water stress index for [county_name] county.
Return: stress_level (low/moderate/high/critical), 
        latest_rainfall_anomaly_mm, 
        drought_phase (NDMA classification),
        recommended_response_actions
```

---

## 11.1.4 Environmental Impact Report

**General prompt:**
"Generate an environmental impact report for [project]."

**Formula:**
"Generate a structured environmental impact report for [project type] in [location, Kenya], covering: baseline conditions, predicted impacts on [water/biodiversity/communities], mitigation measures, and monitoring framework."

**East Africa examples:**
- "Generate an environmental impact report for a 50MW solar farm proposed for Marsabit County, Kenya. Cover: baseline semi-arid ecosystem conditions, impacts on pastoralist land use, water source proximity, and community benefit-sharing framework."
- "Environmental impact report for a new road through Arabuko-Sokoke Forest, Kilifi County. Focus on biodiversity loss, carbon sequestration impacts, and alternative routing options."

---

## 11.2 Land Use Planning

**General prompt:**
"How should land in [region] be allocated to balance agriculture, conservation, and settlement?"

**Formula:**
"Analyze land use conflicts in [location] between [use type 1] and [use type 2]. Recommend a spatial planning framework that [protects/balances/prioritizes] [goal] for [community type]."

**East Africa examples:**
- "Analyze land use conflicts in Laikipia County between large-scale ranches, small-scale farmers, and pastoralists. Recommend a conflict resolution framework."
- "How should riparian buffer zones be defined along the Athi River in Machakos County to protect both water quality and smallholder irrigation access?"

---

## kenya-3d Blender Visualization Prompts

For use with [kenya-3d](https://github.com/gabrielmahia/kenya-3d) via Claude Code + Blender MCP:

```
Run blender_scripts/county_bars.py with data/kenya_counties.json.
Color bars by water_stress field using:
  green = low stress (< 0.3)
  yellow = moderate (0.3-0.6)  
  red = high (0.6-0.8)
  dark red = critical (> 0.8)
Add a camera pointing at the full scene and render a preview PNG.
```

```
Generate a terrain mesh for Kenya's drought severity zones.
Use elevation data from data/kenya_counties.json (lat/lon centroids).
Extrude height proportional to drought_severity.
Apply a heatmap material: blue=low, red=critical.
```

```
Create a water stress map for Kenya's 47 counties.
Position county labels at their centroid coordinates.
Size each county marker proportional to population at risk.
Render from top-down orthographic view.
```
