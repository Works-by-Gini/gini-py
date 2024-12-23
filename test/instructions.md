# From the root directory of the project
pip install -e .

Then you can install the package with test dependencies using:
pip install -e ".[test]"
# or for development dependencies
pip install -e ".[dev]"


Set your API key as an environment variable (recommended for security):
export GINI_API_KEY='your_actual_api_key'

Run the test:
python -m test.test_client

Or run specific test methods:
# In your Python console or script
from test.test_client import TestGiniClient

# Create test instance
test = TestGiniClient()
test.setUp()

# Run specific test
try:
    # Basic execution
    test.test_basic_execution()
    
    # Execution with attachment
    test.test_execution_with_attachment()
finally:
    test.tearDown()