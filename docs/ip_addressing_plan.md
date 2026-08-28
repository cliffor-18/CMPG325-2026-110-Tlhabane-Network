## 4.1. Addressing Strategy & VLSM Design
- The network utilizes Variable Length Subnet Masking (VLSM) based on the assigned `192.168.49.0/24` address block. To satisfy the design constraint of a future branch office opening within 18 months, exactly half of the available address space (`/25`) is reserved. 
- The remaining space is subnetted by functional role (Management, Wired Research, Wireless Staff) rather than physical location. This provides security isolation between mobile clients and data-intensive research equipment across all floors.

## 4.2. Subnet Allocation Table & Static Device IP Assignments
- [Click here to view both IP Adress Tables DOCX](https://github.com/cliffor-18/CMPG325-2026-110-Tlhabane-Network/blob/MOHAU/docs/IP%20Address%20Tables.docx)
- [Click here to view the Static device IP Table IMAGE](https://github.com/cliffor-18/CMPG325-2026-110-Tlhabane-Network/blob/MOHAU/Images/Static%20Device%20IP%20Assignments%20table.png)
- [Click here to view the subnet Allocation Table IMAGE](https://github.com/cliffor-18/CMPG325-2026-110-Tlhabane-Network/blob/MOHAU/Images/Subent_Allocation_Table.png)

## 4.4 DHCP Pool Configuration (Wireless Clients)
- **Pool Name:** `WLAN_POOL`
- **Network:** `192.168.49.32 255.255.255.224`
- **Default Router (Gateway):** `192.168.49.33`
- **Excluded Addresses:** `192.168.49.33` (Gateway reserved)
- **Dynamic Range Available:** `192.168.49.34` - `192.168.49.62`

## 4.5. Design
- **Constraint Compliance:** Allocating the `/25` block specifically for the branch office ensures no future re-addressing is required at the main site when expansion occurs.
- **Security via Segmentation:** Using functional VLANs ensures that wireless clients on Floor 1 and Floor 2 share the same subnet and security policies, fully isolated from wired testing equipment. 
- **Efficiency:** The `/28` and `/27` subnets are sized appropriately for a foundational network, leaving an unused `/26` block (`192.168.49.64/26`) for localized Rustenburg expansion before ever touching the branch office reservation.
