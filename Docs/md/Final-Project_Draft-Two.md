
```python
"""
Python Application for: Bath & Body Works
Client: Bath & Body Works (Consumer Retail)
Github Repository: [Insert Link Here]
Kanban Board: [Insert GitHub Project Link Here]

=== PURPOSE ===
Track fragrance preferences and create event-linked shopping lists organized by:
- Year/Season
- Birthdays/Holidays
- Purchase Status ("I Like This", "Not Smelled", etc.)

=== SCOPE ===
Core Features:
1. Fragrance inventory management with seasonal categorization
2. Shopping list creation for special occasions
3. JSON data storage for user collections
4. Birthday age calculation feature
5. GUI with 3 main classes (FragranceCollection, ShoppingListManager, UserPreferences)

Non-Core Features (Future):
- Email notifications
- Excel integration for birthday tracking

=== SYSTEM DESIGN ===
Architecture:
[GUI Layer] ↔ [Business Logic Layer] ↔ [JSON Data Storage]

Key Components:
1. User Interface (Tkinter/PyQt)
2. Data Managers (Classes below)
3. JSON Database (fragrances.json, lists.json)

=== CLASSES ===
1. FragranceCollection
   - Responsibilities: Manage scent inventory
   - Collections: List[Dict] (fragrance items)
   - Methods: add_fragrance(), categorize_by_season()

2. ShoppingListManager
   - Responsibilities: Handle list operations
   - Collections: Dict{year: List[items]}
   - Methods: create_list(), export_to_json()

3. UserPreferences
   - Responsibilities: Store settings & notifications
   - Collections: Dict{preference: value}
   - Methods: set_reminder(), calculate_age()

=== UML CLASS DIAGRAM (Mermaid) ===
classDiagram
    class FragranceCollection{
        +fragrances: List[Dict]
        +add_fragrance()
        +remove_fragrance()
        +categorize_by_season()
    }

    class ShoppingListManager{
        +shopping_lists: Dict
        +create_list()
        +edit_list()
        +import_export_json()
    }

    class UserPreferences{
        +settings: Dict
        +set_reminder()
        +calculate_birthday()
    }

    class GUI{
        -collection: FragranceCollection
        -list_manager: ShoppingListManager
        -preferences: UserPreferences
        +run_interface()
    }

    GUI --> FragranceCollection
    GUI --> ShoppingListManager
    GUI --> UserPreferences

=== ENTITY RELATIONSHIP DIAGRAM (Mermaid) ===
erDiagram
    USER ||--o{ FRAGRANCE : "Owns"
    USER ||--o{ SHOPPING_LIST : "Creates"
    SHOPPING_LIST ||--o{ EVENT : "Associated With"
    
    USER {
        int user_id PK
        string name
        string contact_info
    }
    
    FRAGRANCE {
        int fragrance_id PK
        string name
        string season
        int year
        string status
    }
    
    SHOPPING_LIST {
        int list_id PK
        string occasion_type
        date target_date
    }
    
    EVENT {
        int event_id PK
        string event_name
        date event_date
    }

ERD Explanation:
1. Users own multiple fragrances and shopping lists
2. Shopping lists connect to specific events (birthdays/holidays)
3. Relationships maintain year/season organization through event dates
4. Fragrance statuses drive shopping list suggestions

=== DATA FLOW ===
User Input → GUI → Class Methods → JSON Storage
(Updates propagate bidirectionally with data validation)

=== IMPLEMENTATION NOTES ===
1. Uses Python 3.10+ type hints
2. Requires json and datetime modules
3. Tested with pytest for core logic
4. GUI uses Tkinter for cross-platform compatibility
"""
```

This header includes:
1. Clear client identification
2. Realistic scope with phased implementation
3. Visual system architecture
4. Three required classes with collection types
5. Mermaid diagrams for both UML and ERD
6. GitHub/Kanban board integration
7. Data flow explanation
8. Technical implementation details

The design focuses on achievable goals while leaving room for future expansion. The class structure enables:
- Separation of concerns (data vs UI)
- Easy JSON serialization
- Collection manipulation (lists for fragrances, dicts for quick year lookups)
- Birthday calculations using datetime module
