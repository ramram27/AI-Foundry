# Smart City Complaint

Build a modern, professional, responsive web application named SmartCity Connect — Smart City Complaint Management System using React.js.

The application will allow citizens to report civic problems such as potholes, garbage overflow, broken streetlights, water leakage, drainage problems, and damaged roads. Government officials and administrators will have dedicated dashboards to manage complaints, track progress, and monitor city issues.

Important: Develop only the frontend. Do not create a backend, server, database, or REST API. Use mock data and browser localStorage to simulate application functionality.

The UI should look like a real, production-quality civic technology platform suitable for a hackathon demonstration.

## 1. Technology Stack

Use the following technologies:

- React.js with Vite
- TypeScript
- Tailwind CSS
- React Router DOM
- Lucide React for icons
- Recharts for charts and analytics
- React Leaflet with OpenStreetMap for interactive maps
- React Hook Form and Zod for form handling and validation
- Context API or Redux Toolkit for state management
- localStorage for persisting demo data
- Toast notifications for user feedback

Use reusable React components and a clean, scalable folder structure.

## 2. UI/UX Design

Create a modern SaaS-style dashboard with a professional government and smart-city theme.

### Design guidelines
- Primary color: Navy blue
- Secondary color: Teal
- Background: Light gray or off-white
- Success: Green
- Warning: Amber
- Critical priority: Red
- Use clean typography and consistent spacing.
- Use cards with subtle shadows and rounded corners.
- Add smooth hover effects and transitions.
- Create responsive layouts for mobile, tablet, and desktop.
- Add loading skeletons, empty states, confirmation dialogs, and error messages.
- Support accessible form labels, keyboard navigation, and readable contrast.
- Avoid excessive gradients, unnecessary animations, and cluttered layouts.

Create a collapsible sidebar for dashboards and a responsive navigation menu for mobile screens.

## 3. Application Pages

### A. Public Landing Page

Create an attractive landing page with:
- SmartCity Connect logo and navigation
- Hero section explaining the platform
- Headline: "Building Better Cities, One Complaint at a Time"
- Short description of the platform
- "Report an Issue" and "Track Complaint" buttons
- Civic issue category cards
- How It Works section
- Platform statistics using clearly labeled demo data
- Recent public complaints
- Benefits for citizens and government officials
- Footer with contact information and navigation links

### B. Login Page

Create a login interface with:
- Email input
- Password input
- Show/hide password
- Remember me option
- Forgot password UI
- Login button
- Form validation
- Demo account selection
- Link to registration

Since there is no backend, implement a simulated login flow using predefined demo accounts and local application state. Clearly label the accounts as demo accounts.

### C. Registration Page

Include:
- Full name
- Email address
- Password
- Confirm password
- Phone number
- Ward or locality
- Terms and conditions checkbox
- Validation messages
- Password strength indicator
- Registration success feedback

Store registered demo users in localStorage. Do not imply that this is production-grade authentication.

### D. Citizen Dashboard

Create a dashboard displaying:
- Welcome message with citizen name
- Total complaints submitted
- Pending complaints
- In-progress complaints
- Resolved complaints
- Recent complaints table
- Complaint status distribution chart
- Recent activity timeline
- Notifications panel
- Quick action button to report a new issue

Every statistic must be calculated from the mock data available in the frontend.

### E. Submit Complaint Page

Build a complete complaint submission form with:
- Complaint title
- Detailed description
- Category dropdown
- Priority selector
- Image upload with preview
- Address
- Landmark
- Ward or locality
- Latitude and longitude fields
- Interactive map location picker
- Submit and cancel buttons

Available categories:
- Road and potholes
- Garbage and sanitation
- Water supply
- Drainage and sewage
- Streetlights
- Public infrastructure
- Other

On submission:
- Validate all fields.
- Generate a unique complaint ID, such as SC-2026-0001.
- Save the complaint to localStorage.
- Set its initial status to "Submitted".
- Show a success notification.
- Redirect to the complaint details page.
- Update the citizen dashboard automatically.

Use local mock behavior for the map. Do not require a paid map API key.

### F. My Complaints Page

Create a complaint management interface for citizens with:
- Search by complaint ID or title
- Filter by status
- Filter by category
- Filter by date
- Sort by newest or oldest
- Table view and card view
- Pagination
- Status badges
- Complaint submission date
- Complaint location
- View details button

Show an attractive empty state when no complaints match the selected filters.

### G. Complaint Details and Tracking Page

Display:
- Unique complaint ID
- Complaint title and description
- Uploaded images
- Location details
- Category and priority
- Submission date
- Current status
- Assigned department and official
- Status progress timeline
- Official remarks
- Resolution images when available
- Feedback form after resolution

Use a visual timeline with these stages:

Submitted → Under Review → Assigned → In Progress → Resolved → Closed

Also support Rejected and Reopened states in the interface.

Provide demo buttons for eligible status changes where appropriate, with confirmation dialogs. Clearly identify simulated updates as demo behavior.

### H. Interactive City Map

Build a map-based complaint visualization page using React Leaflet and OpenStreetMap.

Features:
- Map markers for complaint locations
- Different marker colors for statuses or categories
- Popup cards with complaint ID, title, status, and category
- Category filters
- Status filters
- Priority filters
- Search by locality
- Complaint list alongside the map
- Map/list view toggle
- Fit map to available complaint markers

Use predefined sample coordinates for demo complaints in a configurable sample city. Clearly label sample locations as demonstration data.

Do not expose private citizen details on the public map.

### I. Government Official Dashboard

Create a dedicated dashboard for government officials with:
- Total assigned complaints
- New complaints
- In-progress complaints
- Resolved complaints
- Overdue complaints
- Priority distribution chart
- Recent complaint activity
- Department performance summary
- Complaints requiring immediate attention

Include filters for department, category, status, priority, and ward.

### J. Complaint Management Page

Create a table for managing complaints with:
- Complaint ID
- Title
- Category
- Location
- Priority
- Assigned department
- Assigned official
- Current status
- Submission date
- Actions menu

Allow demo users with the appropriate role to:
- View complaint details
- Assign a department
- Assign an official
- Change status
- Add remarks
- Mark complaints as resolved
- Review uploaded evidence

Persist simulated changes to localStorage and reflect them across the interface.

### K. Admin Dashboard

Build a comprehensive dashboard for administrators.

Summary cards:
- Total complaints
- Pending complaints
- In-progress complaints
- Resolved complaints
- Overdue complaints
- Resolution rate

Charts:
- Complaints submitted over time
- Complaints by category
- Complaints by status
- Complaints by ward
- Monthly resolution trends

Additional features:
- Recent complaints
- High-priority issues
- Department performance table
- Search and filtering
- Export complaints to CSV
- Date range selector

Use Recharts and calculate chart values from the mock complaint dataset. Label any seeded sample data as demonstration data.

### L. User and Department Management

Create administrative pages for:
- Viewing demo users
- Searching and filtering users
- Assigning user roles in demo mode
- Viewing departments
- Adding a department
- Editing department information
- Assigning complaint categories to departments

Persist changes in localStorage.

### M. Notifications Page

Create a notification center with:
- Complaint submission notifications
- Status change notifications
- Assignment notifications
- Resolution notifications
- Read and unread states
- Mark as read
- Mark all as read
- Filter by notification status

Generate local demo notifications when application actions occur.

### N. Profile and Settings

Include:
- User profile
- Edit name and contact details
- Profile avatar
- Preferred locality
- Notification preferences
- Theme preference
- Logout button

Save profile and preference changes in localStorage.

## 4. Demo User Roles

Provide predefined demo accounts for the following roles:

1. Citizen
2. Government Official
3. Administrator

Use a demo login selector so judges can quickly explore each dashboard.

Implement role-based navigation and route guards in the React application. Because there is no backend, explain in the README that frontend role restrictions are only for demonstration and are not secure authorization.

## 5. Mock Data

Create a separate mock data module containing at least:
- 20 sample complaints
- 5 demo citizens
- 3 demo government officials
- 5 departments
- 10 sample notifications
- Status history for several complaints
- Sample resolution evidence
- Different complaint categories, priorities, and locations

Use realistic sample complaint titles, such as:
- Large pothole near the main road
- Garbage not collected for three days
- Streetlight not working near the park
- Water leakage near a residential building
- Drainage overflow in the market area

Seed the demo data into localStorage only when the application has no existing demo data. Do not overwrite user changes on every page refresh.

## 6. Frontend State Management

Implement the following:
- Centralized complaint state
- Reusable custom hooks
- Persistent localStorage state
- Search, sorting, and filtering
- Form validation
- Role-based navigation
- Notification updates
- Dashboard data calculations
- Complaint status history
- CSV export
- Image previews
- Toast messages

Use a clear separation between mock data, UI components, page components, hooks, and utility functions.

Create a mock service layer that simulates asynchronous operations with Promises. Keep all demo data operations separate from the UI so the project can be connected to a real backend in the future.

Do not create fake REST API endpoints or make network requests to a nonexistent server.

## 7. Reusable Components

Create reusable components such as:
- AppLayout
- Sidebar
- Navbar
- MobileNavigation
- StatCard
- ComplaintTable
- ComplaintCard
- StatusBadge
- PriorityBadge
- ComplaintFilters
- SearchInput
- Pagination
- ComplaintTimeline
- NotificationItem
- MapView
- ChartCard
- ImageUploader
- ConfirmDialog
- EmptyState
- LoadingSkeleton
- ToastProvider
- ProtectedRoute
- RoleBasedRoute

Avoid duplicating the same UI and business logic across pages.

## 9. Functional Requirements

Every visible button, form, filter, menu, tab, and navigation link must perform its intended frontend action.

The following must work:
- Registration and demo login
- Role-specific navigation
- Complaint submission
- Image preview
- Complaint search and filtering
- Complaint details
- Status timeline
- Simulated assignment and status updates
- Notifications
- Dashboard charts
- CSV export
- Profile editing
- localStorage persistence
- Responsive mobile navigation
- Logout