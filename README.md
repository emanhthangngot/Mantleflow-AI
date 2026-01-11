# MantleFlow AI - Full Project Setup & Guide

Hướng dẫn cài đặt và chạy toàn bộ dự án MantleFlow AI gồm 3 thành phần chính:
1.  **AI Engine** (FastAPI Python - Backend & AI Logic)
2.  **Frontend** (ReactJS + Vite - User Interface)
3.  **Smart Contracts** (Mantle Network - Blockchain Layer)

---

## 🏗️ 1. Prerequisites (Yêu cầu hệ thống)

Hãy đảm bảo bạn đã cài đặt các công cụ sau:
- **Node.js** v18+ (cho Frontend)
- **Python** 3.10+ (cho AI Engine)
- **Foundry** (Forge, Cast) (cho Smart Contracts)
- **Git**

---

## 🤖 2. AI Engine & Backend Setup

Dịch vụ này cung cấp API cho OCR, Risk Scoring, và OSINT check.

**Thư mục:** `ai-engine/`

### Bước 1: Khởi tạo môi trường Python
```bash
cd ai-engine
# Tạo virtual environment
python -m venv venv

# Activate (Windows)
.\venv\Scripts\activate
# Activate (Mac/Linux)
source venv/bin/activate
```

### Bước 2: Cài đặt thư viện
```bash
pip install -r requirements.txt
```

### Bước 3: Cấu hình Environment
Tạo file `.env` từ `.env.example` (nếu có) và điền API Key (Gemini API Key).

### Bước 4: Chạy Server
```bash
# Chạy server với Uvicorn (Hot reload)
uvicorn app.main:app --reload --port 8000
```
*API sẽ chạy tại: `http://localhost:8000`*
*Docs (Swagger UI): `http://localhost:8000/docs`*

---

## 💻 3. Frontend Setup

Giao diện người dùng web application.

**Thư mục:** `frontend/`

### Bước 1: Cài đặt dependencies
```bash
cd frontend
npm install
```

### Bước 2: Chạy Development Server
```bash
npm run dev
```
*App sẽ chạy tại: `http://localhost:5173` (hoặc port hiển thị trên terminal)*

---

## ⛓️ 4. Smart Contracts Setup

Triển khai và kiểm thử Smart Contracts trên Mantle Network.

**Thư mục:** `mantleflow-contracts/`

### Bước 1: Cài đặt dependencies
```bash
cd mantleflow-contracts
forge install
```

### Bước 2: Compile & Test
```bash
# Build contracts
forge build

# Run tests
forge test
```

### Bước 3: Deploy (Mantle Sepolia)
```bash
# Tạo file .env và điền PRIVATE_KEY
cp .env.example .env

# Deploy script
forge script script/Deploy.s.sol:Deploy --rpc-url https://rpc.sepolia.mantle.xyz --broadcast
```

---

## 🚀 5. Quick Start (Chạy cả 3 cùng lúc)

Mở 3 cửa sổ Terminal riêng biệt:

**Terminal 1 (AI Engine):**
```bash
cd ai-engine
.\venv\Scripts\activate
uvicorn app.main:app --reload
```

**Terminal 2 (Frontend):**
```bash
cd frontend
npm run dev
```

**Terminal 3 (Contracts - Optional):**
```bash
cd mantleflow-contracts
forge test
```

---

## 📂 Project Structure

```
Mantleflow-AI/
├── ai-engine/              # Python FastAPI Backend + AI Models
│   ├── app/                # Source code
│   └── requirements.txt    # Dependencies
├── frontend/               # ReactJS + Vite App
│   ├── src/                # Components & Pages
│   └── package.json        # Dependencies
└── mantleflow-contracts/   # Solidity Smart Contracts
    ├── src/                # Contract Sources (InvoiceNFT, LendingPool...)
    └── script/             # Defloyment Scripts
```

---

## 📝 Notes for Judges/Reviewers

- **Backend Logic**: Hiện tại logic Backend được tích hợp trực tiếp trong `ai-engine` (FastAPI) để phục vụ Hackathon nhanh chóng.
- **Data**: Hệ thống sử dụng dữ liệu mẫu hoặc mock data nếu chưa kết nối Database production.
- **Smart Contracts**: Đã deploy trên Mantle Sepolia Testnet.

---
*MantleFlow AI Team - Hackathon 2026*
