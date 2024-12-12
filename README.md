# Build a Complete Project Management Dashboard

This repository hosts the code for a comprehensive tutorial on building a Project Management Dashboard using Next.js, Node.js, and AWS services.


## Join Our Community


## Technology Stack

- **Frontend**: Next.js, Tailwind CSS, Redux Toolkit, Redux Toolkit Query, Material UI Data Grid
- **Backend**: Node.js with Express, Prisma (PostgreSQL ORM)
- **Database**: PostgreSQL, managed with PgAdmin
- **Cloud**: AWS EC2, AWS RDS, AWS API Gateway, AWS Amplify, AWS S3, AWS Lambda, AWS Cognito

## Getting Started

### Prerequisites

Ensure you have these tools installed:

- Git
- Node.js
- npm (Node Package Manager)
- PostgreSQL ([download](https://www.postgresql.org/download/))
- PgAdmin ([download](https://www.pgadmin.org/download/))

### Installation Steps

1. Clone the repository:
   `git clone [git url]`
   `cd project-management`

2. Install dependencies in both client and server:
   `cd client`
   `npm i`
   `cd ..`
   `cd server`
   `npm i`

3. Set up the database:
   `npx prisma generate`
   `npx prisma migrate dev --name init`
   `npm run seed`

4. Configure environment variables:

- `.env` for server settings (PORT, DATABASE_URL)
- `.env.local` for client settings (NEXT_PUBLIC_API_BASE_URL)

5. Run the project
   `npm run dev`

## Additional Resources

### Code Repositories and Configuration Files

- [Complete project code on GitHub](https://github.com/TranVdc/vandy-cms)
- [Tailwind CSS configuration](https://github.com/TranVdc/vandy-cms/blob/master/client/tailwind.config.ts)
- [Redux Toolkit setup](https://github.com/TranVdc/vandy-cms/blob/master/client/src/app/redux.tsx)
- [Database seed files](https://github.com/TranVdc/vandy-cms/tree/master/server/prisma/seedData)
- [Image files](https://github.com/TranVdc/vandy-cms/tree/master/client/public)
- [globals.css file (to copy for Gantt charts)](https://github.com/TranVdc/vandy-cms/blob/master/client/src/app/globals.css)
- [AWS EC2 Instruction file](https://github.com/TranVdc/vandy-cms/blob/master/server/aws-ec2-instructions.md)


### Database Management Commands

- Command for resetting ID in database:
  ```sql
  SELECT setval(pg_get_serial_sequence('"[DATA_MODEL_NAME_HERE]"', 'id'), coalesce(max(id)+1, 1), false) FROM "[DATA_MODEL_NAME_HERE]";
  ```
