# Ebay Buyer & System Integration Module
## Project Overview
CloneEbay is an e-commerce platform mimicking eBay's functionality, built for buyers with RazorPage for both frontend and backend, integrated with PayOS for payments. Group 1 focuses on buyer features, ensuring a secure, responsive, and scalable system.
## Features
* User Management: Register (email, password, email verification), login/logout, update personal info.
* Product Browsing: List products with pagination, filter by category/price/name, view product details (images, description, seller, reviews).
* Cart & Checkout: Add products to cart (local & server), create orders, select shipping address (multiple, default option).
* Payment: Pay via PayOS (simulated PayPal, COD).
* Order Management: View order history (status, details), request returns.
* Reviews & Coupons: Rate/comment products, apply coupons.
* Notifications: System alerts for orders, promotions, responses.
* Performance: Search & product page load <1s, responsive UI for mobile.
* Security: Password hashing, JWT, CSRF protection, SSL.
* Scalability: Handle high concurrent users.
* Debugging: Detailed client/server error logging.
## Tech Stack
Frontend & Backend: RazorPage
* Database: MS SQL Server
* Payment Gateway: PayOS
* Infrastructure: Load balancing (Nginx), Kubernetes (K8s) for zero downtime
* CI/CD: Jenkins, GitLab Actions
* Rate Limiting: Prevent request spam
* Testing: JMeter for load/security testing
* Project Management: Jira, story points for task estimation
## Database Schema
Below is the MS SQL database schema with additional tables/fields for enhanced functionality.
![CloneEbayDB](https://github.com/user-attachments/assets/27c5940c-acd7-4f5e-82b9-03084d476517)
## Additional Database Notes
* Added isVerified and createdAt to User for email verification and tracking.
* Added postalCode to Address for precise shipping.
* Added parentId to Category for subcategories.
* Added condition and createdAt to Product for item status and listing time.
* Added couponId to OrderTable for coupon application.
* Added transactionId to Payment for PayOS integration.
* Added isRead to Message for read status.
* Added usedCount to Coupon for usage tracking.
* Added Notification table for system alerts (orders, promotions).

## Setup Instructions
1. Database Setup:
    * Install MS SQL Server.
    * Run the provided SQL script to create CloneEbayDB and tables.
2. Configure Environment:
    * Update appsettings.json with PayOS API keys, database connection string, and JWT settings.
3. Run Application:
<img width="1180" height="88" alt="Screenshot 2025-07-26 004337" src="https://github.com/user-attachments/assets/2909d8bf-9b7e-4acc-be29-aef54beee952" />
4. CI/CD:
    * Configure Jenkins/GitLab Actions for automated builds and deployments.
5. Testing:
    * Use JMeter for load and security testing.

## Deployment
* Infrastructure: Deploy with Nginx for load balancing, K8s for zero downtime.
* Rate Limiting: Configure to prevent request spam.

* Monitoring: Log client/server errors for debugging.
## Notes
* Mimics eBay's buyer experience with secure, fast, and responsive design.
* Scalable for high user traffic, with robust logging for debugging.
* PayOS integration ensures smooth payment processing.

