# Event-Resource-Allocator

A modern web application for managing events, resources, and allocations with conflict detection. Built with Flask and featuring a beautiful skyblue and white UI theme.

## Features

- 📅 **Event Management**: Create, edit, and delete events with start and end times
- 🎯 **Resource Management**: Add and manage different types of resources
- 🔗 **Resource Allocation**: Allocate resources to events with automatic conflict detection
- ⚠️ **Conflict Detection**: Automatic detection of scheduling conflicts
- 📊 **Utilization Reports**: View resource utilization statistics and upcoming bookings
- 🎨 **Modern UI**: Beautiful skyblue and white themed interface with smooth animations

## Demo Video

Watch the demo video to see the Event Scheduler in action:

[![Demo Video](https://img.shields.io/badge/📹-Watch%20Demo%20Video-blue)](https://drive.google.com/file/d/1BfHrW4KHdELqaMdF8HQWCfsDwLITrvUw/view?usp=sharing)

**[Direct Link to Demo Video](https://drive.google.com/file/d/1BfHrW4KHdELqaMdF8HQWCfsDwLITrvUw/view?usp=sharing)**

## Technologies Used

- **Backend**: Flask (Python web framework)
- **Database**: SQLite with SQLAlchemy ORM
- **Frontend**: HTML5, CSS3, Bootstrap 5
- **Forms**: Flask-WTF, WTForms
- **Styling**: Custom CSS with modern skyblue and white theme

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/HariHara-sn/Event-Resource-Allocation.git
   cd Event-Resource-Allocation
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   flask --app app run --debug
   ```

5. **Access the application**
   Open your browser and navigate to `http://127.0.0.1:5000`

## Usage

### Creating Events
1. Navigate to the **Events** page
2. Fill in the event details (title, start time, end time, description)
3. Click **Add Event** to save

### Managing Resources
1. Go to the **Resources** page
2. Add resources with a name and type (e.g., Projector, Conference Room)
3. Edit or manage existing resources

### Allocating Resources
1. Visit the **Allocate** page
2. Select an event and a resource
3. The system will automatically check for conflicts
4. If a conflict is detected, you'll be notified and can resolve it

### Viewing Reports
1. Go to the **Report** page
2. Optionally filter by date range
3. View resource utilization hours and upcoming bookings

## Project Structure

```
Event-Scheduler-main/
├── app.py                 # Main Flask application
├── models.py              # Database models (Event, Resource, Allocation)
├── forms.py               # WTForms form definitions
├── requirements.txt       # Python dependencies
├── static/
│   └── theme.css         # Custom CSS styles (skyblue theme)
└── templates/
    ├── base.html         # Base template
    ├── events.html       # Events management page
    ├── resources.html    # Resources management page
    ├── allocate.html     # Resource allocation page
    ├── conflicts.html    # Conflict resolution page
    └── report.html       # Utilization reports page
```

## Features in Detail

### Conflict Detection
The system automatically detects when:
- Multiple events are scheduled for the same resource at overlapping times
- A new allocation conflicts with existing allocations

### Utilization Reports
- Track total hours of resource utilization
- Filter reports by date range
- View upcoming bookings count for each resource

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

**Note**: Make sure to activate your virtual environment before running the application. The database (`events.db`) will be created automatically on first run.

