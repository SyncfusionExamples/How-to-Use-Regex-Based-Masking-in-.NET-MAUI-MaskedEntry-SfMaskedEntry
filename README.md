# How to Use Regex-Based Masking in .NET MAUI SfMaskedEntry

The `MaskType` property provides built-in support for regex-based masking, allowing you to define custom input patterns using regular expressions.

To validate user input with a regular expression, set the `MaskType` property to `RegEx` and specify the desired pattern through the `Mask` property:

* When `MaskType = RegEx`, the control validates user input against the specified regular expression pattern.
* The `Mask` property defines the regex rule that users must follow while entering data.

This approach enables advanced input validation and helps ensure that users enter data in the required format.

### Benefits of Using Regex-Based Masking

* Supports complex and custom validation requirements.
* Restricts input based on regular expression patterns.
* Improves data accuracy and consistency.
* Reduces the need for additional validation logic.
* Provides flexibility for handling various input formats.

## Example Scenario

Here an input field for email validation using a regular expression pattern:

**MainPage.xaml**
```
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:editors="clr-namespace:Syncfusion.Maui.Inputs;assembly=Syncfusion.Maui.Inputs"
             Title="How to Use Regex-Based Masking in .NET MAUI SfMaskedEntry"
             x:Class="MaskedEntrySample.MainPage">
    <VerticalStackLayout>
        <editors:SfMaskedEntry WidthRequest="250"
                       ClearButtonVisibility="WhileEditing"
                       MaskType="RegEx"
                       Mask="[A-Za-z0-9._%-]+@[A-Za-z0-9]+\.[A-Za-z]{2,3}">
        </editors:SfMaskedEntry>
    </VerticalStackLayout>
</ContentPage>
```