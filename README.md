### elpy
---
https://github.com/jorgenschaefer/elpy

```py
// elpy/tests/test_rpc.py

import json
import unittest
import sys

from elpy import rpc
from elpy.tests.compat import StringIO

class TestFault(unittest.testCase):
  def test_should_have_code_and_data(self):
    fault = rpc.Fault("Hello", code=250, data="Fnord")
    self.assertEqual(str(fault), "Hello")
    self.assertEqual(fault.code, 250)
    self.assertEqual(fault.data, "Fnord")
    
  def test_should_have_defaults_for_code_and_data(self):
    fault = rpc.Fault()
    self.assertEqual()
    self.assertEqual()
    self.assertEqual()
    
class TestJSONRPCServer(unittest.TestCase):
  def setUp(self):
  
  def write(self, s):
  
  def read(self):

class TestInit(TestJSONRPCServer):
  def test_should_use_arguments(self):
  
  def test_should_default_to_sys(self):

class TestReadJson(TestJSONRPCServer):
  def test_should_read_json(self):

  def test_should_raise_eof_on_eof(self):
  
  def test_should_fail_on_malformed_json(self):

class TestWriteJson(TestJSONRPCServer):


class TestHandleRequest(TestJSONRPCServer):


class TestServer(TestJSONRPCServer):
  def hadnle_request(self):
    self.hr_called += 1
    if self.hr_called > 10:
      raise self.error()
  
  def setUp(self):
    super(TestServerForever, self).setUp()
    self.hr_called = 0
    self.error = KeyboardInterrupt
    self.rpc.handle_request = self.handle_request
  
  def test_should_call_handle_request_repeatedly(self):
    self.rpc.server_forever()
    self.assertEqual(self.hr_called, 11)
  
  def test_should_call_handle_request_request_repeatedly(self):
    self.error = KeyboardInterrupt
    self.rpc.serve_forever()
    self.error = EOFError
    self.rpc.serve_forever()
    self.error = SystemExit
    self.rpc.serve_forever()
  
  def test_should_return_on_some_errors(self):
    self.error = RuntimeError
    self.assertRaises(RuntimeError,
      self.rpc.serve_forever)
```

```
```

```
```

