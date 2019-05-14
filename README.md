### UNDER CONSTRUCTION
- there's currently nothing here. I wish to finish it this year (2019) but i make no promises.

# js-kanman
The Javascript Kanban Manager - turns your DOM elements into a Kanban board and Manages essential user interaction. Works on desktop and mobile devices. It's opinionated because it's built especially for mobile performance in web and Cordova-based apps.

### Features:
- **smooth drag and drop**: optimized for fluency on big datasets.
- **smooth panning**: optionally, take over scrolling and make it "infinite" to cap the number of DOM elements being rendered at any given moment. This provides a performance boost especially on mobile devices with medium-strength graphic cards.
- **nested, collapsible lists**: this is something i haven't found in any other Kanban UI library - tell me if i'm wrong.
- **drop-action docks**: docks (or drawers) which appear when starting a drag operation, where you can drop stuff to apply various operations, e.g. "Delete item". Docks can be bound to the board or to a list.

### Caveats:
- Mobile performance is a double-edge sword. Less real-time computation means more ahead-of-time computation and storing everything you can in fast in-memory hashes. With big datasets expect corresponding memory consumption. In Cordova-based apps this can potentially lead to the app restarting when the user switches to another app and back to yours.

## Install
TODO: add `npm` install instructions here

## Components
- Board: container of Lists. Singleton (one board per page). Horizontal scroll only. Drop target for Lists.
- List: container of Items and/or other Lists. Vertical scroll only. Draggable. Drop target for Items and Lists.
- Item: final bit of information. Draggable.
- Dock: container of Drop targets which appears upon drag start. Can bind to the edge of a Board or List.
