# Business Requirements Document (BRD)
## Project: Flower Shop Online Ordering System

**Prepared by:** Kalani Tharanga
**Date:** 10 October 2026
**Version:** 1.0 (Draft)

---

## 1. Project Background
A mid-sized flower shop in Colombo sells bouquets, arrangements and event flowers to walk-in customers and businesses. Today, most orders come in by phone call, WhatsApp message or in person, and staff write the details in a notebook or a shared spreadsheet. During busy periods such as Valentine's Day, Mother's Day and the wedding season, calls are missed, order details are copied wrongly, and staff spend a lot of time replying to the same questions about prices and availability. Customers also have no way to check the status of their delivery without calling the shop.

## 2. Problem Statement
Manual order-taking through calls and messages causes missed orders, order mistakes and slow responses, which leads to lost sales and unhappy customers, especially during peak seasons.

## 3. Business Objectives
- Increase total orders by 20% within 6 months of launch by allowing customers to order 24/7
- Reduce order mistakes (wrong flowers, wrong address, wrong date) by 50% within 3 months
- Reduce time staff spend answering price and availability questions by 60%
- Give customers real-time delivery status updates for every order

## 4. Scope
### In Scope
- Website that works on mobile phones and computers
- Product catalogue with photos, prices and availability
- Shopping cart and checkout with delivery date, time slot and address
- Online payment (card) and cash on delivery
- Order confirmation by SMS and email
- Order tracking for customers (Received → Preparing → Out for delivery → Delivered)
- Staff dashboard to manage orders, products and stock
- Basic sales reports for the shop owner

### Out of Scope
- Mobile app (Android / iOS) — planned for phase 2
- Delivery outside the Western Province
- International orders and payments in foreign currency
- Loyalty points or membership program

## 5. Stakeholders
| Stakeholder | Role | What they need from the system |
|---|---|---|
| Shop Owner | Project sponsor | More sales, fewer mistakes, clear sales reports |
| Customers | Main users | Easy ordering, clear prices, delivery updates |
| Sales Staff | Daily users | One place to see and manage all orders |
| Florists | Prepare orders | Clear order details and delivery times |
| Delivery Staff | Deliver orders | Correct address, contact number and time slot |
| Payment Provider | External partner | Secure connection for card payments |

## 6. Functional Requirements
| ID | Requirement | Priority |
|---|---|---|
| FR-01 | Customers must be able to browse products by category (bouquets, weddings, funerals, gifts) | High |
| FR-02 | Each product must show photos, price, description and availability | High |
| FR-03 | Customers must be able to add products to a cart and change quantities | High |
| FR-04 | Customers must be able to choose a delivery date, time slot and address at checkout | High |
| FR-05 | Customers must be able to add a personal message card to an order | Medium |
| FR-06 | Customers must be able to pay by card online or choose cash on delivery | High |
| FR-07 | The system must send an order confirmation by SMS and email | High |
| FR-08 | Customers must be able to track their order status online | Medium |
| FR-09 | Staff must be able to view, update and cancel orders from a dashboard | High |
| FR-10 | Staff must be able to add, edit and remove products and mark items out of stock | High |
| FR-11 | The system must block delivery time slots that are already full | Medium |
| FR-12 | The owner must be able to view daily, weekly and monthly sales reports | Low |

## 7. Non-Functional Requirements
| ID | Requirement |
|---|---|
| NFR-01 | **Payment security:** Card payments must be handled by a PCI-DSS compliant payment provider; the shop's system must never store full card numbers |
| NFR-02 | **Data protection:** Customer personal data must be handled in line with Sri Lanka's Personal Data Protection Act (PDPA) and only used for order processing |
| NFR-03 | **Access control:** Staff accounts must use strong passwords and two-factor authentication; staff can only access features needed for their role |
| NFR-04 | **Encryption:** All pages must use HTTPS so data sent between the customer and the website is encrypted |
| NFR-05 | **Performance:** Pages must load within 3 seconds, including during peak days with up to 1,000 visitors per hour |
| NFR-06 | **Availability:** The website must be available 99.5% of the time |
| NFR-07 | **Backup:** Order data must be backed up daily and be restorable within 4 hours |
| NFR-08 | **Usability:** A first-time customer must be able to complete an order in under 5 minutes on a mobile phone |

## 8. User Stories

**US-01 — Browse flowers**
As a customer, I want to browse flowers with photos and prices so that I can choose the right gift.
*Acceptance criteria:*
- Products are grouped by category
- Each product shows at least one photo, price and availability
- Out-of-stock items are clearly marked and cannot be added to the cart

**US-02 — Place an order**
As a customer, I want to order flowers online at any time so that I don't have to call the shop.
*Acceptance criteria:*
- Customer can enter delivery date, time slot, address and phone number
- The order total, including delivery charge, is shown before payment
- The order is saved and appears on the staff dashboard immediately

**US-03 — Pay securely**
As a customer, I want to pay safely by card so that I can trust the website with my details.
*Acceptance criteria:*
- Payment is processed through a trusted payment provider page
- The customer sees a clear success or failure message
- Card details are never stored by the shop

**US-04 — Track delivery**
As a customer, I want to see my order status so that I know when my flowers will arrive.
*Acceptance criteria:*
- Status shows: Received, Preparing, Out for delivery, Delivered
- The customer receives an SMS when the order is out for delivery

**US-05 — Manage orders**
As a sales staff member, I want to see all orders on one dashboard so that no order is missed.
*Acceptance criteria:*
- Orders can be filtered by delivery date and status
- Staff can update the status of each order
- New orders are highlighted until a staff member opens them

**US-06 — Prepare orders**
As a florist, I want a clear list of today's orders with details so that I prepare the correct arrangements on time.
*Acceptance criteria:*
- List shows product, quantity, message card text and delivery time
- Orders are sorted by delivery time

**US-07 — Update stock**
As a sales staff member, I want to mark flowers as out of stock so that customers cannot order items we don't have.
*Acceptance criteria:*
- Staff can change a product to "out of stock" in one click
- The change shows on the website within 1 minute

**US-08 — Sales report**
As the shop owner, I want a monthly sales report so that I can see which products sell best.
*Acceptance criteria:*
- Report shows total sales, number of orders and top 10 products
- Report can be downloaded as Excel or PDF

## 9. Assumptions and Constraints
**Assumptions**
- Most customers have a smartphone and internet access
- The shop already has reliable internet and at least one computer for the dashboard
- A local payment provider that supports online card payments is available
- Delivery staff have mobile phones to receive order details

**Constraints**
- The system should be ready at least 4 weeks before Valentine's Day (the busiest season)
- Budget is limited, so the solution should use an existing e-commerce platform where possible
- Staff have basic computer skills, so the dashboard must be simple and require minimal training

## 10. Success Criteria
- At least 30% of all orders are placed online within 6 months
- Order mistakes reduced by 50% compared to the previous year's peak season
- Customer satisfaction rating of 4 out of 5 or higher in a post-order survey
- No security incidents involving customer or payment data in the first year

## 11. Approval
| Name | Role | Signature | Date |
|---|---|---|---|
| | Shop Owner (Sponsor) | | |
| Kalani Tharanga | Business Analyst | | |
