# Autocomplete

Autocomplete provides inline code suggestions as you type. It provides real-time, inline code suggestions as you type, helping you write code faster and with fewer errors. As you begin typing, it predicts and displays context-aware completions directly. This feature enhances productivity by reducing repetitive typing and offering intelligent suggestions based on your current code and project context.

## Steps to Integrate Autocomplete Feature:

**Step 1:** Open your `config.yaml` file by clicking the gear icon at the top of the chat.

<img src="/features/Feature_Images/Autocomplete_step-1.png" alt="clicking gear icon" width="100%" height="auto" />

**Step 2:** Then click the **"open config file"** button to open the `config.yaml` file.

<img src="/features/Feature_Images/Autocomplete_step-2.png" alt="clicking open config file button" width="100%" height="auto" />

**Step 3:** Inside the `config.yaml` file, add `roles` under the model which you are using in the `models` section. Inside `roles`, add `"autocomplete"`.

<img src="/features/Feature_Images/Autocomplete_step-3.png" alt="add roles" width="100%" height="auto" />

**Step 4:** Now if you type in the file, it will suggest code completions.

<img src="/features/Feature_Images/Autocomplete_step-4.png" alt="autocomplete" width="100%" height="auto" />

---

## Accepting a full suggestion:
Press the **"Tab"** key on your keyboard.

## Rejecting a full suggestion:
Press the **"Esc"** key on your keyboard.

## Partially accepting a suggestion:
Press **"Cmd/Ctrl + →"** on your keyboard to accept parts of the suggestion word-by-word.

