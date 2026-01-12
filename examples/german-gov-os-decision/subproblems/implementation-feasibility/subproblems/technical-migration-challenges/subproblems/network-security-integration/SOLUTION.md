# Solution: Network Security and System Integration Challenges

## Answer

Network security and system integration challenges for OS deployment at scale in German government infrastructure are **largely solvable but require significant investment in integration tools, expertise, and infrastructure**. The challenges vary dramatically between Linux and Windows:

**For Linux migration from Windows:**
- **Identity/Access Management**: Mature solutions exist (SSSD, Samba) but require additional configuration and expertise beyond native Windows AD
- **Endpoint Security**: Enterprise EDR/antivirus tools now support Linux, but coverage is not as universal as Windows
- **VPN/Network**: Major enterprise VPN clients (Cisco, Palo Alto, Fortinet) support Linux via native or open-source clients
- **File Sharing**: SMB/CIFS interoperability is mature via Samba but adds complexity
- **Email/Collaboration**: Exchange integration improved dramatically in 2024-2025 with native Thunderbird support, Evolution provides full integration
- **Centralized Management**: Configuration management tools (Ansible, Puppet, Chef) replace Group Policy but require DevOps expertise
- **SIEM/Logging**: Major SIEM platforms (Splunk, QRadar, ELK) fully support Linux
- **MDM**: Limited support compared to Windows (VMware Workspace ONE best option)
- **DLP**: Major vendors (Forcepoint, Digital Guardian) support Linux but with less mature features
- **NAC/802.1X**: Full support via standard protocols, works transparently

**For Windows standardization:**
- Integration challenges are minimal as most enterprise tools are designed for Windows first
- Native Active Directory, Group Policy, Intune MDM, comprehensive security tool support
- Main challenge is legacy application compatibility, not network/security integration

**Key Finding**: The French Gendarmerie's successful migration of 103,000+ workstations to Ubuntu (97% of fleet) demonstrates that large-scale government Linux deployment with network integration is achievable. They solved integration challenges through gradual migration, centralized architecture, and investment in proper infrastructure.

## Evidence

### 1. Identity and Access Management Integration

**Active Directory Integration for Linux:**
- SSSD (System Security Services Daemon) is the modern, enterprise-standard solution for Linux-AD integration
- Provides native integration with AD, Kerberos SSO, Group Policy support, DNS updates, and offline authentication
- Red Hat documentation confirms SSSD is enterprise-ready with RBAC, sudo rules, automount maps, and audit logging
- Tested in AD environments with millions of objects, supported on RHEL 7-9, Ubuntu 20-22, Debian 10-11
- Samba remains relevant for file services but SSSD is preferred for user authentication

**Assessment**: Linux AD integration is mature and enterprise-ready, but requires more expertise than native Windows AD.

**Sources:**
- [Modern Enterprise Identity with SSSD: The Essential Guide for SREs & DevOps in 2025](https://jaipsharma.medium.com/modern-enterprise-identity-with-sssd-the-essential-guide-for-sres-devops-in-2025-403b4a34a535)
- [Red Hat: Integrating RHEL systems directly with Windows Active Directory](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/8/html-single/integrating_rhel_systems_directly_with_windows_active_directory/index)
- [Connect Linux to Active Directory using SSSD – 4sysops](https://4sysops.com/archives/connect-linux-to-active-directory-using-sssd/)

### 2. Endpoint Security (EDR, Antivirus, DLP)

**Enterprise EDR Support:**
- CrowdStrike Falcon and SentinelOne Singularity both support Windows, Linux, macOS, ChromeOS, Android, iOS
- CrowdStrike Falcon pricing: $59.99-$184.99 per device/year (2024)
- SentinelOne Singularity: $179.99-$229.99 per device/year (2024)
- Both platforms tested in 2023-2024 MITRE ATT&CK evaluations with strong detection capabilities
- CrowdStrike named in 2024 for attack technique detection; SentinelOne detected all tested techniques in 2024

**Data Loss Prevention:**
- Forcepoint DLP: Named 2024 Global DLP Company of the Year, supports Windows, Linux, Mac
- Digital Guardian (Fortra): Cross-platform support with agents for Windows, Mac, Linux
- Both provide comprehensive endpoint DLP with deep visibility into data, user, and system events

**Assessment**: Enterprise-grade security tools now provide Linux support, though Windows typically receives features first.

**Sources:**
- [SentinelOne vs. CrowdStrike: EPP Tools for the Enterprise](https://www.techtarget.com/searchsecurity/tip/SentinelOne-vs-CrowdStrike-EPP-tools-for-the-enterprise)
- [SentinelOne vs CrowdStrike | Cybersecurity Comparisons](https://www.sentinelone.com/vs/crowdstrike/)
- [Forcepoint Data Loss Prevention Software](https://www.forcepoint.com/product/dlp-data-loss-prevention)
- [Endpoint Data Loss Prevention (DLP) | Fortra's Digital Guardian](https://www.digitalguardian.com/platform/endpoint-dlp)

### 3. PKI and Smart Card Authentication

**Government PKI Support:**
- PIV/CAC smart cards implement NIST SP 800-73 Part 3, FIPS 201/HSPD-12 standards
- Windows: Native smart card authentication via domain controllers with third-party CA certificates in NTAuth store
- Linux: SSSD + GNOME Desktop Manager support smart card logon with certificates in /etc/sssd/pki
- PIVKey supports multiple platforms: Windows, OSX, Linux, Android, iOS, VMware, Citrix
- Smart cards support PKI applications: Windows logon, email/document signing, encryption, VPN, RDP, HTTPS

**Assessment**: Smart card/PKI support works on both platforms but requires more manual configuration on Linux.

**Sources:**
- [Smart Card Logon for SSH - IDManagement](https://www.idmanagement.gov/implement/scl-ssh/)
- [Red Hat: Configuring smart card authentication with local certificates](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/8/html/managing_smart_card_authentication/configuring-and-importing-local-certificates-to-a-smart-card_managing-smart-card-authentication)
- [PIVKey™ | Certificate Based PKI Tokens & Smart Cards](https://pivkey.com/)
- [Enterprise PKI Smart Card Authentication & Management](https://www.securew2.com/blog/pki-smart-card-authentication-enterprise)

### 4. VPN Client Support

**Enterprise VPN Client Availability:**
- Major VPN vendors support Linux:
  - **Cisco AnyConnect**: Native Linux client available, installable via apt on Debian-based systems
  - **Palo Alto GlobalProtect**: Supported via official client and OpenConnect compatibility
  - **Fortinet FortiClient**: Zero Trust Agent with MFA, central management, SSL/IPsec VPN support
- OpenConnect: Open-source multi-protocol VPN client supporting AnyConnect, GlobalProtect, F5, and Fortinet protocols
- Government use confirmed: Lawrence Livermore National Laboratory uses GlobalProtect and AnyConnect on government computers

**Assessment**: VPN integration is a solved problem with native and open-source client availability.

**Sources:**
- [The Top 7 Enterprise VPN Solutions](https://www.techrepublic.com/article/top-enterprise-vpns/)
- [Installing the Cisco AnyConnect VPN Client on Linux](https://www.baeldung.com/linux/cisco-anyconnect-vpn-client)
- [OpenConnect VPN client](https://www.infradead.org/openconnect/)
- [Lawrence Livermore National Laboratory VPN Instructions](https://access.llnl.gov/vpn/softwaredeployment.php)

### 5. SIEM and Centralized Logging

**Major SIEM Platform Support:**
- **Splunk**: Full Linux support, schema-on-read, ~$2,000 per GB annually
- **IBM QRadar**: Native syslog support (UDP/TCP/TLS ports 514/6514), schema-on-ingestion, EPS-based pricing
- **ELK Stack (Elastic Security)**: Open-source with native Linux support, basic version free, Cloud starts at ~$300/month
- All three platforms support cross-platform log collection from Windows, Linux, network devices, security tools
- QRadar provides pre-built connectors and DSMs for numerous devices
- ELK offers maximum flexibility for custom log formats (syslog, Windows Event Logs, network flows)

**Assessment**: SIEM integration is platform-agnostic and fully mature for Linux and Windows.

**Sources:**
- [Which SIEM Tool Is Best: Splunk vs. QRadar vs. ELK Stack?](https://www.hackers4u.com/which-siem-tool-is-best-splunk-vs-qradar-vs-elk-stack)
- [QRadar vs Splunk: SIEM Tools Review](https://www.eweek.com/security/splunk-vs-ibm-qradar-siem-head-to-head/)
- [IBM QRadar Vs. Splunk: The Ultimate SIEM Comparison For Modern Security Operations](https://passitexams.com/articles/ibm-qradar-vs-splunk-the-ultimate-siem-comparison/)

### 6. Email and Collaboration Integration

**Exchange Integration:**
- **Thunderbird**: Added native Microsoft Exchange support via EWS protocol in version 145 (late 2024)
  - Email functionality fully integrated, no third-party add-ons required
  - Calendar and address book support on roadmap
  - Working on Microsoft Graph API support for post-2026 compatibility (EWS sunset for Exchange Online in October 2026)
- **Evolution**: Native Exchange support with synced calendars and contact lists
  - Simple setup: email and password auto-configuration
  - Deep Exchange integration suitable for teams

**Important Note**: Microsoft will sunset EWS for Exchange Online in October 2026, but on-premise Exchange Server will continue supporting EWS. Thunderbird actively developing Graph API support.

**Assessment**: Exchange integration significantly improved in 2024-2025. Evolution provides complete functionality now; Thunderbird catching up rapidly.

**Sources:**
- [Thunderbird Adds Native Microsoft Exchange Email Support](https://blog.thunderbird.net/2025/11/thunderbird-adds-native-microsoft-exchange-email-support/)
- [SOLVED Thunderbird or Evolution for Microsoft Exchange Online email and calendar?](https://forums.linuxmint.com/viewtopic.php?t=397246)
- [Open Source Email Client with Exchange Support: The Best](https://truehost.com/open-source-email-client-with-exchange-support-the-best/)

### 7. Network Access Control (NAC) and 802.1X

**NAC Platform Support:**
- **Cisco ISE**: Supports 802.1X authentication, TrustSec with Security Group Tags (SGTs), robust certificate management with PKI integration
- **Aruba ClearPass**: 802.1X, MAB, web-based authentication, built-in certificate authority for BYOD
- **PacketFence**: Open-source NAC with full 802.1X and RBAC support
- 802.1X protocol is OS-agnostic: supplicant (client), authenticator (switch/AP), authentication server (RADIUS)
- Linux, Windows, and macOS all function as supplicants when properly configured

**Assessment**: NAC and 802.1X work transparently across operating systems using standard protocols.

**Sources:**
- [Cisco ISE vs. Aruba Clearpass: NAC Vendor Comparison](https://www.securew2.com/blog/nac-vendors-cisco-ise-vs-aruba-clearpass)
- [Network Access Control (NAC) - Cisco ISE Vs HPE Aruba Clearpass](https://www.thenetworkdna.com/2020/12/network-access-control-nac-cisco-ise-vs.html)
- [PacketFence | Open Source NAC](https://www.packetfence.org/)

### 8. File Sharing (SMB/CIFS/NFS)

**Cross-Platform File Sharing:**
- **Samba**: Free software implementation of CIFS/SMB protocols for Unix-like systems
- Supports Windows Server Domain, Active Directory, Windows NT domains
- Provides file and print services to Windows clients from Linux servers
- **Modern Protocol**: CIFS obsolete; SMB 2.0/3.0 are standard with stronger encryption
- SMB3 recommended for security-conscious government environments (stronger encryption than legacy CIFS)
- Interoperability works across Windows, Linux, and other OSes without hassle

**Assessment**: File sharing interoperability is mature and well-established via Samba/SMB protocols.

**Sources:**
- [What is CIFS (Common Internet File System)?](https://www.techtarget.com/searchstorage/definition/Common-Internet-File-System-CIFS)
- [CIFS vs SMB: What's the Difference?](https://www.varonis.com/blog/cifs-vs-smb)
- [Introduction to SMB/CIFS for File Sharing - Linux Bash](https://www.linuxbash.sh/post/introduction-to-smbcifs-for-file-sharing)

### 9. Centralized Management (Group Policy Equivalent)

**Configuration Management Tools:**
- **Ansible**: Agentless, Python-based, YAML syntax, easiest to learn, 41% usage in surveys
- **Puppet**: Master-agent model, Puppet DSL declarative language, suited for compliance-heavy/large enterprises, 31% usage
- **Chef**: Master-agent model, Ruby-based, steep learning curve but very flexible, 31% usage

**Key Differences from Windows Group Policy:**
- GPO is tightly integrated with Active Directory and Windows APIs
- Linux configuration management requires explicit tool deployment (though Ansible is agentless)
- Requires DevOps expertise and infrastructure-as-code approach
- More flexible and powerful than GPO but with higher learning curve
- Ansible recommended for government use: simpler, agentless, fast deployment

**Assessment**: Linux centralized management is more powerful but requires different skillset than traditional Windows GPO administration.

**Sources:**
- [Chef vs. Puppet vs. Ansible: a side-by-side comparison for 2026](https://betterstack.com/community/comparisons/chef-vs-puppet-vs-ansible/)
- [Configuration Management with Ansible, Chef, and Puppet](https://www.linuxbash.sh/post/configuration-management-with-ansible-chef-and-puppet)
- [Ansible vs. Chef vs. Puppet: A comparison](https://www.techtarget.com/searchitoperations/feature/Ansible-vs-Chef-vs-Puppet-vs-SaltStack-A-comparison)

### 10. Mobile Device Management (MDM)

**MDM Linux Support:**
- **VMware Workspace ONE**: Most comprehensive Linux support among major MDM platforms (also iOS, Android, Windows, macOS, Chrome OS)
- **Microsoft Intune**: Restricted cross-platform capabilities, limited Linux support, strongest with Windows dominance
- **Jamf**: Apple ecosystem only, no Linux support
- **Alternative Options**:
  - Fleet: Open-source, supports macOS, Windows, Linux, iOS, Android with GitOps automation
  - JumpCloud: Cloud directory + MDM for macOS, Windows, Linux
  - ManageEngine Endpoint Central: Comprehensive Linux endpoint support

**Assessment**: MDM is a gap for Linux compared to Windows. Workspace ONE best enterprise option, but Linux MDM generally less mature.

**Sources:**
- [Best Device Management Tools: Detailed Comparison](https://www.siit.io/blog/best-device-management-tools)
- [Top Endpoint Management Tools 2026 | UEM Buyer's Guide](https://zecurit.com/endpoint-management/top-endpoint-management-tools/)
- [Fleet revises open-source platform for unified device management](https://telconews.co.uk/story/fleet-revises-open-source-platform-for-unified-device-management)

### 11. Real-World Government Success: French Gendarmerie

**Scale and Timeline:**
- **103,000+ workstations** migrated to Ubuntu (GendBuntu)
- **97% of fleet** now running Linux (as of 2024)
- Migration began in early 2000s, accelerated with Ubuntu adoption in January 2008
- Recent achievement: 62,000 stations migrated from Ubuntu 20.04 to 22.04 seamlessly (June 2024)

**Network Integration Approach:**
- 2002-2004: Created centralized architecture, moved applications to Intranet for modularity
- Major challenge: Keeping computer system online during update across metropolitan France and overseas territories
- Solution: Redistributed dedicated servers/workstations on local area networks
- Result: Ubuntu Desktop "much easier to manage and maintain than Windows"

**Cost Savings:**
- 40% reduction in total cost of ownership vs Windows
- €2 million annual savings in licensing fees alone

**Key Success Factors:**
- Gradual, multi-year migration approach
- Centralized architecture investment upfront
- Focus on infrastructure modularity
- Proper planning for distributed network operations

**Assessment**: Proves that large-scale government Linux deployment with network integration is achievable at scale.

**Sources:**
- [France quietly deployed 100,000+ Linux machines in their police force](https://piefed.social/post/953245)
- [La Gendarmerie Nationale upgrades 85,000 PCs to Ubuntu Desktop Edition](https://canonical.com/blog/la-gendarmerie-nationale-upgrades-85000-pcs-to-ubuntu-desktop-edition)
- [Towards the freedom of the OS: French Gendarmerie goes Ubuntu](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/document/towards-freedom-os-french-gendarmerie-goes-ubuntu)
- [GendBuntu - Wikipedia](https://en.wikipedia.org/wiki/GendBuntu)

### 12. Real-World Challenges: Munich LiMux and UK Government

**Munich LiMux Project (2004-2017):**
- Migrated 12,600 of 15,500 desktops to Linux by 2012
- **Reversed in 2017**, returning to Windows by 2020
- Key challenges identified:
  - Initial infrastructure fragmentation: "No common directory, no common user, system or hardware management. Different tools for software distribution and system management. 21 different Windows clients, different patch levels, different security concepts."
  - Technical complexity underestimated, architects called approach "naive" in 2010
  - Most support requests: software distribution system and hardware integration
  - Organizational resistance more substantial than technical problems
  - 2014 compatibility issues with OpenOffice
  - Political factors: leadership changes shifted priorities

**UK Government Open Source:**
- 14 years since UK adopted open source policy (as of ~2024)
- **Major barriers identified**:
  - **Interoperability**: Partnership across public sector introduces biggest barriers, need for government bodies to interface with each other
  - **Skills gaps**: IT capability and confidence issues holding back progress, difficulty attracting/retaining technical expertise
  - **Technical responsibility**: OSS shifts implementation, security, maintenance to user
  - **Legacy systems**: Higher risks, inefficiencies, complexities, limitations to interoperability
  - **Cost misconceptions**: OSS not cost-free, integration and operating costs significant
  - **Procurement**: Tender process favors large providers, insufficient flexibility for small companies

**Assessment**: Integration challenges are real and organizational. Success requires addressing skills, legacy systems, cross-organizational coordination, not just technical capabilities.

**Sources:**
- [Munich Linux 'A Reality' | CIO](https://www.cio.com/article/258880/open-source-tools-munich-linux-a-reality.html)
- [LiMux - Wikipedia](https://en.wikipedia.org/wiki/LiMux)
- [Declaration of Independence: The LiMux Project in Munich](https://interoperable-europe.ec.europa.eu/collection/open-source-observatory-osor/document/declaration-independence-limux-project-munich)
- [The challenges of open source in government | Computer Weekly](https://www.computerweekly.com/news/366569099/The-challenges-of-open-source-in-government)
- [Open Source – Technology in government](https://technology.blog.gov.uk/category/open-source/)

## Confidence

**High** - Based on extensive research of current technologies (2024-2025), real-world government deployment data, and documented vendor support.

The assessment is grounded in:
- Vendor documentation and specifications from major enterprise security/infrastructure providers
- Real-world government deployment case studies (French Gendarmerie success, Munich challenges, UK barriers)
- Current product capabilities and pricing from 2024-2025
- Technical standards and protocols (802.1X, PKI, SMB, etc.)

## Caveats

1. **Timing Matters**: Many Linux integration capabilities have matured significantly in 2024-2025 (especially Thunderbird Exchange support, EDR platform support). Historical assessments may not reflect current capabilities.

2. **Expertise Required**: While technical solutions exist, they require different skillsets than traditional Windows administration. Configuration management (Ansible/Puppet/Chef) requires DevOps expertise vs traditional GPO administration.

3. **Vendor Prioritization**: Enterprise security/management tools typically prioritize Windows for new features, with Linux support following later. This creates ongoing maintenance burden.

4. **MDM Gap**: Mobile device management for Linux is notably less mature than Windows/macOS options. This is a genuine capability gap for organizations requiring strong endpoint control.

5. **Organizational Challenges**: Munich and UK experiences show that organizational factors (skills, legacy systems, cross-organization coordination, procurement) often matter more than pure technical capabilities.

6. **Context-Dependent**: Success depends heavily on:
   - Existing infrastructure investments (heavily Windows-centric environments face higher integration costs)
   - Available expertise (DevOps culture vs traditional Windows admin culture)
   - Government structure (federal vs centralized affects coordination complexity)
   - Legacy system dependencies

7. **Third-Party Tools Required**: Unlike Windows where many capabilities are native, Linux enterprise integration often requires third-party tools (SSSD for AD, Samba for file sharing, Ansible for configuration management). This adds licensing costs and complexity.

8. **Exchange 2026 Transition**: Microsoft's EWS sunset in October 2026 for Exchange Online creates uncertainty. Thunderbird is developing Graph API support, but this remains in progress.

9. **Security Tool Maturity**: While major vendors support Linux, feature parity with Windows is not guaranteed. Some advanced DLP, EDR, or endpoint protection features may be Windows-only or receive delayed Linux implementation.

10. **Assessment Assumes Modern Infrastructure**: Analysis assumes modern enterprise infrastructure (current AD, recent network equipment, contemporary security tools). Legacy systems may have worse compatibility.

## Sources

### Identity and Access Management
- [Modern Enterprise Identity with SSSD: The Essential Guide for SREs & DevOps in 2025](https://jaipsharma.medium.com/modern-enterprise-identity-with-sssd-the-essential-guide-for-sres-devops-in-2025-403b4a34a535)
- [Red Hat: Integrating RHEL systems directly with Windows Active Directory](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/8/html-single/integrating_rhel_systems_directly_with_windows_active_directory/index)
- [Connect Linux to Active Directory using SSSD – 4sysops](https://4sysops.com/archives/connect-linux-to-active-directory-using-sssd/)

### Endpoint Security
- [SentinelOne vs. CrowdStrike: EPP Tools for the Enterprise](https://www.techtarget.com/searchsecurity/tip/SentinelOne-vs-CrowdStrike-EPP-tools-for-the-enterprise)
- [SentinelOne vs CrowdStrike | Cybersecurity Comparisons](https://www.sentinelone.com/vs/crowdstrike/)
- [Forcepoint Data Loss Prevention Software](https://www.forcepoint.com/product/dlp-data-loss-prevention)
- [Endpoint Data Loss Prevention (DLP) | Fortra's Digital Guardian](https://www.digitalguardian.com/platform/endpoint-dlp)

### PKI and Smart Cards
- [Smart Card Logon for SSH - IDManagement](https://www.idmanagement.gov/implement/scl-ssh/)
- [Red Hat: Configuring smart card authentication with local certificates](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/8/html/managing_smart_card_authentication/configuring-and-importing-local-certificates-to-a-smart-card_managing-smart-card-authentication)
- [PIVKey™ | Certificate Based PKI Tokens & Smart Cards](https://pivkey.com/)
- [Enterprise PKI Smart Card Authentication & Management](https://www.securew2.com/blog/pki-smart-card-authentication-enterprise)

### VPN Clients
- [The Top 7 Enterprise VPN Solutions](https://www.techrepublic.com/article/top-enterprise-vpns/)
- [Installing the Cisco AnyConnect VPN Client on Linux](https://www.baeldung.com/linux/cisco-anyconnect-vpn-client)
- [OpenConnect VPN client](https://www.infradead.org/openconnect/)

### SIEM and Logging
- [Which SIEM Tool Is Best: Splunk vs. QRadar vs. ELK Stack?](https://www.hackers4u.com/which-siem-tool-is-best-splunk-vs-qradar-vs-elk-stack)
- [QRadar vs Splunk: SIEM Tools Review](https://www.eweek.com/security/splunk-vs-ibm-qradar-siem-head-to-head/)

### Email Integration
- [Thunderbird Adds Native Microsoft Exchange Email Support](https://blog.thunderbird.net/2025/11/thunderbird-adds-native-microsoft-exchange-email-support/)
- [SOLVED Thunderbird or Evolution for Microsoft Exchange Online email and calendar?](https://forums.linuxmint.com/viewtopic.php?t=397246)

### Network Access Control
- [Cisco ISE vs. Aruba Clearpass: NAC Vendor Comparison](https://www.securew2.com/blog/nac-vendors-cisco-ise-vs-aruba-clearpass)
- [PacketFence | Open Source NAC](https://www.packetfence.org/)

### File Sharing
- [CIFS vs SMB: What's the Difference?](https://www.varonis.com/blog/cifs-vs-smb)
- [Introduction to SMB/CIFS for File Sharing - Linux Bash](https://www.linuxbash.sh/post/introduction-to-smbcifs-for-file-sharing)

### Configuration Management
- [Chef vs. Puppet vs. Ansible: a side-by-side comparison for 2026](https://betterstack.com/community/comparisons/chef-vs-puppet-vs-ansible/)
- [Configuration Management with Ansible, Chef, and Puppet](https://www.linuxbash.sh/post/configuration-management-with-ansible-chef-and-puppet)

### Mobile Device Management
- [Best Device Management Tools: Detailed Comparison](https://www.siit.io/blog/best-device-management-tools)
- [Top Endpoint Management Tools 2026 | UEM Buyer's Guide](https://zecurit.com/endpoint-management/top-endpoint-management-tools/)

### Government Case Studies
- [La Gendarmerie Nationale upgrades 85,000 PCs to Ubuntu Desktop Edition](https://canonical.com/blog/la-gendarmerie-nationale-upgrades-85000-pcs-to-ubuntu-desktop-edition)
- [GendBuntu - Wikipedia](https://en.wikipedia.org/wiki/GendBuntu)
- [LiMux - Wikipedia](https://en.wikipedia.org/wiki/LiMux)
- [The challenges of open source in government | Computer Weekly](https://www.computerweekly.com/news/366569099/The-challenges-of-open-source-in-government)
