# PM Tools Platform

A comprehensive platform for product managers to streamline their workflow using voice input and LLMs to maintain documentation and facilitate project scoping.

## Features

- **Multi-tenant Authentication**: Secure GitHub OAuth authentication with organization-based access control
- **Organization Management**: Create, view, and delete organizations with card-based UI
- **Product Management**: Create and manage products with detailed specifications
- **Feature Management**: Track features associated with products
- **Stakeholder Management**: Track who asked for each features and what where their pain points.
- **System Architecture**: Document system components and their dependencies
- **Voice Input**: Use voice commands to update documentation and create work orders
- **LLM Integration**: Leverage Google Gemini 2.0 and Claude 3.7 for intelligent processing
- **Work Order Management**: Create and track work orders for implementation
- **Documentation System**: Automatically generate and maintain documentation
- **Git Integration**: Sync documentation with Git repositories
- **Task Management**: Integrate with Linear for task tracking

## Tech Stack

- **Frontend**: React, TypeScript, tailwindCSS and shadcn/ui
- **Routing**: Nextjs app router
- **State Management**: Tanstack Query
- **Database**: SQLite with Drizzle ORM (Turso for production)
- **Runtime**: Bun
- **Error Monitoring**: Sentry
- **Authentication**: GitHub OAuth with custom JWT implementation
- **Speech Recognition**: Web Speech API
- **LLM Integration**: Google Gemini 2.0, Claude 3.7

## Getting Started

### Prerequisites

- Bun 1.0.0 or higher
- GitHub OAuth application credentials

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/pmtools.git
cd pmtools
```

2. Install dependencies:

```bash
bun install
```

3. Create a `.env` file in the root directory with the following variables:

```
# Authentication
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
AUTH_SECRET=your_auth_secret

# Database (Production only)
DATABASE_URL=your_turso_database_url
DATABASE_AUTH_TOKEN=your_turso_auth_token

# Sentry
SENTRY_DSN=your_sentry_dsn
```

4. Generate database migrations:

```bash
bun run db:generate
```

5. Apply migrations:

```bash
bun run db:migrate
```

6. Start the development server:

```bash
bun run dev
```

## Development

### Database Management

- Generate migrations: `bun run db:generate`
- Apply migrations: `bun run db:migrate`
- View database: `bun run db:studio`

### Linting

- Run linter: `bun run lint`
- Fix linting issues: `bun run lint:fix`

### Building for Production

```bash
bun run build:prod
```

## Project Structure

## Feature Implementation Details

### Organization Management

The platform includes a complete organization management system:

- **Organization Cards**: Organizations are displayed as interactive cards showing name and creation date
- **Organization Navigation**: Cards are clickable to navigate to detailed organization pages
- **Organization Deletion**: Admins can delete organizations they manage
- **Organization Creation**: Users can create new organizations with a simple form

### Authentication and Multi-tenancy

The system uses a custom authentication solution:

- **GitHub OAuth**: Login through GitHub with secure cookie-based sessions
- **JWT Tokens**: Stateless authentication using JWT in HTTP-only cookies
- **Multi-tenant Access Control**: Organization-based permissions and data isolation
- **Role-based Access**: Support for different roles within organizations (admin, member)

## Contributing


## License

This project is not meant to be used by anyone but its creators. Please don't steal my AI coder's work!

## Acknowledgments

- [Tanstack Router](https://tanstack.com/router)
- [Tanstack Query](https://tanstack.com/query)
- [Drizzle ORM](https://orm.drizzle.team/)
- [Sentry](https://sentry.io/)
- [boomerCSS](https://github.com/yourusername/boomercss)
