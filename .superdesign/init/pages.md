# Page dependency trees
## / — friend wishlist (home)
Entry: `index.html` → `src.jsx`
- `src.jsx`
  - `style.css`
  - react, react-dom/client, lucide-react (external dependencies)
  - public/art/headphones.svg, coffee.svg, bag.svg (local URL assets)
## My wishes and together tabs
Same entry and complete dependency tree; additionally public/art/camera.svg and beach.svg.
No other local module imports. Vite config sets relative asset base. Data resides in localStorage wishtwo-v1; no authentication or backend.
