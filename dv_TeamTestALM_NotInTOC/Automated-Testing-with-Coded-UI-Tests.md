---
title: "Automated Testing with Coded UI Tests"
ms.custom: na
ms.date: 10/03/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f2c5b045-c851-4657-9f88-ff24bc857293
caps.latest.revision: 10
manager: douge
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# Automated Testing with Coded UI Tests
Automated tests of the user interface (UI) are known as *coded UI tests*. These tests provide functional testing of the UI and validation of UI controls. You can create coded UI tests to determine that the UI is functioning correctly after code changes.  
  
 Coded UI tests are often used in Visual Studio solutions to quickly verify correct code functionality and as a quality gate prior to checking in code changes. Coded UI tests can complement the unit tests in a Visual Studio solution. For more information, see [Use UI Automation To Test Your Code](../VS_IDE/Use-UI-Automation-To-Test-Your-Code.md) and [Unit Test Your Code](../VS_IDE/Unit-Test-Your-Code.md).  
  
 You can also create coded UI tests to automate manual tests that you created in Microsoft Test Manager. These automated manual tests can then be included in your Team Build configurations as part of your integration testing.  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
## Tasks  
  
|Tasks|Associated Topics|  
|-----------|-----------------------|  
|**Creating an Automated UI Test from an Existing Manual Test:** Create an automated UI test from an existing action recording from a manual test case.|-   [Generating a Coded UI Test from an Existing Action Recording](../dv_TeamTestALM/Generating-a-Coded-UI-Test-from-an-Existing-Action-Recording.md)<br />-   [- How to: Create an Action Recording](../Topic/-%20How%20to:%20Create%20an%20Action%20Recording.md)|  
|**Record User Actions to Create an Automated UI Test:** Record the user actions that you want to use to create an automated UI test and generate the code for a coded UI test from this recording. You can then add custom code to your coded UI test using the Code Editor, or by using the Coded UI Test Editor.|-   [How to: Generate a Coded UI Test by Recording the Application Under Development](../VS_not_in_toc/How-to--Generate-a-Coded-UI-Test-by-Recording-the-Application-Under-Development.md)<br />-   [Walkthrough: Creating, Editing and Maintaining a Coded UI Test](../VS_IDE/Walkthrough--Creating--Editing-and-Maintaining-a-Coded-UI-Test.md)<br />-   [Making Coded UI Tests Wait For Specific Events During Playback](../VS_IDE/Making-Coded-UI-Tests-Wait-For-Specific-Events-During-Playback.md)<br />-   [How to: Record Mouse Hovers in Coded UI Tests](../VS_not_in_toc/How-to--Record-Mouse-Hovers-in-Coded-UI-Tests.md)<br />-   [How to: Select a Control Using the Keyboard  in Coded UI Tests](../VS_not_in_toc/How-to--Select-a-Control-Using-the-Keyboard--in-Coded-UI-Tests.md)<br />-   [Using HTML5 Controls in Coded UI Tests](../VS_IDE/Using-HTML5-Controls-in-Coded-UI-Tests.md)<br />-   [How to: Use UI Control Actions and Properties in Your Coded UI Tests](../VS_not_in_toc/How-to--Use-UI-Control-Actions-and-Properties-in-Your-Coded-UI-Tests.md)<br />-   [Editing Coded UI Tests Using the Coded UI Test Editor](../VS_IDE/Editing-Coded-UI-Tests-Using-the-Coded-UI-Test-Editor.md)|  
|**Add UI Controls and Validation to Your Automated UI Test:** Add UI controls to your coded UI test and verify the values and the properties of the controls using the Coded UI Test Builder.<br /><br /> If you are testing a large application, you might have to use multiple UI maps to help create your coded UI tests.|-   [How to: Add UI Controls and Validation Code Using the Coded UI Test Builder](../VS_not_in_toc/How-to--Add-UI-Controls-and-Validation-Code-Using-the-Coded-UI-Test-Builder.md)<br />-   [Using HTML5 Controls in Coded UI Tests](../VS_IDE/Using-HTML5-Controls-in-Coded-UI-Tests.md)<br />-   [Anatomy of a Coded UI Test](../VS_IDE/Anatomy-of-a-Coded-UI-Test.md)<br />-   [Testing a Large Application with Multiple UI Maps](../VS_IDE/Testing-a-Large-Application-with-Multiple-UI-Maps.md)|  
|**Add Parameters from a Data Source to Use with Your Coded UI Test:**  Make your coded UI test into a data-driven test by adding a data source for your test method and using the test context to run the test method for each set of data in your data source.|-   [Creating a Data-Driven Coded UI Test](../VS_IDE/Creating-a-Data-Driven-Coded-UI-Test.md)|  
|**Link Test Cases to User Requirements:** Link your automated UI tests to user requirements. You can then determine how many automated tests you have for your user requirements.|-   [How to: Add Product Backlog Items, User Story, or Requirements Work Items to Your Test Plan](../Topic/How%20to:%20Add%20Product%20Backlog%20Items,%20User%20Story,%20or%20Requirements%20Work%20Items%20to%20Your%20Test%20Plan.md)|  
|**Edit coded UI tests using the Coded UI Test Editor:** The Coded UI Test Editor lets you easily modify your coded UI tests. Using the Coded UI Test Editor, you can locate, view, and edit your test methods, UI actions and their associated controls in the UI control map.|-   [Editing Coded UI Tests Using the Coded UI Test Editor](../VS_IDE/Editing-Coded-UI-Tests-Using-the-Coded-UI-Test-Editor.md)|  
|**Running Automated UI Tests:** Run coded UI tests directly from Visual Studio, from Microsoft Test Manager, from Team Foundation Build. Coded UI tests have to interact with the desktop when you run them, unlike other automated tests.|-   [Running Automated Tests Using Microsoft Visual Studio](../dv_TeamTestALM/Running-Automated-Tests-Using-Microsoft-Visual-Studio.md)<br />-   [Run tests in your build process](../Topic/Run%20tests%20in%20your%20build%20process.md)<br />-   [Running automated tests from the command line](../dv_TeamTestALM/Running-automated-tests-from-the-command-line.md)<br />-   [How to: Set Up Your Test Agent to Run Tests that Interact with the Desktop](../dv_TeamTestALM/How-to--Set-Up-Your-Test-Agent-to-Run-Tests-that-Interact-with-the-Desktop.md)<br />-   [Can I include coded UI tests in load tests?](assetId:///7041cbcf-9ab1-4579-98ff-8f296aeaded4#CreateRunLoadTest_QA_IncludeCUIT)<br />-   [Analyzing Coded UI Tests Using Coded UI Test Logs](../VS_IDE/Analyzing-Coded-UI-Tests-Using-Coded-UI-Test-Logs.md)|  
|**Adding Support for Custom Controls:** The coded UI testing framework does not support every possible UI and might not support the UI you want to test. For example, you cannot immediately create a coded UI test of the UI for Microsoft Excel. However, you can create an extension to the coded UI testing framework that will support a custom control.|-   [Enable Coded UI Testing of Your Controls](../VS_IDE/Enable-Coded-UI-Testing-of-Your-Controls.md)<br />-   [Extending Coded UI Tests and Action Recordings to Support Microsoft Excel](../VS_IDE/Extending-Coded-UI-Tests-and-Action-Recordings-to-Support-Microsoft-Excel.md)|  
|**Best Practices for Coded UI Tests:** Write coded UI tests that reduce the effect of a changing UI on the program under test.|-   [Best Practices for Coded UI Tests](../VS_IDE/Best-Practices-for-Coded-UI-Tests.md)|  
  
## Related Scenarios  
 [Supported Configurations and Platforms for Coded UI Tests and Action Recordings](../VS_IDE/Supported-Configurations-and-Platforms-for-Coded-UI-Tests-and-Action-Recordings.md)  
  
 If you want to verify which configurations are supported for coded UI tests, you can find the current list of operating systems, browsers, and supported technologies.  
  
## External Resources  
  
### Guidance  
 [Testing for Continuous Delivery with Visual Studio 2012 – Chapter 2: Unit Testing: Testing the Inside](http://go.microsoft.com/fwlink/?LinkID=255188)  
  
 [Testing for Continuous Delivery with Visual Studio 2012 – Chapter 5: Automating System Tests](http://go.microsoft.com/fwlink/?LinkID=255196)  
  
### FAQ  
 [Coded UI Tests FAQ - 1](http://go.microsoft.com/fwlink/?LinkID=230576)  
  
 [Coded UI Tests FAQ -2](http://go.microsoft.com/fwlink/?LinkID=230578)  
  
### Forum  
 [Visual Studio UI Automation Testing (includes CodedUI)](http://go.microsoft.com/fwlink/?LinkID=224497)