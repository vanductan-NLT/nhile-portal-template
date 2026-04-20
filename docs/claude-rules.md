# Claude Code Rules — NhiLe Portal

## BẮT BUỘC đọc và chạy đầu mỗi session

### 1. Health check
Chạy lệnh sau trước khi làm bất cứ thứ gì:

npx @nhile/cli doctor

- Nếu output "update-available" → DỪNG, báo user chạy `nhile update-template` trước
- Nếu output "ok" → tiếp tục

### 2. Đọc architecture
- Đọc docs/architecture.md
- Đây là source of truth cho toàn bộ portal
- Không build feature nào không có trong architecture

### 3. Commit convention
- Mọi commit phải theo Conventional Commits
- Format: type(scope): message
- Types: feat, fix, chore, docs, refactor, test
- Không push thẳng main. Mọi thay đổi qua branch + PR

### 4. Branch strategy
- main: production only
- dev: integration
- incoming: Claude Code làm việc tại đây
- Flow: incoming → PR → dev → PR → main
