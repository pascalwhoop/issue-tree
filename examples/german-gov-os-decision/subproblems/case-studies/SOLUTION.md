# Solution: Government OS Migration Case Studies

## Answer

Based on extensive analysis of government OS migrations worldwide, particularly in Europe, the evidence shows that **Linux migrations can succeed at large scale when properly planned and politically supported**, but they also demonstrate that **political commitment, organizational readiness, and gradual implementation are more critical than technical factors alone**.

The case studies reveal a clear pattern: successful migrations (French Gendarmerie, Schleswig-Holstein, Austria) share common characteristics of sustained political support, phased implementation, and user engagement, while failures (Munich's LiMux reversal) stem primarily from organizational dysfunction and political changes rather than technical limitations of Linux itself.

## Major Case Studies

### 1. Munich's LiMux Project (Germany) - The Cautionary Tale

**Timeline**: 2004-2017 (migration), 2017-2020 (reversal), 2020+ (renewed open source commitment)

**Scale**: 15,000 PCs, with 12,600 successfully migrated by 2012

**Outcome**: Migration completed successfully with €11.7 million in savings, but reversed in 2017 due to political changes. In 2020, new administration reinstated open source preference and created an Open Source Program Office in 2024.

**What Happened**:
- Initial migration (2004-2012) was technically successful
- Saved €11.7 million in licensing costs
- 2017 SPD-CSU coalition decided to revert to Windows 10, citing user dissatisfaction
- Reversal cost estimated at €86-100 million (€50m for hardware/licensing + €50m for migration)
- Mayor Dieter Reiter questioned LiMux strategy immediately upon taking office
- Microsoft announced moving German headquarters to Munich in 2013, relocating in 2016

**Key Failure Factors**:

*Political*:
- Decision was "not made on the basis of facts" according to critics
- New mayor actively opposed LiMux from the start
- Accenture (a Microsoft partner) was hired to analyze IT infrastructure
- Leadership changes brought different technology priorities
- Microsoft's physical presence in Munich created political pressure

*Organizational*:
- **15 different OS versions** were in use across departments (fundamental lack of standardization)
- No clear structures and responsibilities for IT governance
- Departments could block updates if inconvenient
- IT department lacked processes for proper standardization
- Poor change management - technical rollout outpaced organizational adaptation
- Inadequate training left employees frustrated

*Technical*:
- About 400 of 800 required programs didn't run on Linux
- Compatibility issues with OpenOffice/LibreOffice when collaborating with Windows organizations
- Some public-sector tools were Windows-only
- However, most technical issues were solvable - they weren't the primary cause

**Critical Insight**: A 2018 documentary by Investigate Europe revealed that the majority of city workers were actually satisfied with the operating system. The reversal was politically motivated rather than technically necessary.

**2020+ Update**: New coalition government emphasized open standards and FOSS, created five-point open-source plan and Open Source Program Office. This demonstrates that the software itself wasn't the problem - political will was.

### 2. French Gendarmerie (GendBuntu) - The Gold Standard Success

**Timeline**: 2004-present (ongoing success story)

**Scale**: 103,164 workstations as of June 2024 (97% of all Gendarmerie workstations)

**Outcome**: Highly successful, sustained over 20 years

**Implementation Phases**:
- 2004-2005: Replaced Microsoft Office with OpenOffice.org (20,000 copies initially, 90,000 total by 2005)
- 2006: Migrated 70,000 workstations to Firefox and Thunderbird
- 2008: Began GendBuntu (Ubuntu-based custom distribution) migration
- 2013: 37,000+ desktops converted
- 2023-2024: Upgraded from GendBuntu 20.04 to 22.04 (62,000 stations)
- 2024: 103,164 workstations running GendBuntu

**Financial Impact**: 40% reduction in total cost of ownership compared to Windows

**Success Factors**:
- Gradual, phased approach over many years
- Custom distribution tailored to organizational needs
- Started with applications (OpenOffice, Firefox) before OS migration
- Strong, sustained political support across multiple administrations
- Clear organizational commitment to open source
- Built internal expertise over time
- Maintained consistency despite government changes

**Why It Worked**: The Gendarmerie approached this as a long-term strategic initiative rather than a short-term project. By 2024, they've maintained Linux for 16+ years on over 100,000 machines - this is not a pilot program, it's a proven production environment.

### 3. Schleswig-Holstein (Germany) - The Modern Success in Progress

**Timeline**: 2021-present (ongoing)

**Scale**: 30,000 PCs in state government

**Status**: Ahead of schedule as of December 2025 - nearly 80% complete outside tax administration

**Implementation Strategy**:
- April 2024: Official approval for migration
- LibreOffice provided alongside Microsoft Office during transition
- August 2024: ODF became official document standard
- October 2025: Target for LibreOffice to be sole standard on 70% of workstations
- Microsoft Office remains accessible until October 2025

**Financial Impact**:
- Saves over €15 million annually in license costs (from 2026 onward)
- One-time €9 million investment for 2026 to complete migration

**Motivations**:
- Digital sovereignty: "A digital pioneer region and the first state to introduce a digitally sovereign IT workplace"
- Data security concerns, especially data flowing to other countries
- Independence from vendor lock-in
- Cost reduction

**Success Factors**:
- Clear political commitment from digital leadership
- Phased, structured plan
- Dual-installation strategy (both Office suites during transition)
- Standardization on ODF as official format
- Focused on sovereignty as primary goal, not just cost
- Learning from Munich's mistakes

**Why It's Working**: Unlike Munich, Schleswig-Holstein has consistent political support, clear timelines, proper standardization from the start, and a sovereignty-first rather than cost-first motivation.

### 4. Barcelona (Spain) - Mixed Progress

**Timeline**: 2017-2018 initiative, limited recent updates

**Scale**: Planned for city administration, pilot of 1,000 Ubuntu desktops

**Strategy**:
- Replace user applications with open-source alternatives first
- Windows would be last remaining proprietary software, then replaced
- Outlook/Exchange → Open-Xchange
- Internet Explorer/Office → Firefox/LibreOffice
- Ubuntu as likely distribution

**Status**: Strong initial announcements in 2017-2018, but limited verifiable progress reports for 2023-2025. Mentioned in passing as part of European open-source trend but without specific completion metrics.

**Assessment**: Unclear outcome - appears to have lost momentum or faced implementation challenges. Lack of recent updates suggests either quiet continuation or stalled progress.

### 5. United Kingdom - Policy-Driven Approach

**Timeline**: 2002-present (evolving policy)

**Approach**: Policy-based rather than mandated migration

**Policy Evolution**:
- 2002: Open source should be considered equally with proprietary solutions
- 2013: Government mandated "preference" for open source
- 2024: Digital, Data and Technology Playbook updated with requirement: "Software should be open-source and designed to allow access in a platform-agnostic way"

**Scale of Impact**: UK public sector spends £46 billion on digital annually, so policy has wide-ranging effects

**Implementation**: "Comply or explain" basis for central government, "good practice" for wider public sector

**Key Philosophy**:
- Platform-agnostic approaches
- Open standards to avoid vendor lock-in
- Open source should be used "whenever possible"
- Evolved from equal consideration to prescriptive requirement

**Assessment**: UK takes a pragmatic, policy-driven approach rather than wholesale migration. Emphasizes openness and standards over specific OS mandates.

### 6. Italy - Strategic Framework Approach

**Timeline**: 2013-present with updated 2024-2026 strategy

**Scale**: Whole public administration (targets for 2024-2026)

**Targets** (from Three-Year Plan 2024-2026):
- End 2024: 100 PAs releasing open source, 2,600 reusing
- End 2025: 125 PAs releasing open source, 2,800 reusing
- End 2026: 150 PAs releasing open source, 3,000 reusing

**Notable Successes**:
- Ministry of Defence: LibreOffice and ODF on 150,000 PCs
- Created Competence Centre for Reuse and Open Source (CCROS)
- Developers Italia platform for sharing open source solutions

**Approach**:
- Focus on preventing vendor lock-in
- Promote reuse of solutions across administrations
- Build communities around shared solutions
- Efficiency and transparency goals

**Assessment**: Strategic, coordinated approach across multiple government levels. Focus on sharing and reuse rather than isolated migrations.

### 7. Austria - Recent Military Success

**Timeline**: Completed 2025

**Scale**: 16,000 military systems

**Outcome**: Successful migration to LibreOffice on Linux desktops

**Significance**: One of Europe's largest open-source deployments. Military context demonstrates that even security-sensitive environments can successfully adopt open source.

### 8. Denmark - In Progress

**Timeline**: June-November 2025

**Scale**: Ministry of Digital Affairs

**Implementation**: Half of staff by August 2025, full migration by autumn 2025

**Motivation**: Digital Minister Caroline Stage Olsen: "We must never make ourselves so dependent on so few that we can no longer act freely." Too much public digital infrastructure tied to very few foreign suppliers.

**Status**: Actively in progress as of 2025

### 9. Other Notable Cases

**Toulouse, France**: Migrated 90% of desktops to LibreOffice, saved approximately €1.8 million over three years

**11 French Ministries**: Installed LibreOffice on 500,000 workstations

**South Tyrol**: Sustained open-source success (limited details available)

**Norway**: Various municipalities with successful transitions

**Valencia, Spain**: Early Linux adopter (limited recent information)

## Comparative Analysis: Success vs. Failure Patterns

### Successful Migrations Share These Characteristics:

1. **Sustained Political Support**
   - Support survives leadership changes (French Gendarmerie: 20+ years)
   - Leaders articulate clear reasons beyond just cost (sovereignty, independence)
   - Digital sovereignty as primary motivation (Schleswig-Holstein, Denmark)

2. **Gradual, Phased Implementation**
   - Applications first, then OS (French Gendarmerie)
   - Dual installations during transition (Schleswig-Holstein)
   - Time measured in years, not months
   - Pilot programs to gather feedback before full rollout

3. **Organizational Readiness**
   - Standardization from the start
   - Clear governance structures
   - Adequate training and support
   - User engagement and feedback mechanisms

4. **Strategic Rather Than Tactical Motivation**
   - Digital sovereignty and independence
   - Long-term control and security
   - Cost savings as benefit, not primary driver
   - Avoiding vendor lock-in

5. **Technical Support Infrastructure**
   - Rigorous, personalized technical support
   - Constant dialogue with users
   - Internal expertise development
   - Community engagement

### Failed or Stalled Migrations Share These Problems:

1. **Political Instability**
   - Leadership changes reverse decisions (Munich)
   - Vendor lobbying influences policy
   - Lack of cross-party consensus
   - Short-term thinking

2. **Organizational Dysfunction**
   - No standardization (Munich: 15 different OS versions)
   - Unclear responsibilities and structures
   - Departments can block or ignore changes
   - Change management lags technical rollout

3. **Poor User Experience**
   - Inadequate training
   - Compatibility issues not addressed
   - Windows-only tools without alternatives
   - Support infrastructure inadequate

4. **Cost-First Motivation**
   - When cost savings don't materialize quickly, support evaporates
   - Easy to justify reversal on cost grounds
   - Ignores long-term strategic benefits

## Key Lessons Learned for German Government Context

### 1. Political Commitment is Paramount

Munich's reversal wasn't a technical failure - it was political. The software worked; the political will didn't. Any German federal migration must have:
- Cross-party support or constitutional protection
- Clear articulation of sovereignty goals
- Insulation from vendor lobbying
- Long-term commitment beyond electoral cycles

### 2. Organizational Factors Trump Technical Factors

Munich's Accenture report found "primarily organisational issues at the root of the problems." Technical challenges (compatibility, Windows-only software) are solvable. Organizational dysfunction (lack of standardization, unclear governance, poor change management) is harder to fix and will undermine any platform.

**Critical**: Standardization and governance must precede OS choice. Munich failed because they had 15 different OS versions - that's a management failure, not a Linux failure.

### 3. Gradual Beats Big Bang

French Gendarmerie's 20-year success started with applications (OpenOffice, Firefox) before OS migration. This approach:
- Builds user comfort with open source gradually
- Develops internal expertise over time
- Identifies compatibility issues while Windows is still present
- Demonstrates value before full commitment

### 4. Sovereignty Beats Cost as Motivation

Schleswig-Holstein leads with sovereignty; cost savings are a welcome benefit. Denmark emphasizes independence from foreign suppliers. When cost is the primary driver and savings don't materialize immediately, the project becomes vulnerable.

**Sovereignty provides resilient justification** that survives budget cycles and political changes.

### 5. Training and Support are Not Optional

Munich's users were frustrated partly because training was inadequate. Successful migrations invest heavily in:
- Comprehensive user training programs
- Responsive technical support
- Clear documentation
- Ongoing user engagement

The French Gendarmerie emphasized "rigorous and personalized technical support" as essential.

### 6. Compatibility Must Be Proactively Addressed

Windows-only software and format compatibility issues repeatedly emerge as challenges. Solutions:
- Identify Windows-only tools early and find/build alternatives
- Standardize on ODF early (Schleswig-Holstein made it official in August 2024)
- Maintain Windows compatibility during transition
- Work with vendors to support Linux versions

### 7. Learn from Munich's Mistakes

Munich provides a roadmap of what NOT to do:
- Don't allow 15 different OS versions (standardize first)
- Don't let departments block updates
- Don't skip governance and change management
- Don't hire Microsoft partners to evaluate migration
- Don't start without sustained political commitment
- Don't ignore organizational culture

Munich's 2020 reversal of the reversal (renewed open source commitment) suggests the original technical approach was sound.

### 8. The "Human Factor" is Critical

Best practices emphasize:
- Constant dialogue with users
- Importance of training
- Addressing resistance proactively
- Managing change, not just technology

Technology transitions fail when treated as purely technical projects rather than organizational change initiatives.

### 9. Scale is Achievable

Multiple governments have successfully migrated at scale:
- French Gendarmerie: 103,164 workstations
- Italy Ministry of Defence: 150,000 PCs
- 11 French Ministries: 500,000 workstations
- Austria: 16,000 military systems
- Schleswig-Holstein: 30,000 PCs (in progress)

Large-scale migration is not a theoretical possibility - it's a demonstrated reality.

### 10. Context Matters

What works for France may not work for Germany. Key contextual differences to consider:
- Existing Microsoft dependencies and contracts
- Federation vs. centralization (Germany's federal structure)
- Political culture and stability
- IT industry relationships
- EU policy alignment
- Existing technical debt

## Actionable Recommendations for German Government

Based on these case studies, a German federal Linux migration should:

1. **Lead with sovereignty, not cost** - Frame as digital independence and security, with cost savings as a benefit

2. **Secure multi-party political commitment** - Get buy-in across the political spectrum or establish through policy that transcends electoral cycles

3. **Standardize first, migrate second** - Fix organizational and governance issues before changing platforms. One standardized version, not 15 variants.

4. **Start with applications, not OS** - Migrate to LibreOffice, Firefox, Thunderbird while on Windows. Build comfort before switching OS.

5. **Pilot extensively** - Test in selected departments, gather feedback, build internal case studies before full rollout

6. **Plan for 5-10 years, not 2-3** - French Gendarmerie's success is built on 20 years of sustained effort. This is a strategic transformation, not a quick project.

7. **Invest heavily in training and support** - Budget for comprehensive training programs and responsive technical support from day one

8. **Address compatibility proactively** - Identify Windows-only tools now, develop alternatives, standardize on ODF early

9. **Build internal expertise** - Develop German public sector Linux expertise rather than depending on external vendors

10. **Learn from Schleswig-Holstein** - Watch Germany's own state-level migration closely. It's the most contextually relevant case study.

11. **Establish clear governance** - Define structures, responsibilities, processes for standardization and change management

12. **Communicate constantly** - Maintain ongoing dialogue with users, address concerns early, demonstrate value continuously

## Confidence Assessment

**High Confidence** in the core findings:
- Multiple well-documented case studies available
- Clear patterns emerge across successful vs. failed migrations
- Recent cases (2024-2025) provide up-to-date evidence
- Munich case extensively analyzed from multiple perspectives
- French Gendarmerie represents 20+ years of proven success

**Medium Confidence** in some specifics:
- Barcelona's current status unclear (limited recent reporting)
- Some cases lack detailed cost breakdowns
- Long-term sustainability of recent migrations (Schleswig-Holstein, Denmark) yet to be proven over decades

## Caveats and Limitations

1. **Survivorship bias**: Successful migrations are more heavily documented and publicized than quiet failures

2. **Timeframes differ**: Comparing a 20-year success (French Gendarmerie) with a 2024 initiative (Schleswig-Holstein) has limitations

3. **Context varies**: Military organizations (French Gendarmerie, Austrian military) have different constraints than civilian administrations

4. **Political environments differ**: What's politically feasible in France or Schleswig-Holstein may face different challenges at German federal level

5. **Technology evolves**: Cases from 2004-2010 may not fully reflect 2026 technical landscape

6. **Incomplete data**: Some migrations (Barcelona, Valencia) lack recent comprehensive updates

7. **Munich controversy**: The Munich reversal remains politically contested, with different stakeholders providing conflicting narratives

8. **Scale differences**: Federal German government migration would be larger than most documented cases

9. **Federation complexity**: Germany's federal structure adds coordination complexity not present in unitary governments or single states

## Bottom Line for German Government Decision

The case studies provide clear evidence that:

**Linux migrations CAN succeed at large scale** - this is proven beyond doubt (French Gendarmerie: 103,000+ workstations for 20+ years)

**Technical factors are NOT the primary determinant** - organizational readiness, political support, and change management matter more than OS capabilities

**Sovereignty provides the most resilient justification** - cost-based arguments are vulnerable to reversal when savings are disputed

**Germany has a relevant local success to learn from** - Schleswig-Holstein's ongoing migration provides a contextually similar example

**Munich's failure was organizational and political, not technical** - the reversal of the reversal in 2020 suggests the original approach was sound

For the parent question (should German government use Linux or Windows?), these case studies suggest that **Linux is technically viable and can deliver strategic benefits (sovereignty, cost savings, security)**, but **success depends primarily on political commitment, organizational readiness, and implementation approach rather than inherent OS capabilities**.

The choice should be driven by strategic goals (sovereignty, independence, security) rather than purely technical or cost considerations. If Germany values digital sovereignty and is willing to commit to proper organizational preparation and sustained political support, Linux is demonstrably viable at scale. If political support is uncertain or organizational issues are unresolved, the OS choice may be less important than fixing governance first.

## Sources

### Munich LiMux Project
- [LiMux - Wikipedia](https://en.wikipedia.org/wiki/LiMux)
- [Munich's Long History with Open Source in Public Administration | Interoperable Europe Portal](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/document/munichs-long-history-open-source-public-administration)
- [And we return to Munich's migration back to Windows – it's going to cost what now?! €100m! • The Register](https://www.theregister.com/2018/01/04/munich_linux_costs_ownership/)
- [Munich: A Case Study in Poor Project Management - UK Business Advisors](https://ukba.co.uk/munich-a-case-study-in-poor-project-management/)
- [Munich Is Ditching Linux For Purely Political Reasons](https://itsfoss.com/munich-linux-failure/)
- [The rise and fall of Limux [LWN.net]](https://lwn.net/Articles/737818/)
- [What happened in Munich - FSFE](https://fsfe.org/news/2017/news-20170301-01)
- [Munich's Linux Experiment: What Government Can Learn from Open Source - Studio{Linux}](https://studiolinux.com/posts/the-munich-linux-saga/)

### French Gendarmerie (GendBuntu)
- [Governments Around the World Are Switching to Linux](https://lowtechlinux.com/2025/07/07/governments-around-the-world-are-switching-to-linux/)
- [France quietly deployed 100,000+ Linux machines in their police force - GendBuntu is a silent EU tech success story](https://piefed.social/post/953245)
- [GendBuntu - Wikipedia](https://en.wikipedia.org/wiki/GendBuntu)
- [Towards the freedom of the OS: French Gendarmerie goes Ubuntu | Interoperable Europe Portal](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/document/towards-freedom-os-french-gendarmerie-goes-ubuntu)
- [Case Study: French Gendarmerie Moves to Ubuntu » Linux Magazine](https://www.linux-magazine.com/Online/Blogs/ROSE-Blog-Rikki-s-Open-Source-Exchange/Case-Study-French-Gendarmerie-Moves-to-Ubuntu)

### Barcelona
- [City of Barcelona Kicks Out Microsoft in Favor of Linux and Open Source](https://itsfoss.com/barcelona-open-source/)
- [City of Barcelona Dumps Windows For Linux and Open Source Software - Slashdot](https://linux.slashdot.org/story/18/01/15/0415219/city-of-barcelona-dumps-windows-for-linux-and-open-source-software)
- [Barcelona abandons Windows and Office, goes with Linux instead | TechRadar](https://www.techradar.com/news/barcelona-abandons-windows-and-office-goes-with-linux-instead)
- [A Search for Digital Sovereignty: EU Governments Shift from Microsoft to Linux & LibreOffice](https://www.2-data.com/knowledge-hub/a-search-for-digital-sovereignty-eu-governments-shift-from-microsoft-to-linux-libreoffice)

### United Kingdom
- [Open Source guidance - GOV.UK](https://www.gov.uk/government/publications/open-source-guidance)
- [UK government prescribes open source in public procurement | Interoperable Europe Portal](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/news/uk-government-prescribes-open-source-public-procurement)
- [UK Government Mandates 'Preference' For Open Source - Slashdot](https://news.slashdot.org/story/13/03/16/1642254/uk-government-mandates-preference-for-open-source)
- [Government mandates 'preference' for open source | Computer Weekly](https://www.computerweekly.com/news/2240179643/Government-mandates-preference-for-open-source)

### Italy
- [Italy 2025 Country Report | Interoperable Europe Portal](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/news/italy-2025-country-report)
- [Italy's public service digital strategy updated | Interoperable Europe Portal](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/news/italys-public-service-digital-strategy-updated)
- [A Search for Digital Sovereignty: EU Governments Shift from Microsoft to Linux & LibreOffice](https://www.2-data.com/knowledge-hub/a-search-for-digital-sovereignty-eu-governments-shift-from-microsoft-to-linux-libreoffice)

### Schleswig-Holstein
- [German state moving 30000 PCs to LibreOffice](https://blog.documentfoundation.org/blog/2024/04/04/german-state-moving-30000-pcs-to-libreoffice/)
- [German State Schleswig-Holstein Migrates 30,000 PCs To LibreOffice - OSTechNix](https://ostechnix.com/german-state-schleswig-holstein-migrates-30000-pcs-to-libreoffice/)
- [Updates on Schleswig-Holstein moving to LibreOffice - The Document Foundation Blog](https://blog.documentfoundation.org/blog/2025/03/13/updates-on-schleswig-holstein-moving-to-libreoffice/)
- [German state switches to LibreOffice, promises Windows move • The Register](https://www.theregister.com/2024/04/04/germanys_northernmost_state_ditches_windows/)
- [Hurray! This German State Decides to Save €15 Million Each Year By Kicking Out Microsoft for Open Source](https://itsfoss.com/news/german-state-ditch-microsoft/)

### European Government Migrations - General
- [A Search for Digital Sovereignty: EU Governments Shift from Microsoft to Linux & LibreOffice](https://www.2-data.com/knowledge-hub/a-search-for-digital-sovereignty-eu-governments-shift-from-microsoft-to-linux-libreoffice)
- [Another victory for Linux: The reasons why a European government abandoned Microsoft](https://www.linuxencaja.net/en/another-european-government-is-abandoning-microsoft-in-favor-of-linux-here-are-the-reasons-why/)
- [Governments Around the World Are Switching to Linux](https://lowtechlinux.com/2025/07/07/governments-around-the-world-are-switching-to-linux/)
- [Schleswig-Holstein Adopts Linux Open Source Software for Data Sovereignty](https://linuxsecurity.com/news/government/schleswig-holsteins-bold-move-to-open-source)
- [Open Source Maturity in Europe: Milestones, Opportunities, and Pathways in 2024](https://www.linuxfoundation.org/blog/open-source-maturity-in-europe-milestones-opportunities-and-pathways-in-2024)

### Best Practices and Success Factors
- [A Search for Digital Sovereignty: EU Governments Shift from Microsoft to Linux & LibreOffice](https://www.2-data.com/knowledge-hub/a-search-for-digital-sovereignty-eu-governments-shift-from-microsoft-to-linux-libreoffice)
- [Governments Around the World Are Switching to Linux](https://lowtechlinux.com/2025/07/07/governments-around-the-world-are-switching-to-linux/)
- [Another victory for Linux: The reasons why a European government abandoned Microsoft](https://www.linuxencaja.net/en/another-european-government-is-abandoning-microsoft-in-favor-of-linux-here-are-the-reasons-why/)
