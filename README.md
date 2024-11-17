# Effortlessly manage PlayerPrefs and EditorPrefs with support for multiple data types!

Advanced Save Manager provides an intuitive solution for saving and retrieving various data types to and from PlayerPrefs or EditorPrefs. Customize your saving experience by adding support for new data types seamlessly.

Features include:

- Save and retrieve data across supported types with ease.
- Switch between PlayerPrefs and EditorPrefs for your storage needs.
- Enable EditorPrefs functionality by simply defining USE_EDITOR_PREFS in Scripting Define Symbols.
- Designed for simplicity and extensibility to meet your custom requirements.

Make your data management smarter with Advanced Save Manager!


**OVERVIEW**

Extra Types:

```
Bool
DateTime
Dictionary
Enum
List
Json
Vector3
Color
long
etc
```

# Example with **Bool** Type

```C#
// Create a BoolPrefs instance
IPrefs<bool> boolPrefs = new BoolPrefs(string key, bool defaultValue);
```

**Methods:**

1. `boolPrefs.GetValue()`

- Retrieves the value associated with the given key from the preferences file.
- If the key does not exist, it returns the defaultValue.

```C#
bool value = boolPrefs.GetValue();
```

2. `boolPrefs.SetValue(bool value)`

- Saves a new value for the preference identified by the key.

```C#
boolPrefs.SetValue(true);
```

3. `boolPrefs.Reset()`

- Removes the current value associated with the key and resets it to the defaultValue.

```C#
boolPrefs.Reset();
```

4. `boolPrefs.DeleteKey()`

- Deletes the key assigned to this preference from PlayerPrefs.
```C#
boolPrefs.DeleteKey();
```

5. `MultipleTypesPlayerPrefs.Save()`

- Writes all modified preferences to disk.
- This ensures any changes made are saved persistently.

```C#
MultipleTypesPlayerPrefs.Save();
```

This example demonstrates how to use BoolPrefs effectively with key operations like retrieving, setting, resetting, and deleting preferences.
