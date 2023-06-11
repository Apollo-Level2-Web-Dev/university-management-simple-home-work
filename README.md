# university-management-simple-home-work
## Practice Task: Complete Faculty Module

1. Generate faculty utility function to create faculty incremental id.
   - Pattern: F-00001

2. Create `/create-faculty` route in `user.route.ts` file.

3. Validate Create Faculty Request in router level.

4. Create Faculty controller and service in `user.controller.ts` & `user.service.ts`.

5. Create API End Points in `faculty.route.ts` given below (Do not forget to add it in `routes/index.ts` file):
   - `/api/v1/faculties` (GET) → Get all faculties, implement filtering and pagination, populate reference field.
   - `/api/v1/faculties/:id` (GET) → Get individual faculty by ID and populate reference field.
   - `/api/v1/faculties/:id` (PATCH) → Update faculty data dynamically.
   - `/api/v1/faculties/:id` (DELETE) → Delete individual faculty.

6. Validate Update request using Zod schema.

7. Create faculty controllers and services.

8. Test APIs and Create Data.
