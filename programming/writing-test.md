# Writing Test



### **Frameworks**

* Unit-Test \(phpunit, Atoum\)
* Behaviour Test \(Behat, Peridot, PHPSpec, Kahlan\)
* functional Test \(codeception, storyplayer\)
* Acceptance Tests\(codeception\)

### **Type of testing**: 

* **Black Box**: Black Box Testing is a software testing method in which testers evaluate the functionality of the software under test without looking at the internal code structure.
* **White Box**: White Box Testing is defined as the testing of a software solution's internal structure, design, and coding.

### **Test Double**

Sometimes it is just plain hard to test the[ system under test \(SUT\)](http://xunitpatterns.com/SUT.html) because it depends on other components that cannot be used in the test environment. This could be     because they aren't available, they will not return the results needed for the test or because executing them would have undesirable side effects. When we are writing a test in which we cannot \(or chose not to\) use a real depended-on component \(DOC\), we can replace it with a Test Double. The Test Double doesn't have to behave exactly like the real DOC; it merely has to provide the same API as the real one so that the SUT thinks it is the real one!  
 

#### **Mock objects**

 **mock objects** are simulated objects that mimic the behavior of real objects in controlled ways. A programmer typically creates a mock object to test the behavior of some other object.

* **Dummy**
* **Stubs**
* **Spy**
* **Fake**

#### Dummy object

Use mostly as a parameter and all the methods return null

  
**Example**:  


```php
function getReadyToGo(Engine $engine, Lights $lights) {
     $engine->start();
     $electronics->turnOn($lights);
     return true;
}
```

#### **Stub object**

When an object needs another object for some information we use  
Stub object. Which means we need a fake object to meat the SUT requirements.

**Example**:

```php
function goForward(Electronics $electronics, StatusPanel) {           
    if($statusPanel->engineIsRunning() &&  $statusPanel->thereIsEnoughFuel()) { 
        $electronics->accelerate (); 
    } 
}
```

**Test Case**:

```php
$carController = new CarController();
$electronics = new Electronics();
$stubStatusPanel = $this->getMock('StatusPanel');
$stubStatusPanel->expects($this->any())->method('thereIsEnoughFuel')->will($this->returnValue(TRUE));
$stubStatusPanel->expects($this->any())->method('engineIsRunning')->will($this->returnValue(TRUE));
$carController->goForward($electronics, $stubStatusPanel);
```

####  Spy Object: TODO 







### References

{% embed url="https://stackoverflow.com/questions/3622455/what-is-the-purpose-of-mock-objects" %}

{% embed url="https://martinfowler.com/articles/mocksArentStubs.html\#TheDifferenceBetweenMocksAndStubs" %}



