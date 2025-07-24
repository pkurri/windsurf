# User Stories

## US-001: User Authentication

- As a user, I want to log in with my email and password so that I can access my account.
- Acceptance Criteria:
  - Successful login returns a JWT token.
  - Invalid credentials return a 401 error.
  - `/src/auth/login.ts`
  - `/tests/auth/login.test.ts`

## US-002: Payment Processing

- As a user, I want to make a payment using Stripe so that I can purchase products.
- Acceptance Criteria:
  - Payment is processed successfully.
  - User is redirected to a confirmation page.
- Linked Files:
  - `/src/payment/stripe-service.ts`
  - `/tests/payment/stripe.test.ts`