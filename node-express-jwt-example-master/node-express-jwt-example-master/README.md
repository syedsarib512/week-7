# Node Express JWT Authentication / Authorization Example

An example project implementing JWT authentication and role based authorization.

### Demo Setup
3. Install dependencies with `npm install`.
4. Run migrations and seed that Sqlite database with `sequelize db:migrate` and `sequelize db:seed:all`.
5. Run the project with `node index.js`.

### Default Credentials

| Username | Password | Description |
| - | - | - |
| admin | admin | User with `ADMIN` and `USER` roles. |
| user | user | User with only `USER` role. |

### Default Routes

| Path | Method | Description |
| - | - | - |
| `/auth` | `POST` | Authenticate user, returns JWT token.  Jwt token can the be place in `Authorization` header prefixed with `Bearer`|
| `/users` | `GET` | List all users [requires ADMIN role] |
| `/users` | `POST` | Create new user [requires ADMIN role] |
| `/api/v1/restricted/usersOnly` | `GET` | Users only path |
| `/api/v1/restricted/adminOnly` | `GET` | Admin only path |



Developer:
Syed Sarib Naveed
