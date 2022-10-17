# Visual Studio Code Cleanup

- Enabling:
  - &gt;= Visual Studio 2022 17.1
    - Options > Text Editor > Code Cleanup > Run Code Cleanup profile on Save = On
  - &lt; Visual Studio 2022 17.1
    - https://marketplace.visualstudio.com/items?itemName=MadsKristensen.CodeCleanupOnSave
- .editorconfig
  - https://aka.ms/editorconfigdocs
- Not perfect
  ```c#
      public static void DoSomething(
  object obj) // does not get indented
  ```
  ```c#
          .Select(x => // following lines do not get indented
      new KeyValuePair<string, string>(
  "name",
    "value"
      ))
  ```
