# app-ssh

Aplikasi manajemen SSH berbasis web untuk mengatur akses host, rotasi kunci, dan audit aktivitas, terinspirasi dari Bastillion.

---

## 🚀 Tech Stack

**Backend**
- Bahasa: [Go](https://go.dev/)  
- Framework: [Gin](https://gin-gonic.com/) atau [Fiber](https://gofiber.io/)  
- Library SSH: [`golang.org/x/crypto/ssh`](https://pkg.go.dev/golang.org/x/crypto/ssh)  
- API: REST (OpenAPI/Swagger), opsional gRPC untuk komunikasi internal  
- Database: [PostgreSQL](https://www.postgresql.org/)  
- Cache/Queue: [Redis](https://redis.io/) (untuk session & job eksekusi massal)  
- Auth: OIDC (Keycloak / Okta / Azure AD), TOTP (Google Authenticator/Authy)  

**Frontend**
- Framework: [React.js](https://react.dev/) + [Vite](https://vitejs.dev/) atau [Next.js](https://nextjs.org/)  
- Bahasa: [TypeScript](https://www.typescriptlang.org/)  
- Terminal Web: [xterm.js](https://xtermjs.org/)  
- UI: [Tailwind CSS](https://tailwindcss.com/) + [shadcn/ui](https://ui.shadcn.com/)  
- State/Data: [TanStack Query](https://tanstack.com/query)  

**Infra & Observability**
- Container: Docker  
- Orkestrasi: Kubernetes (Helm chart opsional)  
- Ingress: NGINX / Traefik  
- Monitoring: OpenTelemetry + Prometheus + Grafana  
- Logging: ELK stack atau Loki  

---

## 📋 Prasyarat

Sebelum menjalankan aplikasi ini, pastikan:

- **Go** ≥ 1.21  
- **Node.js** ≥ 18 + npm atau yarn  
- **PostgreSQL** ≥ 14  
- **Redis** ≥ 6  
- **Docker** (opsional, untuk containerization)  
- **Vault** sudah tersedia di server terpisah (tidak dikelola oleh aplikasi ini)  
- **OIDC Provider** (contoh: Keycloak, Okta, Azure AD) bila ingin mengaktifkan SSO  
