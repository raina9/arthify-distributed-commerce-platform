# Pagination & Sorting Roadmap

## Objective

Implement pagination and sorting in Arthify User Service, progressing from Spring Data JPA pagination to Offset/Limit and Cursor/Keyset pagination.

Focus on implementation, SQL/database behavior, performance, consistency, and interview readiness.

---

## Implementation Checklist

### Foundation
- [ ] MySQL connectivity
- [ ] User & Address entities
- [ ] Repository
- [ ] Service
- [ ] Controller
- [ ] Basic User API
- [ ] Verify generated SQL

### Spring Data Pagination
- [ ] `Pageable`
- [ ] `Page<T>`
- [ ] Page number & size
- [ ] Sorting
- [ ] Multiple-column sorting
- [ ] Zero-based pages
- [ ] Count queries
- [ ] Stable ordering
- [ ] Pagination validation
- [ ] Maximum page size

### Offset / Limit
- [ ] `LIMIT`
- [ ] `OFFSET`
- [ ] Explicit Offset/Limit API
- [ ] Deep-offset behavior
- [ ] Index impact
- [ ] Query analysis

### Cursor / Keyset
- [ ] Stable ordering key
- [ ] Indexed key
- [ ] Keyset predicate
- [ ] Cursor encoding/decoding
- [ ] Cursor validation
- [ ] Tie-breaking
- [ ] Composite ordering
- [ ] Offset vs Keyset comparison

### Search & JOINs
- [ ] Search + pagination
- [ ] Search + sorting
- [ ] User + Address JOIN pagination
- [ ] JOIN duplication handling
- [ ] Count-query behavior

### Production
- [ ] DTOs
- [ ] Request validation
- [ ] Sorting-field validation
- [ ] Error handling
- [ ] Database indexes
- [ ] Execution plans
- [ ] Performance testing
- [ ] Unit tests
- [ ] Integration tests
- [ ] Logging / observability

---

# Pagination & Sorting Interview Questions

## Core Questions

- [ ] 1. How do you implement pagination in Spring Boot?
- [ ] 2. How do you implement sorting along with pagination?
- [ ] 3. What is Pageable? What is Page?
- [ ] 4. Page vs Slice ?
- [ ] 5. Offset Pagination vs Cursor (Keyset) Pagination ?
- [ ] 6. Why does OFFSET pagination become slow for large datasets?
- [ ] 7. How do you implement pagination and sorting in your project?

## Scenario-Based Questions

- [ ] 8. Your table has 100 million records. OFFSET pagination has become very slow. How would you optimize it?
- [ ] 9. Why does OFFSET pagination become slower as the page number increases?
- [ ] 10. When would you choose Cursor (Keyset) Pagination over OFFSET Pagination?
- [ ] 11. A user is browsing page 5, and meanwhile new records are inserted. The user starts seeing duplicate or missing records. Why does this happen, and how would you fix it?
- [ ] 12. How would you implement pagination and sorting together in Spring Boot?
- [ ] 13. The UI allows sorting by multiple columns (e.g., salary DESC, name ASC). How would you implement it?
- [ ] 14. How would you paginate a REST API? What request parameters and response structure would you return?
- [ ] 15. Should pagination happen in the database or in Java? Why?
- [ ] 16. A client requests 10,000 records in a single API call. How would you handle it?
- [ ] 17. How would you paginate search results while maintaining consistent ordering?
- [ ] 18. How would you optimize a paginated query that is still slow even after adding pagination?
- [ ] 19. A paginated API works fine in development but becomes slow in production with millions of records. How would you troubleshoot it?
- [ ] 20. Would you use Page or Slice in Spring Data JPA? When and why?
- [ ] 21. How would you implement pagination if the data is coming from multiple tables using JOINs?
- [ ] 22. How would you implement infinite scrolling in a web application?

---

## Definition of Done

- [ ] Spring Data pagination implemented
- [ ] Sorting implemented
- [ ] Offset/Limit implemented
- [ ] Cursor/Keyset implemented
- [ ] Search + pagination implemented
- [ ] JOIN + pagination implemented
- [ ] Stable ordering enforced
- [ ] Indexes and execution plans analyzed
- [ ] Performance compared
- [ ] Tests completed
- [ ] All 22 interview questions can be explained using this project

### Rule

Do not skip pagination approaches. Implement them, understand the SQL/database behavior and trade-offs, and then mark the relevant interview questions as complete.