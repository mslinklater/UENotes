# Automated Testing

## Source Locations

* Source/Runtime/Core/Public/Misc/AutomationTest.h
* Plugins/Tests/...
* Source/Runtime/AutomationMessages/
* Source/Runtime/AutomationWorker/
* Source/Developer/AutomationController
* Source/Developer/AutomationDriver
* Source/Developer/AutomationWindow

## Code Modules

* EditorTests (plugins)
* FbxAutomationTestBuilder (plugins)
* FunctionalTestingEditor (plugins)
* RuntimeTests (plugins)
* ScreenshotTools (plugins)
* AutomationController (developer)
* AutomationDriver (developer)
* AutomationWindow (developer)
* UnrealEd (editor)
* AutomationMessages (runtime)
* AutomationWorker (runtime)


### Unit Tests

Lots of examples here

Source/Runtime/Core/Private/Tests

### 

## Types

### Enums
```
EAutomationTestFlags
EAutomationExpectedErrorFlags
```
### Structs
```
FAutomationExpectedError
FAutomationScreenShotData
```
### Macros

PRIVATE defines are hidden behind the non-PRIVATE ones so that the WITH_AUTOMATION_WORKER define can replace them will empty stubs
```
ADD_LATENT_AUTOMATION_COMMAND
BEGIN_DEFINE_SPEC
BEGIN_DEFINE_SPEC_PRIVATE
DEFINE_ENGINE_LATENT_AUTOMATION_COMMAND
DEFINE_ENGINE_LATENT_AUTOMATION_COMMAND_ONE_PARAMETER
DEFINE_EXPORTED_LATENT_AUTOMATION_COMMAND
DEFINE_EXPORTED_LATENT_AUTOMATION_COMMAND_ONE_PARAMETER
DEFINE_LATENT_AUTOMATION_COMMAND
DEFINE_LATENT_AUTOMATION_COMMAND_ONE_PARAMETER
DEFINE_SPEC
DEFINE_SPEC_PRIVATE
END_NETWORK_AUTOMATION_COMMAND
IMPLEMENT_BDD_AUTOMATION_TEST
IMPLEMENT_BDD_AUTOMATION_TEST_PRIVATE
IMPLEMENT_COMPLEX_AUTOMATION_TEST
IMPLEMENT_COMPLEX_AUTOMATION_TEST_PRIVATE
IMPLEMENT_CUSTOM_COMPLEX_AUTOMATION_TEST
IMPLEMENT_CUSTOM_SIMPLE_AUTOMATION_TEST
IMPLEMENT_NETWORKED_AUTOMATION_TEST
IMPLEMENT_NETWORKED_AUTOMATION_TEST_PRIVATE
IMPLEMENT_SIMPLE_AUTOMATION_TEST
IMPLEMENT_SIMPLE_AUTOMATION_TEST_PRIVATE
START_NETWORK_AUTOMATION_COMMAND
```
### Interfaces
```
IAutomationLatentCommand
IAutomationNetworkCommand
```
### Classes
```
FAutomationTestBase
	FAutomationSpecBase
	FBDDAutomationTestBase
FAutomationTestExecutionInfo
FAutomationTestFramework
FAutomationTestInfo
FDelayedFunctionLatentCommand
FFunctionLatentCommand
FThreadedAutomationLatentCommand : IAutomationLatentCommand
FUntilCommand
```
