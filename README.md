# WeLocal Small Business Service

Local business management and promotion service for the WeLocal platform, built with Node.js and Express.

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/OpenAPI
- **Testing**: Jest
- **Logging**: Winston
- **Validation**: Joi
- **ORM**: TypeORM
- **File Storage**: AWS S3
- **Search Engine**: Elasticsearch
- **Payment Processing**: Stripe
- **Email Service**: SendGrid
- **SMS Service**: Twilio

## Features

- Business profile management
- Service catalog
- Appointment scheduling
- Customer reviews and ratings
- Business analytics
- Promotional campaigns
- Customer loyalty program
- Business verification
- Location-based search
- Business hours management
- Special offers and discounts

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Elasticsearch
- npm or yarn
- AWS S3 bucket
- Stripe account
- SendGrid account
- Twilio account

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-small-business-service.git
   cd welocal-small-business-service
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Configure environment variables in `.env`:
   ```env
   NODE_ENV=development
   PORT=8083
   DATABASE_URL=postgresql://welocal:welocal123@localhost:5432/welocal
   ELASTICSEARCH_URL=http://localhost:9200
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   STRIPE_SECRET_KEY=your-stripe-secret-key
   SENDGRID_API_KEY=your-sendgrid-api-key
   TWILIO_ACCOUNT_SID=your-twilio-account-sid
   TWILIO_AUTH_TOKEN=your-twilio-auth-token
   ```

## Running the Service

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Docker
```bash
docker build -t welocal-small-business-service .
docker run -p 8083:8083 welocal-small-business-service
```

## API Endpoints

### Business Profiles
- `GET /api/v1/businesses` - Get businesses list
- `POST /api/v1/businesses` - Create business profile
- `GET /api/v1/businesses/:id` - Get business details
- `PUT /api/v1/businesses/:id` - Update business profile
- `DELETE /api/v1/businesses/:id` - Delete business profile

### Services
- `GET /api/v1/businesses/:id/services` - Get business services
- `POST /api/v1/businesses/:id/services` - Add service
- `PUT /api/v1/services/:id` - Update service
- `DELETE /api/v1/services/:id` - Delete service

### Appointments
- `GET /api/v1/appointments` - Get appointments
- `POST /api/v1/appointments` - Create appointment
- `PUT /api/v1/appointments/:id/status` - Update appointment status
- `DELETE /api/v1/appointments/:id` - Cancel appointment

### Reviews
- `GET /api/v1/businesses/:id/reviews` - Get business reviews
- `POST /api/v1/reviews` - Create review
- `PUT /api/v1/reviews/:id` - Update review
- `DELETE /api/v1/reviews/:id` - Delete review

### Analytics
- `GET /api/v1/businesses/:id/analytics` - Get business analytics
- `GET /api/v1/businesses/:id/analytics/revenue` - Get revenue analytics
- `GET /api/v1/businesses/:id/analytics/customers` - Get customer analytics

## API Documentation

API documentation is available at `/api-docs` when running the service.

## Testing

### Unit Tests
```bash
npm run test
# or
yarn test
```

### Integration Tests
```bash
npm run test:integration
# or
yarn test:integration
```

### E2E Tests
```bash
npm run test:e2e
# or
yarn test:e2e
```

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route controllers
├── middleware/       # Custom middleware
├── models/          # Database models
├── routes/          # API routes
├── services/        # Business logic
├── utils/           # Utility functions
├── validators/      # Request validation
├── storage/         # File storage handling
├── search/          # Search functionality
├── payments/        # Payment processing
├── notifications/   # Email and SMS notifications
├── analytics/       # Business analytics
└── app.js           # Application entry point
```

## Security Features

- JWT token-based authentication
- Rate limiting
- CORS configuration
- Helmet security headers
- Input validation
- SQL injection prevention
- XSS protection
- File upload validation
- Secure payment processing
- Business verification system

## Monitoring

The service exposes the following endpoints for monitoring:
- `/health` - Health check
- `/metrics` - Prometheus metrics
- `/status` - Service status

## Logging

Logs are written to:
- Console (development)
- File (production)

Log levels:
- ERROR
- WARN
- INFO
- DEBUG

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 