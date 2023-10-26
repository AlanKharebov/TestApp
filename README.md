# TestApp
Testting user control  resfrecing from library

I encoputer this probklem with WinUI 3.
1. Created TestLibrary with user control TestUserControl
2. Created WinUI 3 .NET 6 TestApp
3. Created nuget package for TestLibrary. I am using d:\dev\nuget for local packages
4. Referecnced  TestLibrary in TestApp
5. In ManWindow add user control TestUserControl
6. When I run app I ma geeting errors

![image](https://github.com/AlanKharebov/TestApp/assets/17842209/3b81400a-4a7a-4515-8134-e2907ca5399e)

I think problem is how user control refrnced in WinUI. In WPF it addds assembly name

## Here my response to similar ptroblem
https://github.com/microsoft/WindowsAppSDK/issues/3546

I have the same problem.
In a similar WPF app, the reference to a UserControl looks like this:
xmlns:wpfControlLibrary="clr-namespace:WpfControlLibrary;assembly=WpfControlLibrary"

However, in WinUI, it is done like this:
xmlns:testLibrary="using:TestLibrary".

Note that there is no "assembly=WpfControlLibrary" in the WinUI version.

I wanted to switch to WinUI, but it still looks very immature compared to WPF.

