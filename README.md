# Work In Progress &mdash; User Experience NFRs for Web Application Projects

As a design professional you may find yourself being asked to contribute Usability or Performance NFRs for a Web or Application project. There are a lot of different resources that have recommendations for different properties and metrics can be used to quantify the experience of using a website or app, below is an attempt to collate them into a usable template you can customise to your specific requirements.

>**Nonfunctional Requirements** (NFRs) define system attributes such as security, reliability, performance, maintainability, scalability, and usability.  
> &mdash; https://www.scaledagileframework.com/nonfunctional-requirements

## Non Functional Requirements

### 🚀&nbsp;&nbsp;Page Speed Metrics
- https://web.dev/metrics/
- https://webpagetest.org/easy

|Item|Value|Notes|
|:--|--:|:--|
|First&nbsp;Contentful&nbsp;Paint&nbsp;(FCP)  | <1500ms ||
|Largest&nbsp;Contentful&nbsp;Paint&nbsp;(LCP)| <2000ms ||
|First&nbsp;Input&nbsp;Delay&nbsp;(FID)       |  <100ms ||
|Time&nbsp;To&nbsp;Interactive&nbsp;(TTI)     | <2500ms ||
|Total&nbsp;Blocking&nbsp;Time&nbsp;(TBT)     |  <300ms ||
|Cumulative&nbsp;Layout&nbsp;Shift&nbsp;(CLS) |    <0.1 ||

  
### 📱&nbsp;&nbsp;Browser/Device Support
- These values are based on our GA reporting or on Australian statistics, you should tailor these to your market.
- https://gs.statcounter.com/screen-resolution-stats/all/australia
- Can be tested with browserstack or similar.

|Item|Value|Notes|
|:--|:--|:--|
|Chrome                                                     |>=84||
|Safari                                                     |>=13||
|Samsung&nbsp;Internet                                      |>=11||
|Support&nbsp;TouchEvents&nbsp;on&nbsp;Event&nbsp;Handlers  |||
|Support Resolutions in Portrait and Landscape              |||
|Supported Desktop Resolutions (w/h)                        |<br><ul><li>3840x2160</li><li>1920x1080</li><li>1440x900</li><li>1366x768</li><li>1280x720</li></ul>||
|Supported Tablet Resolutions (w/h)                         |<br><ul><li>800x1280</li><li>768x1024</li></ul>||
|Supported Mobile Resolutions (w/h)                         |<br><ul><li>414x896/736</li><li>375x812/667</li><li>360x780/640</li></ul>||

  
### 🙋&nbsp;&nbsp;Accessibility
- https://wave.webaim.org/
- https://www.w3.org/TR/wai-aria-practices/

|Item|Value|Notes|
|:--|:--|:--|
|WCAG 2.0 AA Compliance                       |WAVE Accessibility Tool: 0 Errors 0 Warnings||
|Semantic HTML Elements w/ Meaningful Names   |
|ARIA Labeling                                |
|[Relative Font Sizing](#relative-font-sizing)|||
|All media descriptively titled               ||

<details><summary><strong style="font-size: 1.2em" id="relative-font-sizing">Relative Font Sizing</strong></summary>
<br>
<blockquote>A current accessibility recommendation is to use relative font sizes such as percentages or units of em instead of absolute sizes such as pixels or points. This allows text to be more easily resized appropriately across multiple devices and platforms.<br>
&mdash; EIT Accessibility Group, 
Pennsylvania State University</blockquote>
 <ul>
   <li>https://alistapart.com/article/relafont/</li>
   <li>https://css-tricks.com/accessible-font-sizing-explained/</li>
   <li>https://accessibility.psu.edu/fontsizehtml/</li>
</ul>
</details>

  
### ⌛&nbsp;&nbsp;Bandwidth
|Item|Value|Notes|
|:--|:--|:--|
|Images should be in the appropriate format for the content |
|Images served at the appropriate resolution for the device |
|Total Page Weight / App Bundle Size                        |<=5mb|
|Make use of local caching                                  |
|Download media on-demand, provide thumbnails and previews  |

  
### 🏃&nbsp;&nbsp;Usability & Performance
|Item|Value|Notes|
|:--|:--|:--|
|Animations at 60fps                            |||
|Process User Events                            | <50ms ||
|Visible Response to Events                     | <100ms||
|Responses typically over 1s should provide an indicator / warning |
|Responses typically over 10s should be performed in the background and not block other tasks|
|Consider Server Side Rendering to optimise the first load |
|Reduce Content shift by:<ul><li>Reserve Space for images and media by size or aspect ratio</li><li>Reserve space/provide minimum height for dynamically loaded content</li><li>Prefer CSS Grid for Layouts</li></ul>|||
