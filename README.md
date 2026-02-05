# Armbian Build for Q9S RK3128 Android TV Box

Build Armbian 22.08.2 Bullseye với Linux 4.4.x cho Q9S Android TV Box (TXCZ-RK3128-V3.1).

## 🚀 Quick Start

### Tự động build trên GitHub Actions
1. Fork repository này
2. Vào **Actions** → **Build Armbian for Q9S RK3128**
3. Click **Run workflow** → Chọn options → **Run**
4. Chờ 2-4 giờ, download image từ **Artifacts** hoặc **Releases**

## 📁 Cấu Trúc Project

```
armbian-q9s-rk3128/
├── .github/workflows/
│   └── build-armbian.yml      # GitHub Actions workflow
├── userpatches/
│   ├── config-default.conf    # Default options
│   └── lib.config             # Library overrides
├── config/
│   └── boards/
│       └── q9s-rk3128.wip     # Board configuration
└── README.md
```

## 📋 Thông Số

| Item | Value |
|------|-------|
| **Chip** | Rockchip RK3128 (ARM Cortex-A7 quad-core) |
| **Board** | TXCZ-RK3128-V3.1 |
| **Model** | Q9S Android TV Box |
| **Kernel** | Linux 4.4.x (legacy) |
| **Distro** | Debian 11 Bullseye |
| **Armbian** | v22.08.2 |
| **Architecture** | armhf (32-bit) |

## 🔧 Flash Image

### Yêu cầu
- [RKDevTool](https://github.com/nickmullaney/RK3128-Documentation) (Windows)
- [rkdeveloptool](https://github.com/rockchip-linux/rkdeveloptool) (Linux)

### Các bước
1. Download image từ Releases
2. Giải nén `.img.xz` → `.img`
3. Boot Q9S vào **Maskrom mode**:
   - Cắm USB OTG vào máy tính
   - Nhấn giữ nút Recovery + cắm nguồn
4. Flash image bằng RKDevTool

## ⚠️ Lưu Ý

- Backup firmware gốc trước khi flash!
- RK3128 chỉ hỗ trợ 32-bit (armhf)
- Một số tính năng có thể không hoạt động do kernel legacy

## 📝 License

MIT License - Tự do sử dụng và chỉnh sửa.
