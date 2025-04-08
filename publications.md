---
layout: page
permalink: /publications/index.html
title: Publications
---
<style>
/* === 纵向图片优化版 === */
.img-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); /* 缩小最小列宽 */
    gap: 1rem;
    margin: 1.5rem -0.8rem; /* 负边距补偿 */
}

.img-grid img {
    width: 100%;
    height: 320px; /* 增加高度适应竖图 */
    object-fit: contain; /* 改为contain完整显示 */
    object-position: center top; /* 顶部对齐 */
    border-radius: 6px;
    background: #fff; /* 添加白色背景 */
    box-shadow: 0 2px 8px rgba(0,0,0,0.12);
    padding: 4px; /* 留白 */
}

/* 创建竖图专用类 */
.img-grid.vertical {
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
}
.img-grid.vertical img {
    height: 280px;
    object-position: contain;
}

/* 响应式调整 */
@media (max-width: 768px) {
    .img-grid {
        margin: 1rem -0.5rem;
    }
    .img-grid img {
        height: 280px;
    }
}
</style>

(†: equal contribution, ~: corresponding author)

## Working Paper

None

<br>
---

## Conference Paper

- [Optimization Analysis on Seismic Mitigation of Building Foundation in Coastal Area](https://iopscience.iop.org/article/10.1088/1742-6596/2386/1/012055)<br>**Zongheng Li**<br>The International Conference on Computing Innovation and Applied Physics ([CONF-CIAP 2022](https://2022.confciap.org/)). August, 2022.

<br>


---

## Early Project

- Big data processing on relationship between the number of earthquakes and the elevation using an earthquake catalog containing 25,000 events with a magnitude >5.0 since year 2007  
  *Python for Graduate Research course project*  
  **Zongheng Li** (Advised by: [Mingming Li](https://search.asu.edu/profile/1558323))  
  Arizona State University, April 2024
  <div class="img-grid vertical">
    <img src="/images/ses494personal.jpg">
  </div>
%%{init: {'theme': 'neutral', 'themeVariables': { 'primaryColor': '#f5f5f5'}}}%%
flowchart TD
    A[Import numpy/pandas] --> B[Load Large_Eq.csv]
    B --> C[Process coordinates]
    C -->|Round to integer| D[Create LL_csv]
    D --> E{Longitude check}
    E -->|lon < 0| F[West data (W_LL_csv)]
    E -->|lon > 0| G[East data (E_LL_csv)]
    E -->|lon == 0| H[Prime Meridian (PM_LL_csv)]
    
    I[Load topo.dat] --> J{Longitude split}
    J -->|lon < 180| K[East terrain (E_LL_dat)]
    J -->|lon >= 180| L[West terrain (W_LL_dat)]
    
    F --> M[Adjust West longitude (+360)]
    M --> N[Merge West data]
    G --> O[Merge East data]
    H --> P[Merge PM data]
    
    N & O & P --> Q[Combine datasets]
    Q --> R[Calculate elevation intervals]
    R --> S[Plot histogram]

- Comparative Analysis of Geophysical Characteristics of Major Regions in the Phoenix Metropolitan Area  
  *Geophysics course design*  
  **Zongheng Li** (Advised by: [Edward Garnero](https://search.asu.edu/profile/216280))  
  Arizona State University, December 2024
  <div class="img-grid vertical">
    <img src="/images/Aeromagnetic2.jpg">
    <img src="/images/Bouguer2.jpg">
    <img src="/images/EQstatistics.jpg">
  </div>
*All data used in this research were obtained from USGS

- Simulation of Sub-Plinian Eruption of La Fossa Cone   
  *Geohazards of Mediterranean course design.*  
  **Zongheng Li** (Advised by: [Amanda Clarke](https://search.asu.edu/profile/499877))  
  Sicily, Italy, June 2024
  
  <div class="img-grid vertical">
    <img src="/images/ash.jpg">
    <img src="/images/pumice.jpg">
  </div>
*Simulated diffusion path of ash and pumice， respectively.

---

## Degree Thesis

None

<br>