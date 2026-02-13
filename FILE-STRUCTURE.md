# documove - File Structure & Routing

## Folder Structure
```
documove/
  index.html              # Marketing homepage
  login.html              # Unified login
  app/
    agent.html            # Agent dashboard
    solicitor.html        # Solicitor dashboard
    track.html            # Buyer/Seller portal
    documents.html        # Document upload
    messages.html         # Real-time messaging
    sign.html             # E-signature
  css/
    design-system.css     # Shared styles
  js/
    lib-supabase.js       # Helper functions
  database/
    schema.sql            # Supabase schema
```

## URL Structure

### Public Pages
- `https://documove.co.uk` - Marketing homepage
- `https://documove.co.uk/login` - Unified login

### App Pages (Requires Login)
- `https://documove.co.uk/app/agent` - Agent dashboard
- `https://documove.co.uk/app/solicitor` - Solicitor dashboard
- `https://documove.co.uk/app/track` - Buyer/Seller tracking

### Feature Pages (Within Dashboards)
- `app/documents` - Document management
- `app/messages` - Messaging
- `app/sign` - E-signature

## Navigation Flow
```
index.html (Marketing) -> Click Login -> login.html
login.html -> Agent -> app/agent.html
login.html -> Solicitor -> app/solicitor.html
login.html -> Buyer/Seller -> app/track.html
```

## File Mapping
| Original File | Deploy As | URL |
|---|---|---|
| documove-agent-focused.html | index.html | / |
| unified-login.html | login.html | /login |
| agent-dashboard-connected-FIXED.html | app/agent.html | /app/agent |
| solicitor-dashboard.html | app/solicitor.html | /app/solicitor |
| buyer-seller-portal.html | app/track.html | /app/track |

## Protected Routes
All app routes check for authentication:
```javascript
const { data: { session } } = await supabase.auth.getSession();
if (!session) window.location.href = '/login.html';
```

## Logout
All logout buttons redirect to `/login.html` or `/index.html`
