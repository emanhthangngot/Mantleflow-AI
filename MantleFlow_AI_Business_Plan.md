# MANTLEFLOW AI
## Kế Hoạch Kinh Doanh (Business Plan)

---

**Thông tin tài liệu**

| Trường | Nội dung |
|--------|----------|
| Tên dự án | MantleFlow AI |
| Phiên bản | 1.2 |
| Ngày lập | 11/01/2026 |
| Phân loại | Tài liệu nội bộ |
| Người nhận | Ban Giám Khảo Hackathon |

---

## Mục lục

1. [Tóm tắt Điều hành (Executive Summary)](#1-tom-tat-dieu-hanh)
2. [Vấn đề & Giải pháp (Problem & Solution)](#2-van-de-va-giai-phap)
3. [Kiến trúc Công nghệ (Technology Architecture)](#3-kien-truc-cong-nghe)
4. [Phân tích Thị trường (Market Analysis)](#4-phan-tich-thi-truong)
5. [Mô hình Kinh doanh (Business Model)](#5-mo-hinh-kinh-doanh)
6. [Lộ trình Phát triển (Product Roadmap)](#6-lo-trinh-phat-trien)
7. [Tokenomics](#7-tokenomics)
8. [Quản lý Rủi ro & Bảo mật (Risk Management & Security)](#8-quan-ly-rui-ro-va-bao-mat)
9. [Cấu trúc Đội ngũ (Team Structure)](#9-cau-truc-doi-ngu)
10. [Dự phóng Tài chính (Financial Projections)](#10-du-phong-tai-chinh)
11. [Kết luận (Conclusion)](#11-ket-luan)

---

## 1. Tóm tắt Điều hành

**MantleFlow AI** là nền tảng tài chính phi tập trung (DeFi) tiên phong trong lĩnh vực Invoice Factoring (bao thanh toán hóa đơn), được xây dựng trên **Mantle Network**. Dự án kết hợp sức mạnh minh bạch của Blockchain với khả năng phân tích dữ liệu của Trí tuệ nhân tạo (AI) để giải quyết bài toán thanh khoản cho Doanh nghiệp vừa và nhỏ (SMEs).

**Giá trị Cốt lõi (Core Value Proposition):**
- **Instant Liquidity**: Cấp vốn nhanh chóng cho SMEs thông qua việc token hóa hóa đơn thành NFT.
- **AI-Powered Risk Scoring**: Hệ thống đánh giá tín dụng tự động với 8 chỉ số rủi ro chuyên sâu.
- **OSINT Anti-Fraud**: Sử dụng Open Source Intelligence để phát hiện gian lận và công ty ma.
- **On-chain Transparency**: Mọi giao dịch, lịch sử tín dụng và tranh chấp đều được ghi nhận minh bạch trên Blockchain.

**Mục tiêu Năm đầu tiên (Key Metrics Year 1):**
- Tổng giá trị khóa (TVL): $10,000,000
- Người dùng hoạt động (Active Users): 3,000 SMEs
- Tỷ lệ nợ xấu (Default Rate): Dưới 2%
- Doanh thu (Revenue): $425,000

---

## 2. Vấn đề & Giải pháp

### 2.1 Thách thức của SMEs (The Problem)
Các doanh nghiệp vừa và nhỏ tại Việt Nam và khu vực đang đối mặt với áp lực dòng tiền nghiêm trọng:
- **Chu kỳ thanh toán dài**: Thời gian chờ thanh toán trung bình từ 30-90 ngày.
- **Tiếp cận vốn khó khăn**: Ngân hàng truyền thống yêu cầu tài sản thế chấp và hồ sơ tín dụng phức tạp.
- **Thị trường Factoring kém hiệu quả**: Phí cao, quy trình thủ công kéo dài 2-4 tuần, và thiếu minh bạch.

### 2.2 Giải pháp MantleFlow AI (The Solution)
Chúng tôi cung cấp giải pháp toàn diện bao gồm:
1.  **Tokenization**: Chuyển đổi hóa đơn giấy thành tài sản số (Invoice NFT) có thể giao dịch.
2.  **Automated Due Diligence**: Sử dụng AI để thẩm định hóa đơn và doanh nghiệp chỉ trong vài giây.
3.  **DeFi Lending Pool**: Kết nối trực tiếp người vay (SMEs) với người cho vay (Liquidity Providers) thông qua Smart Contracts, loại bỏ trung gian.

---

## 3. Kiến trúc Công nghệ

Hệ thống MantleFlow AI được xây dựng trên 4 trụ cột công nghệ chính:

### 3.1 Backend Architecture (Hệ thống Thanh Toán & Quản lý)
Hệ thống Backend được xây dựng trên nền tảng .NET Core mạnh mẽ, đảm nhiệm logic nghiệp vụ phức tạp về thanh toán và quản lý khoản vay.

**Technology Stack:**
- **Framework**: ASP.NET Core 8.0 Web API (High performance).
- **Database**: PostgreSQL kết hợp Entity Framework Core (Code-first migration).
- **Blockchain Integration**: Nethereum để tương tác với Smart Contracts.
- **Authentication**: JWT Bearer Token + ASP.NET Identity.

**Các Modules Chính:**
1.  **Loan Controller**: Quản lý vòng đời khoản vay (Create, Repay, Default).
2.  **Oracle Controller**: Xử lý logic thanh toán off-chain và đồng bộ trạng thái on-chain.
3.  **Payment Gateway Integration**: Kết nối cổng thanh toán để nhận tiền fiat từ SMEs.
4.  **Swagger Documentation**: Cung cấp tài liệu API trực quan cho Frontend và đối tác tích hợp.

### 3.2 AI Engine (Trí tuệ Nhân tạo)
- **OCR Service**: Sử dụng Google Gemini 1.5 Flash để trích xuất dữ liệu từ hóa đơn (PDF/Image) với độ chính xác cao đối với format tiếng Việt.
- **Risk Scoring Model**: Thuật toán đánh giá 8 yếu tố (Wallet age, Transaction volume, Business age...) để phân loại Tier tín dụng (A/B/C/D).
- **OSINT Checker**: Hệ thống rà soát 5 điểm chạm số (Website, LinkedIn, Maps, News, Social) để phát hiện công ty ma.
- **AI Agent (FastAPI)**: Microservice độc lập phục vụ các tác vụ AI chuyên sâu.

### 3.3 Smart Contracts (Blockchain)
Triển khai trên **Mantle Sepolia Testnet** (Solidity 0.8.20):
- `InvoiceNFT`: Token chuẩn ERC-721 lưu trữ metadata hóa đơn.
- `LendingPool`: Quản lý vay/trả, lãi suất theo Tier.
- `PaymentOracle`: Cơ chế Multi-sig (2/3) xác thực thanh toán off-chain.
- `Liquidator`: Cơ chế đấu giá ngược (Dutch Auction) để thanh lý tài sản khi nợ xấu.

### 3.4 Frontend (Giao diện Người dùng)
- **Framework**: ReactJS + Vite + TypeScript.
- **UI Library**: Ant Design 5.0 (Enterprise-grade UI).
- **Web3 Integration**: wagmi + viem cho kết nối ví và tương tác Blockchain.

---

## 4. Phân tích Thị trường

### 4.1 Quy mô Thị trường (Market Size)
- **Toàn cầu**: Thị trường Factoring đạt $4.1 nghìn tỷ năm 2024.
- **Việt Nam**: Hơn 800,000 SMEs đóng góp 40% GDP, nhưng 70% gặp khó khăn tiếp cận vốn.
- **DeFi RWA**: Tổng giá trị tài sản thực (RWA) on-chain dự kiến đạt $16 nghìn tỷ vào năm 2030 (BCG Report).

### 4.2 Lợi thế Cạnh tranh (Competitive Advantage)
| Tiêu chí | Ngân hàng Truyền thống | DeFi Lending (Aave/Compound) | MantleFlow AI |
|----------|------------------------|------------------------------|---------------|
| **Tài sản đảm bảo** | Bất động sản | Crypto (Over-collateralized) | **Hóa đơn thực (RWA)** |
| **Thời gian duyệt** | 2-4 tuần | Tức thì | **< 24 giờ** |
| **Lãi suất** | 10-15% | Biến động mạnh | **Cạnh tranh (5-12%)** |
| **Minh bạch** | Thấp | Cao | **Cao (On-chain)** |
| **Thẩm định** | Thủ công | Không có | **AI + OSINT (Tự động)** |

---

## 5. Mô hình Kinh doanh

MantleFlow AI hoạt động theo mô hình thu phí giao dịch B2B:

### 5.1 Các dòng Doanh thu (Revenue Streams)
1.  **Origination Fee (Phí khởi tạo)**: 1% giá trị khoản vay (thu từ người vay).
2.  **Interest Spread (Chênh lệch lãi suất)**: 20% trên tổng lãi suất thực thu.
3.  **Liquidation Fee (Phí thanh lý)**: 5% giá trị thu hồi từ đấu giá tài sản.
4.  **Premium Subscription**: $500/tháng cho gói Enterprise (API access, Priority support).

### 5.2 Unit Economics (Trên mỗi khoản vay $50,000)
- **Doanh thu phí (1%)**: $500
- **Lãi suất chia sẻ (Est.)**: $164
- **Tổng doanh thu**: **$664 / khoản vay**
- **Chi phí trực tiếp (Gas, AI, Ops)**: ~$50
- **Lợi nhuận gộp**: **$614 (Margin ~92%)**

---

## 6. Lộ trình Phát triển

### Phase 1: MVP & Validation (Q1 2026) - **Hiện tại**
- [x] Hoàn thiện 7 Smart Contracts cốt lõi.
- [x] Tích hợp AI Engine (OCR, Risk, OSINT).
- [x] Triển khai Backend .NET Core cho logic thanh toán.
- [ ] Hoàn tất Frontend Integration.
- [ ] Security Audit & Mainnet Launch.

### Phase 2: User Acquisition (Q2 2026)
- Chương trình Pilot với 10 doanh nghiệp VNR500.
- Tích hợp KYC Providers (Jumio/Onfido).
- Ra mắt Mobile App (iOS/Android) cho SMEs.
- Đạt cột mốc $1M TVL.

### Phase 3: Scale & Expansion (Q3-Q4 2026)
- Mở rộng Multi-chain (Arbitrum, Optimism).
- Hỗ trợ Cross-border Factoring (Việt Nam - ASEAN).
- Ra mắt tính năng Fractional NFTs (chia nhỏ khoản vay).
- Phát hành MFL Governance Token.

---

## 7. Tokenomics

**MFL Token** là token quản trị và tiện ích của hệ sinh thái, tổng cung 100,000,000 token.

**Phân bổ (Allocation):**
- **Ecosystem Growth**: 30% (Khuyến khích người dùng).
- **Team & Advisors**: 20% (Vesting 4 năm).
- **Investors**: 20% (Vesting 2 năm).
- **Treasury**: 15% (Dự trữ chiến lược).
- **Liquidity**: 15% (Thanh khoản ban đầu).

**Tiện ích (Ultility):**
- **Governance**: Bỏ phiếu thay đổi tham số hệ thống.
- **Staking**: Stake MFL để tăng hạn mức vay (LTV) lên tới +10%.
- **Fee Discount**: Giảm phí giao dịch cho người nắm giữ token.

---

## 8. Quản lý Rủi ro & Bảo mật

### 8.1 Bảo mật Smart Contract
- **Audit**: Hợp tác với các đơn vị audit hàng đầu trước khi mainnet.
- **Challenge Period**: Cơ chế "thời gian thách thức" 24h cho phép cộng đồng khiếu nại khoản vay gian lận trước khi giải ngân.
- **Multi-sig**: Yêu cầu 2/3 chữ ký oracle cho các giao dịch quan trọng.

### 8.2 Kiểm soát Rủi ro Tín dụng (Credit Risk)
- **AI Screening**: Loại bỏ 90% hồ sơ rác tự động.
- **Fraud Detection**: Phát hiện công ty ma thông qua OSINT (Web, Social, News).
- **Insurance Fund**: Trích lập 5% doanh thu vào quỹ bảo hiểm để đền bù trong trường hợp nợ xấu.

---

## 9. Cấu trúc Đội ngũ

### Đội ngũ Hiện tại (Core Team)
- **Smart Contract Lead**: Phụ trách Blockchain architecture và security.
- **Backend Lead (.NET)**: Phụ trách Payment logic, Database, System Architecture.
- **Frontend & AI Lead**: Phụ trách UX/UI, AI models và OSINT algorithms.

### Kế hoạch Mở rộng (Hiring Plan Q2 2026)
- **Product Manager**: Định hướng chiến lược sản phẩm.
- **Business Development (BD)**: Phát triển đối tác doanh nghiệp và quỹ đầu tư.
- **Legal & Compliance**: Đảm bảo tuân thủ pháp lý tài chính.

---

## 10. Dự phóng Tài chính

| Chỉ số (USD) | Năm 1 | Năm 2 | Năm 3 |
|--------------|-------|-------|-------|
| **Tổng khoản vay (Volume)** | $10M | $50M | $200M |
| **Doanh thu (Revenue)** | $425,000 | $2,000,000 | $7,500,000 |
| **Chi phí (Expenses)** | $600,000 | $1,340,000 | $2,550,000 |
| **Lợi nhuận ròng (Net Income)** | ($175,000) | $660,000 | $4,950,000 |

*Ghi chú: Năm 1 tập trung vào tăng trưởng người dùng và hoàn thiện sản phẩm, dự kiến hòa vốn vào giữa Năm 2.*

---

## 11. Kết luận

MantleFlow AI không chỉ là một ứng dụng DeFi, mà là cầu nối quan trọng giữa Tài chính truyền thống (TradFi) và Tài chính phi tập trung. Với công nghệ Blockchain minh bạch và sự hỗ trợ mạnh mẽ của AI, chúng tôi tự tin giải quyết bài toán thanh khoản cho hàng triệu doanh nghiệp SMEs, mở ra kỷ nguyên mới cho tài chính chuỗi cung ứng.

---
*Hết tài liệu*
