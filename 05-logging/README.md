# 📝 Logging in Python

Python's `logging` module is used to record events, errors, and information while a program runs.

## 📦 Basic Example

```python
import logging

logging.basicConfig(filename="app.log",level=logging.INFO)    #output will get saved in the file and level will start from info to critical

logging.debug("Debug message")    #level 1
logging.info("Program started")    #level 2
logging.warning("Something may be wrong")    #level 3
logging.error("An error occurred")    #level 4
logging.critical("Critical error")    #level 5
