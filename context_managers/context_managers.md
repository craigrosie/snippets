# Context Managers

## Simple timing context manager

### Implementation

```python
import time
import contextlib

@contextlib.contextmanager
def timer(name):
    start = time.time()
    try:
        yield
    finally:
        end = time.time()
        print('{} took {}'.format(name, end - start))
```

### Usage

```python
with timer('really slow function'):
    function_you_want_to_time()
```
