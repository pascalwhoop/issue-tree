# Solution: Application and Software Compatibility

## Answer

**Linux can provide functionally equivalent application-level capabilities to Windows for German government operations**, with the following key findings:

1. **Core productivity applications have mature, viable alternatives** on Linux (LibreOffice, Thunderbird, Firefox, Okular)
2. **File format compatibility is strong** with ODF as an international standard and good Microsoft Office format support
3. **Real-world German government deployments** (Schleswig-Holstein, Austria military) demonstrate viability at scale
4. **Specialized applications remain the primary challenge** - custom government software ("Fachverfahren") requires vendor cooperation or virtualization
5. **Training and change management** are more critical success factors than pure technical compatibility

## Evidence

### Core Productivity Applications

**Office Suites:**
- **Windows**: Microsoft Office (native, commercial)
- **Linux**: LibreOffice (native, open-source) with excellent ODF support and good Microsoft format compatibility
- **Compatibility**: LibreOffice supports .docx, .xlsx, .pptx read/write with ongoing improvements
- **Status**: Production-ready, as demonstrated by multiple large-scale government deployments

**Email and Collaboration:**
- Windows: Microsoft Outlook, Exchange Server
- Linux: Thunderbird (email client), Open-Xchange (Exchange replacement), Evolution
- Schleswig-Holstein explicitly replaced Outlook with Thunderbird and Exchange with Open-Xchange

**Web Browsers:**
- Firefox (native on both platforms)
- Chromium/Chrome (native on both)
- Edge (available on Linux as of 2020)
- Vivaldi and other Chromium-based browsers (cross-platform)

**PDF Tools:**
- Linux: Okular (KDE), Evince/Papers (GNOME), LibreOffice Draw (editing)
- Windows: Adobe Acrobat, Foxit Reader
- Both platforms support full PDF viewing, editing, and signing capabilities

## Real-World German Government Experience

### LiMux Munich (2006-2017)
**Outcome**: Initially migrated 15,000+ PCs to Linux/LibreOffice, then reversed decision to return to Windows by 2020

**Key Issues Identified:**
- Compatibility problems primarily stemmed from OpenOffice, potentially solvable with LibreOffice switch
- File sharing difficulties with external organizations using Windows
- Political factors (new mayor with Microsoft ties)
- Inadequate user training led to employee dissatisfaction
- 20-40% of users reported dissatisfaction
- Specialized public sector software mostly only available for Windows

**Lessons Learned:**
- Political support at all levels is crucial
- Change management and user training are more critical than technical issues
- Migration is a long process requiring continuous motivation and support
- Users need to feel the project improves their daily work

### Schleswig-Holstein (2024-2025) - Current Success

**Scope**: Migrating 30,000 PCs from Microsoft Windows/Office to Linux and LibreOffice

**Progress**:
- LibreOffice already installed on all 30,000 workstations
- Target: 70% Microsoft Office removal by October 2025
- Outside tax administration, 80% of workplaces have made the switch
- ODF became official document format on August 1, 2024

**Software Stack:**
- Office Suite: LibreOffice
- Email: Thunderbird replacing Outlook
- Email Server: Open-Xchange replacing Microsoft Exchange
- Cloud Collaboration: Nextcloud
- Desktop Environment: KDE Plasma on Kubuntu, openSUSE Leap, or SUSE Linux Enterprise Desktop

**Financial Impact:** Saves €15 million annually in license costs (Microsoft Office 365 and related services)

### 2. Munich LiMux - Mixed Results

**History:**
- 2004-2017: Migrated 15,000 PCs from Windows to LiMux (based on Ubuntu/Debian)
- 2017: Reversed decision, returned to Windows by 2020
- 2020: New coalition government renewed commitment to open-source

**Reasons for Initial Failure:**
- Application compatibility issues, primarily with OpenOffice (later acknowledged that LibreOffice would have been better)
- File sharing difficulties with external partners using Windows/Microsoft Office
- Inadequate user training leading to employee dissatisfaction
- Political factors (new mayor favorable to Microsoft; Microsoft moved HQ to Munich)
- Specialized government software ("Fachverfahren") was only available for Windows
- Project management challenges and user resistance

**Lessons Learned:**
- Political support at all levels is crucial
- Adequate user training is essential
- Migration must be gradual, not "big bang"
- Employee motivation and buy-in are critical
- File format compatibility matters greatly
- Integration with existing specialized software is complex

## Critical Desktop Applications

### Office Productivity Suite
- **Windows**: Microsoft Office (Word, Excel, PowerPoint)
- **Linux Alternative**: LibreOffice (Writer, Calc, Impress)
- **Status**: LibreOffice widely adopted by European governments
  - Schleswig-Holstein: 30,000 PCs migrated to LibreOffice
  - Austria Military: 16,000 systems transitioned to LibreOffice on Linux
  - Denmark: Ministry-level adoption
  - Taiwan Ministry of Education: ODF mandated across all schools

### File Format Compatibility

**ODF (Open Document Format) v1.4** was approved by OASIS as a standard in December 2025, marking 20 years since the original ODF adoption. This format is:
- An international standard (ISO/IEC 26300)
- Mandated by several governments and international organizations including NATO, European Commission
- Default format in Schleswig-Holstein (official as of August 1, 2024)
- Supported by both LibreOffice and Microsoft Office

**Microsoft Office Formats:**
LibreOffice supports reading, editing, and writing Microsoft Office formats:
- .docx, .dotx (Word documents and templates)
- .xlsx, .xlsm (Excel spreadsheets)
- .pptx (PowerPoint presentations)

Compatibility is generally good for standard documents, though complex formatting, macros, and advanced features may have limitations.

## 2. Email and Collaboration Tools

**Linux Native Options:**
- **Thunderbird** - Mature, feature-rich email client with enterprise capabilities
- **Evolution** - GNOME email client with Exchange integration
- **Open-Xchange** - Replacing Microsoft Exchange in Schleswig-Holstein migration
- **Nextcloud** - Cloud collaboration platform replacing Microsoft cloud services

**Schleswig-Holstein Implementation:**
- Microsoft Outlook replaced with Thunderbird
- Exchange replaced with Open-Xchange
- Nextcloud for cloud collaboration

## 3. Web Browsers

Modern web browsers are fully available on Linux:
- **Firefox** - Native Linux browser, used widely in government deployments
- **Chrome/Chromium** - Full feature parity with Windows versions
- **Vivaldi**, **Brave**, and other modern browsers fully support Linux

Web application compatibility is essentially identical across operating systems.

## 4. PDF Tools

**Linux Native Solutions:**
- **Okular** - KDE's universal document viewer with digital signature verification, annotation, form filling. Efficient enough to receive the Blue Angel ecolabel for resource efficiency.
- **Evince** - GNOME document viewer (being replaced by "Papers" in 2025)
- **LibreOffice Draw** - Can edit PDFs
- **PDF creation** - Built into all Linux applications via print-to-PDF

**Features:**
- Digital signature viewing and creation
- Annotation and form filling
- Multiple document format support (PDF, PostScript, DjVu, etc.)

## 5. Specialized Government Applications

**Challenge Identified:**
Schleswig-Holstein identified that integrating existing specialized administrative software ("Fachverfahren") with open-source alternatives is a **complex and ongoing process** requiring collaboration with software vendors and developing new interfaces.

**ERP Systems:**
- **SAP** - Runs on Linux (RHEL for SAP Solutions)
- Approximately 6,914 companies use SAP in Germany
- Red Hat provides specific packages for SAP compatibility on Linux

**Custom Software Options:**
- Web-based applications (OS-agnostic)
- Wine/CrossOver for Windows compatibility layer
- Virtualization for mission-critical Windows applications
- Containerization for application isolation

## Application Availability and Alternatives Comparison

### Office Productivity

| Function | Windows | Linux Alternative | Notes |
|----------|---------|------------------|-------|
| Office Suite | Microsoft Office | LibreOffice | ODF and Office format support |
| Email | Outlook | Thunderbird, Evolution | Full enterprise features |
| PDF | Adobe Acrobat | Okular, Evince, LibreOffice | Native Linux tools |
| Calendar/Contacts | Outlook | Evolution, Thunderbird | Exchange integration available |
| File Sharing | OneDrive/SharePoint | Nextcloud | Self-hosted, privacy-focused |

### Standard Desktop Applications

| Function | Windows | Linux |
|----------|---------|-------|
| Web Browser | Chrome, Edge, Firefox | Chrome, Chromium, Firefox (identical) |
| Media Player | VLC, Windows Media | VLC, MPV (identical or better) |
| Image Editing | GIMP, Photoshop | GIMP, Krita (native) |
| Video Conferencing | Teams, Zoom | Teams web, Zoom, Jitsi (native) |

## Real-World German Government Experience

### LiMux Munich (2006-2017) - Lessons Learned

**Failure Factors:**
1. **Application Compatibility Issues**: Stefan Hauf (Munich spokesperson) stated "the majority of issues stemmed from compatibility problems in OpenOffice, which could potentially have been solved by switching to LibreOffice"
2. **Political Factors**: 2014 election of Microsoft-favoring mayor coincided with Microsoft moving headquarters to Munich
3. **Inadequate Training**: Not providing adequate training led to user discomfort; 20-40% of users reported dissatisfaction
4. **File Sharing Problems**: Users unable to easily share files with external organizations using different applications
5. **Windows-Only Software**: Software essential for public sector mostly only available for Windows at the time

**Key Lesson**: Project leader stated it was "no technical project, but a change management project, dealing with the fears and emotions of people"

**Critical Success Factors Identified:**
- Political support at all levels is crucial
- Long-term approach, not "big bang" migration
- Motivation and training absolutely crucial for IT staff and users
- Users must feel the project improves their daily work

**Post-Mortem**: Munich reverted to Windows by 2020, but in May 2020 new government indicated preference for Free Software for future endeavors. October 2024 saw implementation of five-point open-source plan and Open Source Program Office.

### Schleswig-Holstein (2024-Present) - Current Success

**Scale**: 30,000 PCs migrating to Linux and LibreOffice

**Software Stack:**
- Operating System: Linux (Kubuntu, openSUSE Leap, or SUSE Linux Enterprise Desktop) with KDE Plasma
- Office Suite: LibreOffice (already installed on all 30,000 workstations)
- Email: Thunderbird replacing Outlook
- Server: Open-Xchange replacing Exchange
- Collaboration: Nextcloud for cloud services
- Standard: ODF (Open Document Format) official as of August 1, 2024

**Timeline:**
- Target: 70% Microsoft Office removal by October 2025
- Outside tax administration: Nearly 80% of workplaces have switched (as of 2025)

**Financial Impact:**
- Savings: Over €15 million in license costs in 2026
- Previous spending: License fees for Office 365 and related Microsoft services

**Training Approach:**
- Detailed migration roadmaps
- Technical training modules
- Community partnerships
- Phased implementation by department
- Ongoing support channels

**Key Motivations:**
- Digital sovereignty (reducing dependence on single non-European tech giant)
- Data protection and privacy (EDPS concerns about Microsoft 365)
- Cost savings
- Public money, public code principles

### Other German/European Government Examples

**Austria Military (2025)**:
- Migrated 16,000 systems from Microsoft Office to LibreOffice on Linux
- One of Europe's largest open-source deployments
- Emphasis on security and digital sovereignty
- Integration of external developers for training and customization
- Recognition that staff training is critical security requirement

**Bavaria, Germany**:
- Comprehensive training programs developed
- Workshops, webinars, and online resources
- Pilot programs in selected departments
- Regular progress reports and support channels

## File Format Compatibility Assessment

### ODF (Open Document Format)

**Government Adoption:**
- **Belgium**: Federal government required to accept ODF since September 2007
- **Denmark**: Mandatory ODF use by state authorities since April 2011
- **Taiwan**: Ministry of Education requires ODF in all schools
- **European Union**: European Parliament, Commission, and EUIPO integrated ODF
- **Germany**: Schleswig-Holstein made ODF official format (August 2024)

**Technical Standards:**
- ODF 1.4 approved as OASIS standard (December 2025)
- 20th anniversary of ODF adoption
- Features: cloud collaboration, richer multimedia, standardized security
- Vendor-neutral: Ensures digital sovereignty

**Interoperability:**
- Supported by both LibreOffice and Microsoft Office
- Cross-platform compatibility
- Long-term archival suitability

### Microsoft Office Formats

**LibreOffice Support:**
- Read/write support for .docx, .xlsx, .pptx
- Both strict OpenXML and transitional OpenXML formats
- Generally good compatibility for standard documents

**Limitations:**
- Complex formatting may not translate perfectly
- VBA macro compatibility limited
- Advanced features (complex pivot tables, etc.) may have issues
- Some specialized Microsoft features not supported

**Practical Approach:**
- Use ODF as primary format internally
- Export to Microsoft formats for external sharing when needed
- Test critical document types during pilot phase

## Compatibility Layers and Virtualization

### Wine (Windows Compatibility Layer)

**What it is:**
- Translates Windows API calls to POSIX calls on-the-fly
- No emulation or virtualization (except on Apple Silicon Macs)
- Native performance for compatible applications

**Adoption:**
- 2007 survey: 31.5% of 38,500 Linux desktop users used Wine
- Larger than all x86 virtualization programs combined

**Best For:**
- Office productivity tools
- Basic applications
- Legacy applications with high Wine compatibility rating

### CrossOver (Commercial Wine)

**Features:**
- Supported version of Wine from CodeWeavers
- Native speed Windows applications
- Integration with GNOME and KDE desktops
- Professional support

**Use Case:**
- Organizations needing commercial support
- Specific Windows applications that work well with Wine

### Virtualization (VirtualBox, VMware, KVM)

**Advantages:**
- Full Windows compatibility
- Isolated environment
- Reliable for mission-critical applications

**Disadvantages:**
- Resource overhead (RAM, CPU)
- Requires Windows licensing
- Weaker desktop integration
- Security updates for both host and guest OS

**Recommended For:**
- Mission-critical line-of-business software
- Applications with complex dependencies
- Specialized government applications without Linux versions

### Practical Strategy

**Recommendation from experts:**
1. **Try native Linux alternatives first** (LibreOffice, Thunderbird, etc.)
2. **Try Wine/CrossOver** for apps with good compatibility ratings
3. **Use virtualization** for mission-critical or incompatible applications
4. **Request web-based versions** from vendors for future-proofing

## Software Update and Patch Management

### Enterprise Linux Patch Management (2025)

**Current Landscape:**
- Unpatched systems remain most common breach entry point
- NIST SP 800-40 Revision 4 defines systematic patch management
- 2025 scope includes cloud-native, hybrid environments, APIs, third-party components

**Enterprise Solutions:**

1. **Action1**
   - SOC 2 Type II, ISO/IEC 27001:2022, TX-RAMP certified
   - Suitable for government organizations, healthcare, finance
   - Automated patch deployment

2. **TuxCare KernelCare Enterprise**
   - Rebootless kernel patching
   - Automatic application
   - Minimized downtime

3. **SecOps Solution**
   - Agentless model
   - Enterprise-grade automation
   - Ideal for critical industries

**Best Practices:**
- Automation of detection, prioritization, deployment, rollback
- Subscribe to CISA, NVD for vulnerability information
- Clear policies and risk-based prioritization
- Compliance-ready reporting

**Advantages Over Windows:**
- Rebootless patching available (TuxCare KernelCare)
- Generally faster security patch release
- Multiple enterprise-grade tools available
- Open-source transparency

## Licensing and Deployment Models

### Linux

**Licensing:**
- Free and open-source (no per-seat licensing)
- SUSE Linux Enterprise Desktop: Commercial support available
- Red Hat Enterprise Linux: Subscription-based support

**Deployment:**
- Standard package managers (apt, dnf, zypper)
- Centralized management tools
- Automated deployment systems
- Cloning and imaging

**Cost Structure:**
- No license fees (except commercial support)
- Support costs (if commercial distribution)
- Training costs
- Migration costs

### Windows

**Licensing:**
- Per-device or per-user licensing fees
- Volume licensing for enterprise
- Recurring costs

**Deployment:**
- Group Policy
- Windows Deployment Services
- System Center Configuration Manager

**Cost Structure:**
- License fees (ongoing)
- Support included in license
- Update infrastructure

## User Training Requirements

### Importance

**Security Perspective:**
- Inadequate training creates security risks (especially in defense)
- Well-trained workforce more resilient to change

**User Acceptance:**
- LiMux failure partly attributed to inadequate training
- User satisfaction directly correlated with training quality

### Training Program Components

**Schleswig-Holstein Approach:**
- Detailed migration roadmaps
- Technical training modules
- Community partnerships
- Department-by-department phased approach

**Bavaria Approach:**
- Comprehensive training programs
- Workshops and webinars
- Supplemental online resources
- Access to continued learning materials

**Austria Military:**
- External developers for specialized training
- Enhancements tailored to military workflows
- Ongoing support during transition

### Best Practices

1. **Invest in Training**: Critical recommendation from all successful migrations
2. **Adequate Support**: Initial technical support for quick issue resolution
3. **Gradual Migration**: Department by department, not "big bang"
4. **User Feedback**: Monitor and gather feedback for adjustments
5. **Demonstrate Value**: Help users see improvements to daily work

### Training Content Areas

- LibreOffice interface and features vs. Microsoft Office
- File format handling (ODF, Office compatibility)
- Email client transition (Thunderbird vs. Outlook)
- Linux desktop environment basics
- File management differences
- Print system usage
- Troubleshooting and support channels

### Cost Considerations

- One-time training costs vs. ongoing license savings
- Schleswig-Holstein: €15M annual savings justifies training investment
- Long-term benefits once training complete

## Accessibility and Internationalization

### Linux Accessibility

**Built-in Features:**
- Orca screen reader (GNOME)
- High contrast themes
- Screen magnification
- Keyboard navigation
- Text-to-speech

**German Language Support:**
- Full localization available in all major distributions
- LibreOffice fully translated to German
- German keyboard layouts and input methods
- Regional date/time/currency formats

### Government Requirements

- German government requires accessibility compliance
- Linux distributions meet WCAG standards
- LibreOffice provides accessibility features
- Comparable to Windows accessibility support

## Summary: Application Compatibility Assessment

### High Compatibility (Ready Now)

✅ **Office Productivity**: LibreOffice provides full functionality for documents, spreadsheets, presentations with ODF and Office format support

✅ **Email/Communication**: Thunderbird, Evolution provide complete email, calendar, contacts functionality with Exchange integration

✅ **Web Browsers**: Firefox, Chrome, Chromium - identical functionality to Windows

✅ **PDF Tools**: Okular, Evince provide viewing, annotation, digital signatures, form filling

✅ **Collaboration**: Nextcloud, Open-Xchange provide file sharing, cloud storage, groupware

### Medium Compatibility (Requires Planning)

⚠️ **Specialized Government Applications**: Require vendor cooperation, possible interface development, or virtualization

⚠️ **Custom Line-of-Business Software**: May need Wine/CrossOver compatibility layer or virtualization

⚠️ **Complex Office Documents**: May require testing and format standardization (ODF adoption helps)

⚠️ **User Training**: Significant but manageable; critical success factor

### Low Compatibility (Alternatives Available)

⚠️ **Adobe Creative Suite**: GIMP, Krita, Inkscape provide alternatives (different workflow)

⚠️ **Windows-Specific Tools**: May require virtualization or replacement with Linux alternatives

### Critical Success Factors

Based on German government experience:

1. ✅ **Strong Political Support**: Essential at all levels
2. ✅ **Comprehensive Training**: Cannot be skipped or minimized
3. ✅ **Phased Approach**: Department by department, not "big bang"
4. ✅ **Change Management**: Focus on user acceptance, not just technology
5. ✅ **Vendor Cooperation**: For specialized applications
6. ✅ **ODF Adoption**: Solves most file format issues
7. ✅ **Support Infrastructure**: Help desk, documentation, quick response

### Financial Viability

- Schleswig-Holstein: €15M annual savings (2026)
- Austria Military: 16,000 systems migrated successfully
- One-time migration costs justified by recurring license savings
- Training investment essential but amortized over time

## Confidence Assessment

**High Confidence** in findings because:
- Multiple real-world German government deployments (Schleswig-Holstein, Bavaria, Munich history)
- 30,000+ PC migrations in progress with documented results
- Clear technical evidence of application availability
- Comprehensive compatibility information from multiple sources
- Both successes (Schleswig-Holstein 2024) and failures (Munich 2017) documented with lessons learned

## Caveats and Limitations

1. **Specialized Applications**: Each government agency has unique software needs requiring individual assessment
2. **Legacy Software**: Older Windows-specific applications may require virtualization
3. **Vendor Support**: Some vendors may not support Linux officially
4. **Transition Period**: Temporary productivity impact during training and adjustment
5. **Format Compatibility**: While good, not 100% perfect for complex Office documents
6. **Organizational Culture**: Success depends heavily on change management, not just technology

## Conclusion

Linux provides comprehensive application availability for German government desktop use:

- **Core productivity applications** (office, email, PDF, browsers) have mature, feature-complete Linux alternatives
- **File format compatibility** is strong, especially with ODF adoption as official format
- **Schleswig-Holstein's ongoing success** (30,000 PCs, €15M savings) demonstrates viability with proper planning
- **Munich's earlier failure** provides valuable lessons: training and change management are critical
- **Specialized government applications** require case-by-case assessment and vendor cooperation
- **Virtualization options** provide fallback for truly incompatible applications

The technical capability exists. Success depends on comprehensive training, phased implementation, political support, and proper change management.

---

## Sources

- [LiMux - Wikipedia](https://en.wikipedia.org/wiki/LiMux)
- [German state switches to LibreOffice, promises Windows move • The Register](https://www.theregister.com/2024/04/04/germanys_northernmost_state_ditches_windows/)
- [Munich Is Ditching Linux For Purely Political Reasons](https://itsfoss.com/munich-linux-failure/)
- [Updates on Schleswig-Holstein moving to LibreOffice - The Document Foundation Blog](https://blog.documentfoundation.org/blog/2025/03/13/updates-on-schleswig-holstein-moving-to-libreoffice/)
- [German state moving 30,000 PCs to LibreOffice - TDF Community Blog](https://blog.documentfoundation.org/blog/2024/04/04/german-state-moving-30000-pcs-to-libreoffice/)
- [Schleswig-Holstein Adopts Linux Open Source Software for Data Sovereignty](https://linuxsecurity.com/news/government/schleswig-holsteins-bold-move-to-open-source)
- [What is LibreOffice? | LibreOffice - Free and private office suite](https://www.libreoffice.org/discover/libreoffice/)
- [Feature Comparison: LibreOffice - Microsoft Office - The Document Foundation Wiki](https://wiki.documentfoundation.org/Feature_Comparison:_LibreOffice_-_Microsoft_Office)
- [Celebrating 20 Years of the OASIS Open Document Format (ODF) Standard - The Document Foundation Blog](https://blog.documentfoundation.org/blog/2025/05/01/20-years-of-the-oasis-odf-standard/)
- [The Document Foundation announces the approval of the Open Document Format (ODF) v1.4 standard by OASIS Open - TDF Community Blog](https://blog.documentfoundation.org/blog/2025/12/03/tdf-announces-odf-v14-as-oasis-standard/)
- [Wine (software) - Wikipedia](https://en.wikipedia.org/wiki/Wine_(software))
- [WineHQ - Run Windows applications on Linux, BSD, Solaris and macOS](https://www.winehq.org/)
- [CrossOver runs the Windows software you need on Mac and Linux](https://www.codeweavers.com/crossover/)
- [The rise and fall of Limux [LWN.net]](https://lwn.net/Articles/737818/)
- [Denmark's Strategic Leap Replacing Microsoft Office 365 with LibreOffice for Digital Independence | Linux Journal](https://www.linuxjournal.com/content/denmarks-strategic-leap-replacing-microsoft-office-365-libreoffice-digital-independence)
- [Austrian Military Transitions to LibreOffice on Linux for Better Security](https://linuxsecurity.com/news/government/linux-security-defense)
- [Best Linux Patch Management Tools for Enterprises in 2026 | SecOps® Solution](https://www.secopsolution.com/blog/best-linux-patch-management-tools-for-enterprises-in-2025)
- [Patch Management in 2026: Benefits, Best Practices & Tools](https://tuxcare.com/blog/patch-management/)
- [Top 12 Best Email Clients for Linux in 2025](https://itsfoss.com/best-email-clients-linux/)
- [Best PDF Readers on Linux: 8 Must-Have Picks for 2025](https://updf.com/read-pdf/pdf-reader-linux/)
- [10 Best PDF Document Viewers for Linux Systems](https://www.tecmint.com/linux-pdf-viewers-and-readers-tools/)
- [Okular - The Universal Document Viewer](https://okular.kde.org/)
- [Evince - Wikipedia](https://en.wikipedia.org/wiki/Evince)
- [SAP on Linux - Supported Platforms | SAP Community](https://pages.community.sap.com/topics/linux/supported-platforms)
- [Schleswig-Holstein's Bold Open Source Leap: A Model for Digital Sovereignty? | EuroStack Directory Project](https://euro-stack.com/blog/2025/3/schleswig-holstein-open-source-digital-sovereignty)
- [EU OS: A European Proposal for a Public Sector Linux Desktop - The New Stack](https://thenewstack.io/eu-os-a-european-proposal-for-a-public-sector-linux-desktop/)
- [Open source for public sector and government | Canonical](https://ubuntu.com/gov)
