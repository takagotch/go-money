### go-money
---
https://github.com/rhymond/go-money

```go
// money_test.go

func TestNew(t *testing.T) {
  m := New(1, "EUR")
  
  if m.amount.val != 1 {
    t.Errorf("Expected %d got %d", 1, m.amount.val)
  }
  
  if m.currency.Code != "EUR" {
    t.Errorf("Expected currency %s got %s", "EUR", m.currency.Code)
  }
  
  m = New(-100, "EUR")
  
  if m.amount.val != 100 {
    t.Errorf("Expected %d got %d", -100, m.amound.val)
  }
}



```

```
```

```
```


