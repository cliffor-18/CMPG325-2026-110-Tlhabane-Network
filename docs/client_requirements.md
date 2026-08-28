## 1. Client Profile

**Client ID:** CLI-110

**Organization**: Tlhabane Materials Testing Laboratory

**Location**: Rustenburg

**Industry:** Research

**Addressing Block:** `192.168.49.0/24`

**Difficulty Classification:** Foundational

## 2. Organizational Context & Business Needs

Tlhabane Materials Testing Laboratory is a research facility conducting scientific
analysis of materials for industrial, construction, and manufacturing clients.
Its operations involve:

**Data-intensive testing procedures** 
- Test results and reports must be captured, stored, and shared reliably between staff.
  
**Collaborative research** 
- Technicians and researchers work across shared projects and need consistent access to network resources regardless of which room or floor they are working from.

**Mobile work patterns** 
- Staff move between testing stations, offices, and meeting areas, requiring flexible connectivity rather than being tied to a single wired desk.

**Business Impact:** 
- Network downtime or poor connectivity directly affects research turnaround time and client deliverables, so the network must be reliable and straightforward to extend as the lab grows.

**Design Implication:** 
- The lab already occupies two distinct floors (the original floor, and the additional floor taken over under CR2), the network is organized per floor rather than by device type. Each floor has its own switch, its own wireless access point, and its own logical network segment (VLAN). This keeps each floor's traffic and coverage independently manageable.

## 3. Network Requirements

The proposed network must:
3.1. Provide connectivity and network services appropriate to the client scenario

3.2. Include an appropriate network topology and device arrangement built from `192.168.49.0/24`

3.3. Configure the necessary routers, switches, end devices, Wireless Access Points, and other required nodes.

3.4. Provide successful data exchange between the appropriate network nodes.

3.5. Provide a functional Wireless LAN, integrated into the network, with coverage extended to the additional floor specified in CR2

3.6. Support future branch-office expansion within 18 months via the addressing plan.

## 4. Networking Challenge

 **Wireless LAN (AP integration and coverage)**
- The solution must configure, verify, and demonstrate the Wireless LAN within the client's network and be able to explain what was configured, why it was appropriate, and how it was verified.

## 5. Change Request ( CR2)

- The client has taken over an additional floor and requires network coverage there. The design response is a dedicated switch (Switch2-F2) and access point (AP-F2) on that floor, on its own VLAN and subnet, rather than extending Floor 1's existing hardware.

## 6. Future Expansion Requirement

- A branch office may be opened within 18 months. The IP addressing plan reserves a full, unused `/25` block (126 usable addresses) so the future branch does not require re-addressing the current site.


