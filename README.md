# CRequests

## Structures

```C
struct s_response {
  headers;
  uint32_t  return_code;
  bool      success;
  uint8_t   *text;
};

struct s_session {
  // ...
}
```

## Interface

```C
struct s_response *requests_get(uint8_t const * const uri, headers, params, session);
struct s_response *requests_post(uint8_t const * const uri, headers, data, session);
struct s_response *requests_head(uint8_t const * const uri, headers, ..., session);
struct s_response *requests_put(uint8_t const * const uri, headers, ..., session);
struct s_response *requests_delete(uint8_t const * const uri, headers, ..., session);
```
