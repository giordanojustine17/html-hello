
# AgentHub — Admin Panel Specification

## 1. Product Description

AgentHub is a SaaS platform that allows companies to rent AI agents for business tasks. Each AI agent can be equipped with skills such as web browsing, document reading, and calendar management.

The admin panel is an internal management interface used by AgentHub administrators to monitor platform activity and manage users, AI agents, skills, rental contracts, and execution errors.

The prototype will use hardcoded example data and will not connect to a backend or external APIs.

## 2. Technology Stack and Constraints

### Technologies
- HTML will provide the structure of the admin panel.
- Tailwind CSS will be loaded through a CDN for all styling.
- Vanilla JavaScript will handle all interactive features.

### Constraints
- No React, Vue, Angular, or other JavaScript frameworks.
- No jQuery or build tools.
- No external CSS files or inline style attributes.
- No backend, database, or API connections.
- All example data will be hardcoded.
- The interface must work on desktop and tablet screens.
- Tailwind's dark: utilities will support light and dark modes.

### Required Interactions
- Sidebar navigation between six sections.
- Action dropdown menus for managing records.
- Modal windows for viewing details and configuring agents.
- Expandable and collapsible agent skill lists.
- A light/dark mode toggle that maintains its state while navigating.

## 3. Dashboard Specifications

1. The Dashboard displays four metric cards in a responsive grid. On desktop, the cards appear in four columns; on tablet, they appear in two columns. Each card includes an icon, label, and hardcoded value.

2. The four metric cards show:
   - Total Revenue This Month
   - Discount and Coupon Losses
   - Active Agents
   - Failing Agents

3. Each metric card has a distinct accent color, rounded corners, and a subtle shadow. Revenue uses green, discounts use amber, active agents use blue, and failing agents use red.

4. Below the metric cards, a full-width placeholder represents a weekly activity chart. It has a dashed border and centered text reading "Weekly Activity Chart"

5. The Dashboard includes a page heading, a short description, and consistent spacing between components. It supports both light and dark mode.

## 4. User Management Specifications

1. The User Management section displays a table with at least five hardcoded user records. Each row includes the user's name, email, subscription plan, and status badge.

2. Each user row includes a clickable action button that opens a dropdown menu with two options: "View Detail" and "Delete".

3. Clicking "View Detail" opens a modal displaying information about the selected user. The modal includes a close button.

4. Clicking "Delete" opens a confirmation dialog before removing the user from the displayed table.

## 5. Agent Management Specifications

1. The Agent Management section displays a listing of at least four hardcoded AI agents. Each agent shows its name, owner, status badge, and a collapsed list of associated skills.

2. Each agent includes an expand/collapse control. Clicking the control reveals the agent's associated skills with a smooth transition. Clicking it again hides the skills.

3. Each agent has an action dropdown containing "Configure" and "Delete" options.

4. Clicking "Configure" opens a modal containing the selected agent's system prompt in an editable textarea. The administrator can save changes or close the modal.

5. Clicking "Delete" opens a confirmation dialog before removing the agent from the displayed list.

## 6. Skills Specifications

1. The Skills section displays a catalog of at least four hardcoded skills. Each skill shows its name, description, and the number of AI agents that have it enabled.

2. The Skills section includes a brief explanation of what a skill is and how skills provide capabilities to AI agents.

3. Each skill includes an action dropdown containing "View Detail" and "Delete" options.

4. Clicking "View Detail" opens a modal displaying additional information about the selected skill.

5. Clicking "Delete" opens a confirmation dialog before removing the skill from the displayed catalog.

## 7. Agent Contracts Specifications

1. The Agent Contracts section displays a table containing at least four hardcoded contracts. Each contract shows the client, assigned AI agent, contracted skills, start date, end date, and amount paid.

2. Each contract row includes an action dropdown containing a "View Detail" option.

3. Clicking "View Detail" opens a modal displaying the selected contract's full breakdown, including its contracted skills and the individual price of each skill.

4. The contract details modal includes a close button that allows the administrator to return to the contracts table.

## 8. Error Log Specifications

1. The Error Log section displays at least six hardcoded error entries. Each entry includes a timestamp, agent name, color-coded error type badge, and short description.

2. Each error entry includes an action dropdown containing two options: "View Detail" and "Mark as Resolved".

3. Clicking "View Detail" opens a modal displaying the full error trace for the selected error.

4. Clicking "Mark as Resolved" changes the selected error's status to "Resolved" and updates its appearance in the interface.

5. The Error Log uses distinct badge colors to help administrators visually distinguish different error types.

## 9. Global Interactions Specifications

1. The admin panel includes a sidebar with navigation links to all six sections: Dashboard, User Management, Agent Management, Skills, Agent Contracts, and Error Log.

2. Clicking a sidebar navigation link displays the selected section without requiring a full page reload. The currently selected section is visually highlighted.

3. The admin panel includes a light/dark mode toggle. Switching themes updates the interface across all six sections and maintains the selected theme while navigating.

4. The interface is responsive and adjusts its layout for desktop and tablet screen sizes.

5. Dropdown menus, modal windows, and expandable skill lists are interactive and can be opened and closed using JavaScript.

6. All action dropdowns close when clicking outside the menu, and all modals close using either the close button or by clicking the backdrop.

7. Hardcoded data remains consistent across sections, and the interface uses appropriate semantic HTML elements.


## 10. Component Inventory

The admin panel will use these reusable UI components:

- **Sidebar:** Navigation between all six sections.
- **Metric Cards:** Display dashboard statistics.
- **Action Dropdowns:** Provide actions for individual records.
- **Modals:** Display detailed information and agent configuration.
- **Status Badges:** Show statuses and error types using colors.
- **Collapsible Skill Lists:** Show or hide an agent's skills.
- **Dark/Light Toggle:** Switch between interface themes.

## 11. Acceptance Criteria

The prototype is complete when:

1. All six sections are accessible through the sidebar.
2. The Dashboard displays four metric cards and a weekly activity chart placeholder.
3. User Management, Agent Management, Skills, Agent Contracts, and Error Log display the required records and information.
4. All action dropdowns open and close correctly, including when clicking outside.
5. View Detail opens working modals in at least four sections.
6. All modals close using the close button or by clicking the backdrop.
7. Agent skill lists expand and collapse with a smooth transition.
8. The Configure modal displays an editable system prompt.
9. The dark/light toggle changes the entire interface and maintains the selected theme between sections.
10. Hardcoded data is consistent across sections.
11. The interface uses semantic HTML and works on desktop and tablet screens.
12. All styling uses Tailwind CSS via CDN, and all interactions use vanilla JavaScript.