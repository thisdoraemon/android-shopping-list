# Android Shopping List App

## Overview

This is a simple Android app developed using Kotlin and Jetpack Compose that allows users to manage a shopping list. Users can add, edit, and delete shopping items. The app features a clean and intuitive user interface for a seamless shopping list management experience.

## Components
## 1. ShoppingItem Data Class

```kotlin
data class ShoppingItem(
    val id: Int,
    var name: String,
    var quantity: Int,
    var isEditing: Boolean = false
)
```

- Represents a shopping item with an id, name, quantity, and an optional editing flag.

## 2. ShoppingListApp Composable

```kotlin

@Composable
fun ShoppingListApp() { ... }
```

- Main composable function that builds the entire shopping list UI.
- Allows users to add new items and displays a list of existing items.

## 3. ShoppingItemEditor Composable

```kotlin

@Composable
fun ShoppingItemEditor(item: ShoppingItem, onEditComplete: (String, Int) -> Unit) { ... }
```

- Composable for editing shopping items.
- Provides text fields for editing the item name and quantity.
- Allows users to save changes.

## 4. ShoppingListItem Composable

```kotlin

@Composable
fun ShoppingListItem(
    item: ShoppingItem,
    onEditClick: () -> Unit,
    onDeleteClick: () -> Unit
) { ... }
```

- Composable for displaying a single shopping item.
- Shows the item name, quantity, and provides buttons for editing and deleting.

## Usage

1. Adding a New Item
   - Click the "Add Item" button.
   - Enter the item name and quantity in the dialog.
   - Click "Add" to confirm or "Cancel" to discard changes.
     
2. Editing an Item
   - Click the edit (pencil) icon next to the item.
   - Update the name and quantity in the editor.
   - Click "Save" to confirm changes.

3. Deleting an Item
   - Click the delete (trash can) icon next to the item.

## Code Structure

- The code is organized into composable functions for modularity and readability.
- State variables are used to manage the app's data and UI state.
- Jetpack Compose is leveraged for creating a reactive and declarative UI.

## Dependencies

- Jetpack Compose for building the UI.
- AlertDialog for displaying dialogs.
- Icons from the Material3 library for edit and delete actions.

## Conclusion

This app provides a basic yet functional shopping list management system using modern Android development practices. Feel free to explore and customize the code for further enhancements or integrate additional features.
