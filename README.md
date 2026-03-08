FinancePulse 

Modern Personal Finance Ledger for Next.js
FinancePulse is a high-performance, aesthetically driven personal finance tracker built with Next.js 14+, Tailwind CSS, and Recharts. It’s designed as a "glassmorphism-inspired" dashboard that balances professional data visualization with a minimalist user experience.

🚀 The Build
Framework: Next.js (App Router)using javascript

Styling: Tailwind CSS (Modern arbitrary values & animations)

Icons: Lucide-React

Charts: Recharts (Responsive SVG-based visualization)

State & Persistence: React Hooks + LocalStorage API

🛠️ Design & Technical Choices
Next.js Client Components: Used the "use client" directive to leverage browser-side APIs (LocalStorage) and complex state management, ensuring a smooth, single-page application feel within the Next.js framework.

Intelligent UI Feedback: Beyond basic CRUD, the app features logic-based UX, such as "Low Funds" warnings and a "Budget Alert" mode that transforms the UI color palette when spending limits are exceeded.

Smart Search Pattern: Implemented a unique search logic that clears the input field while maintaining the filtered view, reducing visual clutter in the Activity Log.

Performance Optimization: Utilized useMemo for heavy transaction filtering and useEffect cleanups for all timers/notifications to prevent memory leaks during rapid data entry.

🧠 Challenges & Solutions
SSR vs. Hydration: A common Next.js challenge was ensuring the localStorage data didn't cause hydration mismatches. I solved this by wrapping the data retrieval in a useEffect hook, ensuring the client-side state only populates after the initial mount.

Responsive Visualization: Making SVG charts truly responsive within a complex Tailwind Grid required fine-tuning the ResponsiveContainer and aspect ratios to ensure legibility on both mobile and ultra-wide screens.

📈 Future Roadmap (What I'd Improve)
Modular Architecture: While currently a single-file power-component, I’d move the categoryMap, SummaryCard, and business logic into a dedicated /hooks and /components folder structure for better scalability.

API Integration: Transition from LocalStorage to a database (like Supabase or PostgreSQL) using Next.js Server Actions for cross-device synchronization.

Dark Mode Support: Implement a native Tailwind dark: theme to complement the current high-contrast light mode.

⏱️ Project Metadata
Time Spent: Approximately 4.5 hours (Logic development, UI polishing, and responsive testing).

Goal: To build a functional, production-ready tool that solves the "over-complicated finance app" problem with a clean, one-page solution.
