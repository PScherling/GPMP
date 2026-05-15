# Roadmap and Vision

## 💡 Vision

Sensei aims to become:

“The modern GPMC replacement for real-world enterprise environments.
Classic GPMC Re-Imagined for admins of tomorrow.”

Not just a viewer — but a control plane for Group Policy.

---

## 🛣️ Roadmap

### Phase 2
<dl>
  <ul>
    <li><dt>GPO creation workflow</dt></li>
    <li><dt>GPO link creation workflow</dt></li>
    <li><dt>GPO deletion workflow</dt></li>
    <li><dt>Advanced write auditing</dt></li>
    <li><dt>Scheduled background sync</dt></li>
    <li><dt>UI polish</dt></li>
      <dd>Toolbar Polish:
        <ul>
          <li>Sync Button realignment (maybe a drop down menu selection)</li>
          <li>Button "Create GPO" realignment into "All GPO Objects" pane</li>
          <li>History polish</li>
        </ul>
      </dd>
      <dd>Sort for "Applied GPOs" (affects only 'directly linked' GPOs):
        <ul>
          <li>By Link Order</li>
          <li>By Name (DESC and ASC)</li>
        </ul>
      </dd>
  </ul>
</dl>


<br>

### Phase 3
<dl>
  <ul>
  <li><dt>Advancing Info Tab for selected GPO element</dt></li>
    <dd>Showing linked OU information including:
      <ul>
        <li>Link enabled/disabled</li>
        <li>Enforced/Not Enforced</li> 
        <li>if it's directly linked or inherited from parent (hirarchial tree view</li>
      </ul>
    </dd>
    <li><dt>Function "Create and directly link GPO to selected OU"</dt></li>
    <li><dt>Drag and Drop GPO to OU for linking</dt></li>
    <li><dt>Full Group Policy Configuration export for security audits</dt></li>
    <li><dt>Advanced auditing (user, timestamp, before/after values, IDs, filtering, export, possible SIEM integration)</dt></li>
    <li><dt>GPO Import/Export Functionality (including manifest.xml) like GPMC is doing it</dt></li>
  </ul>
</dl>

<br>

### Phase 4
<dl>
  <ul>
    <li><dt>Backup / Rollback (before write operations?)</dt>
      <dd>Important for 'destructive' changes</dd>
    <li><dt>Dry-Run / Preview Mode</dt>
      <dd>Example: "This action will affect:
        <ul><li>14 OUs</li>
          <li>320 users</li>
          <li>12 servers/workstations</li>
        </ul>
      </dd>
    <li><dt>WMI Filter Management</dt></li>
    <li><dt>Search by Settings-Content (partially already implemented in phase 1)</dt></li>
      <dd>Example: "Find every GPO configuring RDP, LAPS, Credential Delegation, Defender, SmartScreen"</dd>
    <li><dt>Cache-DB-AD Drift detection / Scheduled Background Sync</dt></li>
      <dd>Example: Configuration changed via GPMC (externally) -> Cache detects drifts</dd></li>
    <li><dt>Multi Domain Support</dt></li>
  </ul>
</dl>


---

## ⚠️ Known Limitations (RC1)
- No write operations UI yet (read-first design)
- No multi-user audit trail
- No role-based UI personalization
- Initial sync progress visibility is basic


