# DBBL Core Auth Service Architecture 🏦🔒

Welcome to the **DBBL Core Authentication & OTP Engine** repository. This project demonstrates a secure, high-availability authentication flow designed for core enterprise banking applications and internal employee portals.

## 🏗️ Architecture Overview

The authentication workflow utilizes a **Dual-Factor Authentication (MFA)** approach using Employee ID, Phone Number verification, and dynamic OTP generation with time-bound authorization tokens.

```text
[ Client App ]  ──( ID + Phone )──> [ API Gateway ] ──> [ Auth Service ]
                                                              │
                                                     ( Verify Credentials )
                                                              │
                                                     [ DB Validation ]
                                                              │
[ Access Token ] <──( Verify OTP )── [ Send SMS OTP ] <──────┤
