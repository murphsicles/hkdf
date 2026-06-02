# ⚡ @crypto/hkdf — HMAC-based Key Derivation for Zeta

**Port of the Rust `hkdf` crate (v0.12.x). HMAC-SHA256 extract-and-expand
per RFC 5869. Depends on @crypto/sha2 for the underlying HMAC.**

## 📦 Package

```
zorbs add @crypto/hkdf
```

## 🔧 API

```zeta
let okm = hkdf::derive(salt, ikm, info, 32);
// 32 bytes of derived key material

// Or step by step:
let prk = hkdf::extract(salt, ikm);
let okm = hkdf::expand(&prk, info, 64);
```

## 📄 License

MIT OR Apache-2.0
