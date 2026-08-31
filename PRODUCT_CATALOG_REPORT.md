# RK Systems - Product Catalog Report

Generated: 2026-08-30

## CCTV Section (02)
| Code | Brand | Product Name | Key Features | Image Asset |
|------|-------|-------------|--------------|-------------|
| HW.CV3 | HIKVISION | ColorVu 3.0 & AcuSense AI Dome Cameras | ColorVu 3.0, AcuSense AI, Audio 2.0 | colorvu-acusense.jpg |
| SW.NVR | HIKVISION | AcuSeek NVR & AI Agent Cloud | Natural Language Search, Elasticsearch Engine, Hik-Connect App | nvr-acuseek.jpeg |
| HW.TIOC | DAHUA | TiOC 4K Active Deterrence | Full-Colour 4K, Ενεργή Αποτροπή, Smart Dual Light | dahua.jpg |

## Alarms Section (03)
| Code | Brand | Product Name | Key Features | Image Asset |
|------|-------|-------------|--------------|-------------|
| HW.AX | HIKVISION | AX PRO Wireless Hub System | Tri-X & CAM-X Protocol, PIRCAM & IVAS, Multi-Channel Connectivity | axpro.jpg |
| HW.AJX | AJAX | Wireless Security Ecosystem | Jeweller & Wings, OS Malevich Shield, Smart Scenarios | ajax.jpg |

## Intercoms Section (04)
| Code | Brand | Product Name | Key Features | Image Asset |
|------|-------|-------------|--------------|-------------|
| HW.INT | HIKVISION | Smart IP Video Intercom | Άνοιγμα από το Κινητό, Τεχνολογία 2-Wire HD, Access Control, Σύνδεση με CCTV | hikvision-intercom.jpg |

## Networks Section (05)
| Code | Brand | Product Name | Key Features | Image Asset |
|------|-------|-------------|--------------|-------------|
| NW.UI | UBIQUITI | UniFi Wi-Fi 6/7 Systems | UniFi OS Console, Seamless Roaming, VLAN Segmentation | unifi.jpg |
| NW.TPL | TP-LINK | Omada SDN | Cloud Controllers, Managed PoE Switches, Captive Portal | omada.jpg |
| NW.MKT | MIKROTIK | RouterOS Advanced Systems | Dual-WAN Failover, WireGuard & IPsec VPN, Advanced QoS Profiles | mikrotik.jpg |

## Starlink Section (06)
| Code | Brand | Product Name | Key Features | Image Asset |
|------|-------|-------------|--------------|-------------|
| HW.SL | STARLINK | LEO High Speed Broadband | Στιβαρή Στήριξη & Στεγανοποίηση, Bypass Mode Integrations, Ιδανικό για Απομακρυσμένα Σημεία | starlink-logo.jpeg |

## Audio Section (07)
| Code | Brand | Product Name | Key Features | Image Asset |
|------|-------|-------------|--------------|-------------|
| AV.SNS | SONOS | Multi-Room Architectural Sound | Sonos Amp & Port, Multi-Zone Audio System, Επαγγελματικός & Οικιακός Ήχος | Sonos-Logo.wine.svg |

## Image Asset Inventory

### Available Images
- `ajax.jpg` (56,252 bytes)
- `axpro-black.jpg` (79,897 bytes)
- `axpro.jpg` (47,026 bytes)
- `colorvu-acusense.jpg` (81,644 bytes)
- `dahua.jpg` (91,701 bytes)
- `hero.jpg` (69,991 bytes)
- `hikvision-intercom.jpg` (506,697 bytes)
- `mikrotik.jpg` (64,332 bytes)
- `nvr-acuseek.jpeg` (58,776 bytes)
- `omada.jpg` (57,287 bytes)
- `sonos-1.jpeg` (193,475 bytes)
- `sonos.jpg` (62,804 bytes)
- `sonos-logo_2.png` (331,000 bytes)
- `Sonos-Logo.wine.svg` (1,139 bytes)
- `starlink-logo.jpeg` (107,527 bytes)
- `unifi.jpg` (71,300 bytes)

### Largest Images (Size Optimization Candidates)
1. `hikvision-intercom.jpg` - 506KB
2. `sonos-logo_2.png` - 331KB
3. `starlink-logo.jpeg` - 107KB
4. `sonos-1.jpeg` - 193KB

## Component Architecture Summary

### Component Types Used
- **NumberedSection**: Wrapper for all sections with number, title, tags
- **FeatureCard**: Standard product cards (CCTV, Alarms, Networks sections)
- **Custom Layouts**: Starlink, Audio, Intercom sections use inline layouts

### Image Sizing Patterns
- **FeatureCard**: Uses `width={800} height={600}` with `object-cover`
- **Custom Sections**: Uses `w-full h-full object-cover` in fixed-height containers
- **Hero Section**: Uses `mix-blend-multiply` with gradient masks

### Responsive Behavior
- **Mobile**: Single column grids
- **Tablet**: 2-column grids (md:grid-cols-2)
- **Desktop**: 2-3 column grids depending on section
- **Image Containers**: Fixed aspect ratios or explicit heights

## Recommendations for Table View Implementation

### Image Sizing Best Practices
1. **Use consistent aspect ratios** across all product cards
2. **Implement proper responsive widths**:
   - Mobile: 100% width
   - Tablet: 50% width
   - Desktop: 33.33% width (3 columns)
3. **Use object-fit: contain** for logos (Sonos, Starlink)
4. **Use object-fit: cover** for product photos
5. **Set explicit dimensions** in Image components for Astro optimization

### Table Structure Options
1. **CSS Grid with aspect-ratio**: Modern, responsive
2. **Flexbox with fixed widths**: More predictable
3. **HTML Table**: Traditional but less flexible
4. **Hybrid approach**: Grid for layout, flex for internal card structure

### Mobile-First Approach
- Stack all products vertically on mobile
- 2-column grid on tablet (768px+)
- 3-column grid on desktop (1024px+)
- 4-column grid on large screens (1280px+)

## Action Items
1. ✓ Create ProductCatalog component with consistent card sizing
2. ✓ Implement responsive image handling
3. ✓ Add hover effects and transitions
4. ✓ Ensure all images are optimized
5. ✓ Test across different orientations and screen sizes
