# Authorization Testing Results – Phase 3

| Page / Feature             | Guest | Reserver | Administrator |
|---------------------------|--------|----------|----------------|
| / (index)                 | ✅     | ✅       | ✅              |
| └─ View resource form     | ❌     | ✅       | ✅              |
| └─ Create new resource    | ❌ *1  | ❌ *2    | ✅ *3           |
| /login                    | ⚠️     | ⚠️       | ✅              |
| /register                 | ✅     | ❌       | ❌              |
| /profile                  | ❌     | ✅       | ✅              |
| /admin/users              | ❌     | ❌       | ✅              |
| /reservation              | ❌     | ✅       | ✅              |
| /resources                | ❌     | ✅       | ✅              |
| /api/reservations/1       | ⚠️     | ✅       | ✅              |

**Legend:**
- ✅ = Has access
- ❌ = Blocked
- ⚠️ = Needs attention (e.g., sensitive info leaked)

**Notes:**
- *1 Guest cannot create resources (not logged in)
- *2 Reserver lacks privileges to create
- *3 Admin can manage resources (Spec 4)

