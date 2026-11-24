# Route Branch Planner

Plan a trip as a network of places and the legs between them, then build, compare and pick named plans on one timeline.

It is a single HTML file with no build step, no server and no dependencies. Open `index.html` in a browser, or host it anywhere that serves static files (GitHub Pages works out of the box).

## How it works

- **Nodes** are places: home, a station, an airport, a city. Each node is one row on the timeline, and every leg in or out of it meets there.
- **Legs** join two nodes. Each leg has how you travel (flight, train, bus, cab / van, ferry, other), when it leaves and arrives, an optional buffer for delays, and a fare. When you add a leg, you pick its ends from your nodes or create a new node.
- **Plans** are made in the plan maker. You name the plan, pick the start node and one of its departures, then the end node and one of its arrivals. Every leg that fits between them is listed, and wherever the routes split you choose which way. Nothing is chosen for you.
- **Costs**: each leg has one fare, shared by every plan that uses it. Legs with the same two nodes, transport and times are treated as the same trip and always share a fare. Each plan can add its own other costs, such as a hotel or food.

## Features

- Timeline with a day and night sky, start and end times on every leg, travel time on every line, and waiting times with labels you can edit (Transfer, Stay, Overnight stop, or your own).
- A view for each plan that shows only that plan. Legs you add while a plan is shown join it as soon as they connect to its route.
- Plan comparison: total per head, door-to-door time, waiting time and a budget check, sorted however you like. Star the plan you pick.
- A picture for each node, from a file or a link.
- Costs on the timeline, off by default, with a button to switch them on.
- Currency picker, starting from the browser's region.
- Light and dark mode, a hideable edit panel and a slide-up plans drawer.
- Undo, plus Export and Import as a JSON file.

## Your data

Everything you enter is saved in your own browser (`localStorage`) on the device you use. Nothing is sent anywhere. Someone else opening the same hosted page sees only their own plans. Use **Export** to keep a copy or move your plans to another browser, and **Import** to load them back.

Browser storage is limited to a few megabytes. Node pictures are shrunk before they are saved, but many pictures can still fill it; the page tells you when it cannot save.

A picture added from a link is copied into your plans when the site allows it. Otherwise it is shown straight from the link, which needs the internet each time.

## Use it

- **Online:** https://chowdri7.github.io/wander_map/
- **Offline:** download `index.html` and open it in any current browser.

## Try it

Choose **Example** (or **Load an example** on the empty screen) to load a made-up weekend trip with three plans. Its places, times and costs are invented. **Clear** empties the planner again.
