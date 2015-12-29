﻿A class used for mocking other classes in Qt

#Usage:
In your mock class just inherit this class
```
class MyMockClass : public MockedInterface, public QtMock
{
    ...
};
```

And after that add few calls in your MyMockClass:

```
void MyMockClass::call1()
{
    CALL;
}

void MyMockClass::call2(int arg);
{
    CALL; ARG(MOCK_FNAME, arg);
}
```