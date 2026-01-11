# MantleFlow AI - Full Project Setup & Guide

Hướng dẫn cài đặt và chạy toàn bộ dự án MantleFlow AI gồm 4 thành phần chính:
1.  **AI Engine** (FastAPI Python - Backend & AI Logic)
2.  **Payment Backend** (ASP.NET Core - Payment & Loan Logic)
3.  **Frontend** (ReactJS + Vite - User Interface)
4.  **Smart Contracts** (Mantle Network - Blockchain Layer)

---

## 🏗️ 1. Prerequisites (Yêu cầu hệ thống)

Hãy đảm bảo bạn đã cài đặt các công cụ sau:
- **Node.js** v18+ (cho Frontend)
- **Python** 3.10+ (cho AI Engine)
- **.NET SDK** 8.0 (cho Payment Backend)
- **Foundry** (Forge, Cast) (cho Smart Contracts)
- **PostgreSQL** (Database)

---

## 🤖 2. AI Engine Setup (Python)

Dịch vụ này cung cấp API cho OCR, Risk Scoring, và OSINT check.

**Thư mục:** `ai-engine/`

1.  **Cài đặt môi trường**:
    ```bash
    cd ai-engine
    python -m venv venv
    # Windows:
    .\venv\Scripts\activate
    # Mac/Linux:
    source venv/bin/activate
    ```

2.  **Cài đặt thư viện & Cấu hình**:
    ```bash
    pip install -r requirements.txt
    # Tạo file .env và điền GEMINI_API_KEY
    ```

3.  **Chạy Server**:
    ```bash
    uvicorn app.main:app --reload --port 8000
    ```
    *API chạy tại: `http://localhost:8000`*

---

## 💳 3. Payment Backend Setup (.NET Core)

Dịch vụ xử lý logic thanh toán, quản lý khoản vay và xác thực người dùng.

**Thư mục:** `BE/BE/`

1.  **Cấu hình Database**:
    Mở file `BE/BE/appsettings.json` và cập nhật `ConnectionStrings:DefaultConnection` với thông tin PostgreSQL của bạn:
    ```json
    "DefaultConnection": "Host=localhost;Port=5432;Database=HackathonDb;Username=postgres;Password=yourpassword"
    ```

2.  **Chạy Server**:
    ```bash
    cd BE/BE
    dotnet restore
    dotnet run
    ```
    *API chạy tại: `http://localhost:5000` (hoặc port hiển thị)*
    *Swagger Docs: `http://localhost:5000/swagger`*

---

## 💻 4. Frontend Setup (React)

Giao diện người dùng web application.

**Thư mục:** `frontend/`

1.  **Cài đặt & Chạy**:
    ```bash
    cd frontend
    npm install
    npm run dev
    ```
    *App chạy tại: `http://localhost:5173`*

---

## ⛓️ 5. Smart Contracts Setup (Foundry)

Triển khai Smart Contracts trên Mantle Network.

**Thư mục:** `mantleflow-contracts/`

1.  **Build & Test**:
    ```bash
    cd mantleflow-contracts
    forge build
    forge test
    ```

2.  **Deploy**:
    ```bash
    cp .env.example .env # Điền Private Key
    forge script script/Deploy.s.sol:Deploy --rpc-url https://rpc.sepolia.mantle.xyz --broadcast
    ```

---

## 🚀 6. Quick Start (Chạy toàn bộ dự án)

Mở 4 cửa sổ Terminal riêng biệt:

**Terminal 1 (AI Engine):**
```bash
cd ai-engine
.\venv\Scripts\activate
uvicorn app.main:app --reload
```

**Terminal 2 (Payment BE):**
```bash
cd BE/BE
dotnet run
```

**Terminal 3 (Frontend):**
```bash
cd frontend
npm run dev
```

**Terminal 4 (Contracts):**
```bash
cd mantleflow-contracts
forge test
```

---

## 📂 Project Structure

```
Mantleflow-AI/
├── ai-engine/              # Python FastAPI (AI Models)
├── BE/                     # ASP.NET Core API (Payment Backend)
│   └── BE/                 # Source code (Controllers, Models)
├── frontend/               # ReactJS + Vite App
└── mantleflow-contracts/   # Solidity Smart Contracts
```

---
*MantleFlow AI Team - Hackathon 2026*
