# Online Appointment System
**Doctor Schedule and Appointment Management for KPPMCH**

A high-performance, scalable enterprise web application engineered for Kamphaeng Phet Municipality Community Hospital (KPPMCH). The platform streamlines clinical workflows by synchronizing real-time medical scheduling with a cloud-based data layer.

---

### Project Specification
| Category | Detail |
| :--- | :--- |
| **Project Name** | Online Appointment System |
| **Organization** | Kamphaeng Phet Municipality Community Hospital (KPPMCH) |
| **Framework** | Next.js 14+ (App Router Architecture) |
| **Language** | JavaScript (ES6+) |
| **Database** | Google Sheets API (Asynchronous Data Layer) |
| **Styling** | CSS Modules (Scoped Architecture) |

---

### System Architecture & Design Patterns

The application follows a **Decoupled Tiered Architecture**, ensuring high maintainability and scalability:

#### 1. Presentation Layer (Frontend)
* **Next.js App Router Architecture:** Utilizes the latest React Server Components (RSC) to minimize client-side JavaScript payloads.
* **Component-Based Design:** UI is decomposed into reusable, atomic components to ensure consistency across the application.
* **Client-Side Hydration:** Strategic use of `'use client'` directives for interactive appointment forms and dynamic state handling.

#### 2. Data Access Layer (Abstraction)
* **Server-Side Middleware:** Employs Next.js API Routes and Server Actions to interface securely with external APIs.
* **Data Transformation Layer:** A dedicated utility service maps raw Google Sheets arrays into structured JSON objects, ensuring the UI remains agnostic of the data source format.
* **Asynchronous I/O:** Leverages non-blocking asynchronous operations for seamless data retrieval from the Google Cloud environment.

#### 3. Styling Architecture (CSS Modules)
* **Encapsulation:** Utilizes `.module.css` files to generate unique class names, preventing global namespace pollution and style conflicts.
* **BEM Methodology:** Employs the Block-Element-Modifier convention for clear, predictable, and maintainable CSS structures.
* **Responsive Design Logic:** Implements mobile-first media queries to ensure cross-device compatibility for both patients and medical staff.



---

### Technical Infrastructure
| Component | Technology | Description |
| :--- | :--- | :--- |
| **Core Engine** | Next.js | Modern React framework optimized for production. |
| **Data Storage** | Google Sheets | Acts as a headless CMS for hospital administration. |
| **Styling** | CSS Modules | Local-scoped styling for modularity and performance. |
| **API Protocol** | REST / Server Actions | Secure end-to-end communication for booking mutations. |
| **Deployment** | Vercel | Global CDN deployment with edge caching capabilities. |

---

### Core Functionalities
* **Dynamic Resource Mapping:** Real-time conversion of spreadsheet data into accessible clinical schedules.
* **Conflict Prevention Logic:** Server-side validation routines to ensure appointments do not overlap.
* **Optimized Resource Loading:** Implementation of `React.Suspense` for granular loading states and improved Perceived Performance.
* **Data Integrity:** Robust input sanitization for all patient registration workflows.

---

### Database & Environment Configuration
To initialize the connection between the application and the data layer, the following environment variables must be defined:

```env
# Google Sheets Core Configuration
GOOGLE_SHEET_ID=your_unique_spreadsheet_id_here

# Styling Configuration (Optional)
NEXT_PUBLIC_THEME_PRIMARY=#0070f3
