# SIAL Connection Dashboard

A real-time dashboard for tracking team performance and work activities, built with React, TypeScript, and Tailwind CSS.

## Features

- **Live View**: Real-time display of today's activities for team members
- **Monthly View**: Calendar-based interface to browse activities by date
- **Pending Tasks**: Comprehensive view of all pending tasks across all dates
- **Auto-refresh**: Automatically updates data every 10 seconds
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## Tech Stack

- **Frontend**: React 18 with TypeScript
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Build Tool**: Vite
- **Data Source**: Google Sheets integration

## Getting Started

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/abdullahsial123g/bolt-dashboard.git
cd bolt-dashboard
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## Configuration

The dashboard fetches data from a Google Sheets document. The sheet URL is configured in `src/utils/dataFetcher.ts`. Make sure your Google Sheet is publicly accessible for the dashboard to fetch data.

### Google Sheets Format

Your Google Sheet should have the following columns:
- `Date`: Date of the work entry
- `Employee Name`: Name of the team member
- `Work`: Description of the work/task
- `Direction`: Additional directions or notes
- `Status`: One of "Pending", "Working", or "Finished"

## Build for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

## Project Structure

```
src/
├── components/          # React components
│   ├── Header.tsx      # Main navigation header
│   ├── LiveView.tsx    # Today's activities view
│   ├── MonthlyView.tsx # Calendar-based monthly view
│   ├── PendingTasksView.tsx # All pending tasks view
│   ├── Calendar.tsx    # Calendar component
│   ├── WorkCard.tsx    # Individual work entry card
│   ├── StatusBadge.tsx # Status indicator component
│   └── EmployeeSection.tsx # Employee-specific section
├── types/              # TypeScript type definitions
├── utils/              # Utility functions
│   └── dataFetcher.ts  # Google Sheets data fetching
├── App.tsx            # Main application component
├── main.tsx           # Application entry point
└── index.css          # Global styles
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.
