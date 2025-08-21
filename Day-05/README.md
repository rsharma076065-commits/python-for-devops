# ✅ 1. Environment Variable Example (Secrets)
# You don’t want to hardcode secrets like API keys or passwords in your script. Use environment variables.

# 🔧 Example: env_example.py
```python
import os

api_key = os.environ.get("API_KEY")

if not api_key:
    print("API_KEY not found in environment!")
else:
    print(f"Deploying with API key: {api_key[:4]}***")

# ▶️ Run it:
export API_KEY=1234abcdsecret
python env_example.py
```

# ✅ 2. Command-Line Argument Example (Choose Environment)
# Useful when running the same script for different environments like dev, test, prod.

# 🔧 Example: args_example.py

```python
import sys

if len(sys.argv) < 2:
    print("Usage: python args_example.py <env>")
    sys.exit(1)

env = sys.argv[1]
print(f"Deploying to: {env}")

# ▶️ Run it:
python args_example.py dev
```
