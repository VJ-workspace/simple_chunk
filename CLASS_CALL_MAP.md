
# Definitions

AuthController -> src/controllers/auth_controller.py
OrderController -> src/controllers/order_controller.py
PaymentController -> src/controllers/payment_controller.py

AuthService -> src/services/auth_service.py
OrderService -> src/services/order_service.py
PaymentService -> src/services/payment_service.py
InventoryService -> src/services/inventory_service.py

UserRepository -> src/repositories/user_repository.py
OrderRepository -> src/repositories/order_repository.py
InventoryRepository -> src/repositories/inventory_repository.py

JwtHelper -> src/utils/jwt_helper.py
AuditLogger -> src/utils/audit_logger.py

# Usage Chain

AuthController
 -> AuthService
    -> UserRepository
    -> JwtHelper

OrderController
 -> OrderService
    -> InventoryService
       -> InventoryRepository
    -> OrderRepository

PaymentController
 -> PaymentService
    -> UserRepository
