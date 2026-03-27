# DID Key Recovery Extension (DID-KR)

A standardized extension for Decentralized Identifiers (DIDs) enabling secure, interoperable key recovery through three complementary mechanisms:

**Type A — Social ZKP Recovery:** Threshold guardians with zero-knowledge proofs, implementing Feldman Verifiable Secret Sharing (VSS) with Schnorr proofs for share verification and proactive share refreshment to prevent cryptographic key lifecycle failures.

**Type B — Deterministic Seedling Inheritance:** Hierarchical Deterministic (HD) seeds with Verifiable Delay Function (VDF) time-locks, providing cryptographically enforced temporal constraints for inheritance and dead-man's switch scenarios.

**Type C — MPC-Mediated Recovery:** fROST threshold signatures with proactive share refreshment, enabling distributed key custody with epoch-based state synchronization and cryptographic verification of refresh transcripts.

The specification includes guardian privacy enhancements through salted hashes and pseudonymous identifiers, provider state synchronization protocols, and normative requirements for conformance testing.

---

## Reference Implementation Test Results

| Test Suite | Status | Duration | Details |
|------------|--------|----------|---------|
| Group Parameter Validation | ✅ Pass | 3.88 ms | All group parameter checks passed |
| Random Secret Generation and Recovery | ✅ Pass | 37.08 ms | 10 random secrets tested with 3-of-5 threshold |
| Proactive Share Refreshment | ✅ Pass | 7.69 ms | 5 refresh cycles completed while preserving secret |
| Edge Cases and Configurations | ✅ Pass | 13.59 ms | All threshold configurations validated |
| Performance Benchmarks | ✅ Pass | 123.83 ms | 100 iterations completed |
| Zero-Knowledge Proof Simulation | ✅ Pass | 0.87 ms | Schnorr ZKP verification successful |

### Performance Metrics

| Operation | Average Time |
|-----------|--------------|
| Share Generation | 0.33 ms |
| Share Verification | 0.14 ms |
| Secret Recovery | 0.20 ms |
| Refresh Cycle | 0.15 ms |
| Zero-Knowledge Proof Verification | 0.26 ms |

### Summary

| Metric | Value |
|--------|-------|
| Total Tests | 6 |
| Passed | 6 |
| Failed | 0 |
| Success Rate | 100% |

---

## Features

- **Verifiable Secret Sharing (VSS):** Feldman VSS with Pedersen commitments for share verification
- **Verifiable Delay Functions (VDF):** Time-locked inheritance with Wesolowski proof verification
- **fROST Threshold Signatures:** Flexible Round-Optimized Schnorr Threshold signatures with proactive refresh
- **Guardian Privacy Enhancements:** Salted hashes and pseudonymous identifiers for guardian entries
- **Provider State Synchronization:** Epoch-based catch-up protocol for MPC provider consistency
- **JSON-LD Context:** Machine-readable discovery for DID Document extension methods

---

## Resources

| Resource | Link |
|----------|------|
| **DID-KR Specification** | [Repository Link] |

---

## Status

Editor's Draft — March 2026