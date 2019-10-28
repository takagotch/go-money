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

// formatter_test.go

func TestFormatter_ToMajorUnits(t *testing.T) {
  
  for _, tc := range tcs {
    formatter := NewFormatter(tc.fraction, tc.decimal, tc.thousand, tc.grapheme, tc.template)
    r := formatter.ToMajorUnits(tc.amount)
    
    if r != tc.expected {
      t.Errorf("Expected %d formatted to major units to be %f got %f", tc.amount, tc.expected, r)
    }
  }
}

```

```
```

```
```


