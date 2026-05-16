# Review Categories Checklist

## 1. Business Logic Review
- **Correctness**: Does the logic correctly implement the requirement?
- **Edge Cases**: Are boundary conditions handled?
- **Failure Handling**: What happens when things go wrong? (nil/null handling, retries).
- **Consistency**: Are state transitions and transactions handled reliably?
- **Validation**: Are input rules strictly enforced?

## 2. Architecture Review
- **Consistency**: Does it follow the established architectural patterns?
- **Boundaries**: Are module boundaries and domain separation respected?
- **Coupling**: Are there circular dependencies or God objects?
- **Logic Placement**: Is business logic in the right layer (e.g., Service vs Model)?
- **Patterns**: Quality of repository patterns, event handling, and background jobs.

## 3. DRY / Clean Code Review
- **Duplication**: Repeated queries, conditions, or transformations.
- **Naming**: Clarity and intent of variable/function names.
- **Complexity**: Method/class size and nesting depth.
- **Magic Values**: Use of hardcoded strings or numbers.
- **Over/Under Engineering**: Is the solution appropriately complex for the problem?

## 4. Security Review
- **AuthZ/AuthN**: Proper permission checks and tenant isolation.
- **Injections**: SQLi, XSS, CSRF, SSRF, and command execution risks.
- **Secrets**: Exposing keys, tokens, or sensitive data in logs/code.
- **Validation**: Mass assignment and insecure redirects.
- **Integrations**: Security of webhooks and external API calls.

## 5. Database & Query Review
- **Migrations**: Indexing, constraints, and table rewrite risks.
- **Performance**: N+1 queries, missing eager loading, and locking issues.
- **Scalability**: Non-paginated queries and large memory loads.
- **Compatibility**: Rollback safety and backward compatibility.

## 6. API & Contract Review
- **Consistency**: Request/response naming and status codes.
- **Breaking Changes**: Backward compatibility of schema changes.
- **Serialization**: Efficiency and correctness of data transfer.
- **Documentation**: Are contract changes documented?

## 7. Performance Review
- **Complexity**: Algorithm efficiency and unnecessary allocations.
- **Bottlenecks**: Synchronous blocking operations and expensive loops.
- **Caching**: Opportunities for improvement.

## 8. Concurrency & Reliability Review
- **Safety**: Race conditions and thread safety.
- **Reliability**: Idempotency, timeout handling, and partial failure states.
- **Async**: Consistency across asynchronous workflows.

## 9. Observability Review
- **Logging**: Quality, context, and avoidance of sensitive data.
- **Metrics/Tracing**: Support for operational visibility.
- **Debuggability**: Is the code easy to troubleshoot in production?

## 10. Testing Review
- **Coverage**: Unit/integration tests for critical business paths and edge cases.
- **Quality**: Flaky tests and weak assertions.
- **Failure Paths**: Testing how the system handles errors and security threats.

## 11. Dependency Review
- **Risks**: Vulnerable, outdated, or oversized packages.
- **Necessity**: Is the new library actually required?
