# 子法：DDD 架構規範

> 父法：CONSTITUTION.md 第一章

## 第 1 條：目錄結構

```
src/
├── Domain/                    # 領域層（核心）
│   ├── Entities/              # 實體
│   ├── ValueObjects/          # 值物件
│   ├── Aggregates/            # 聚合根
│   ├── DomainServices/        # 領域服務
│   ├── DomainEvents/          # 領域事件
│   └── Repositories/          # Repository 介面（僅介面）
│
├── Application/               # 應用層
│   ├── UseCases/              # 用例
│   ├── DTOs/                  # 資料傳輸物件
│   ├── Services/              # 應用服務
│   └── Interfaces/            # 外部服務介面
│
├── Infrastructure/            # 基礎設施層
│   ├── Persistence/           # DAL 資料存取
│   │   ├── Repositories/      # Repository 實作
│   │   ├── DbContext/         # 資料庫上下文
│   │   └── Migrations/        # 資料遷移
│   ├── ExternalServices/      # 外部服務實作
│   └── Messaging/             # 訊息佇列
│
└── Presentation/              # 呈現層
    ├── API/                   # REST API
    ├── GraphQL/               # GraphQL（可選）
    └── CLI/                   # 命令列介面
```

## 第 2 條：依賴方向

```
Presentation → Application → Domain
                    ↓
              Infrastructure
```

- Domain 不依賴任何外層
- Infrastructure 實作 Domain 定義的介面

## 第 3 條：DAL 規範

### 3.1 Repository 介面（在 Domain 層）
```python
# Domain/Repositories/IUserRepository.py
class IUserRepository(ABC):
    @abstractmethod
    def get_by_id(self, id: UserId) -> Optional[User]: ...
    
    @abstractmethod
    def save(self, user: User) -> None: ...
```

### 3.2 Repository 實作（在 Infrastructure 層）
```python
# Infrastructure/Persistence/Repositories/UserRepository.py
class UserRepository(IUserRepository):
    def __init__(self, db_context: DbContext):
        self._db = db_context
    
    def get_by_id(self, id: UserId) -> Optional[User]:
        # 實際資料庫操作
        ...
```

## 第 4 條：命名慣例

| 類型 | 命名規則 | 範例 |
|------|----------|------|
| Entity | 名詞單數 | `User`, `Order` |
| Value Object | 描述性名詞 | `EmailAddress`, `Money` |
| Repository | `I{Entity}Repository` | `IUserRepository` |
| Use Case | 動詞 + 名詞 | `CreateOrder`, `GetUserById` |
| Domain Event | 過去式 | `OrderCreated`, `UserRegistered` |
