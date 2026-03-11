---
title: Ensuring Consistent AI Responses with Context‑Aware Prompt Optimization in Code Studio
description: Learn how to write context-aware prompts that produce consistent, reliable AI responses in Syncfusion Code Studio. Master prompt engineering techniques for bug fixing and code generation.
platform: syncfusion-code-studio
keywords: context-aware-prompting, bug-fixing, prompt-optimization,code-studio-prompts
---

# Ensuring Consistent AI Responses with Context‑Aware Prompt Optimization in Code Studio

## Overview

Have you ever asked an AI to "fix this code" and gotten a completely different answer each time? That's frustrating, right?

When you tell the AI simply "fix this function," it's like asking someone to "make dinner" without telling them what you like, what ingredients you have, or if anyone has allergies. The results will be unpredictable!

**The Problem:**
- First time: AI completely rewrites your function
- Second time: AI changes your formula
- Third time: AI adds complex error handling you don't need
- Every time: Something different!

**The Solution: Context-Aware Prompting**

This means giving the AI clear instructions about:
- What the code currently does
- What's broken
- What you want fixed
- What you DON'T want changed

In this tutorial, You'll see how vague prompts cause problems, and how adding context makes the AI give you consistent, reliable answers every time.

## Prerequisites

Before beginning, ensure:

- Syncfusion Code Studio is installed and properly configured on your system. If you have not yet downloaded Code Studio, refer to [Install and Configure](../getting-started/install-and-configuration) for step-by-step instructions.
- You have a workspace or project folder opened in Code Studio where you can create files.
- Agent mode is enabled in chat window. Learn more about [Agent mode](../features/agent.md).

## What You Will Learn

By the end of this tutorial, you'll be able to:

- Understand why the AI gives different answers each time (and how to fix it)  
- Write clear prompts that get consistent results  
- Tell the AI exactly what to fix and what NOT to touch  
- Test if your prompt works reliably  
- Use these techniques in your daily coding work

## The Bug: A Price Calculation Function

Consider this common scenario in e-commerce applications. You have a function that calculates the final price after applying a discount:

**JavaScript Code:**

```javascript
function calculateFinalPrice(price, discount) {
  return price - discount / 100 * price;
}
```

### What's Wrong?

This function has several critical bugs:

1. **String inputs**: `price` may come as a string (e.g., `"100"`) causing incorrect calculations
2. **Missing discount**: `discount` may be `undefined`, resulting in `NaN`
3. **Formula ambiguity**: Operator precedence might not work as intended
4. **No validation**: Negative numbers aren't handled properly

### Real-World Impact

Imagine these bugs in a real online store:

- Customer adds $100 item, 20% discount → Sees `NaN` in cart (customer leaves!)
- Product price comes from database as text → Cart breaks
- Discount code missing → Checkout fails
- Someone tries negative price hack → Shows `-$45` (you lose money!)

**These are the kind of bugs you'll learn to fix with AI assistance.**

### Why Vague Prompts Don't Work (An Example)

Before we dive into the solution, let's see why simply asking "fix this function" leads to inconsistent results.

**Example of a Vague Prompt:**
```
Fix this function
```

<img src="./tutorials-images/Drag-Function.png" alt="Drag-Function" />

**What Happens - Attempt 1:**
<img src="./tutorials-images/Attempt1.png" alt="Attempt-1" />

**What Happens - Attempt 2 (Same prompt!):**
<img src="./tutorials-images/Attempt2.png" alt="Attempt-2" />

**The Problem:**  
The AI gave two different answers! Why? Because it didn't know:
- **What** you mean by "fix" (fix what exactly?)
- **Which** bugs to focus on
- **How much** to change (small fix or complete rewrite?)
- **What** to keep the same

This is why **vague prompts = inconsistent results!**

Now let's learn the right way to get consistent, reliable fixes.

## Steps

### Step 1 — Create the Buggy Code

Let's start by creating the broken function so you can see the problem yourself.

1. **Create a new file in Code Studio:**
   - **Option 1 - Using Menu:** Click `File` in the top menu bar, then select `New File` from the dropdown menu
   - **Option 2 - Using Keyboard Shortcut:** Press `Ctrl+Alt+Windows+N` (Windows/Linux) or `Cmd+N` (Mac) to instantly create a new file
   - After the new file opens, press `Ctrl+S` (Windows/Linux) or `Cmd+S` (Mac) to save it
   - In the save dialog, name the file `priceCalculator.js` and choose your desired location in your workspace
   - Click `Save` to confirm

2. **Copy and paste this Below buggy code:**
   - Select all the code below by clicking at the start and dragging to the end
   - Copy it using `Ctrl+C` (Windows/Linux) or `Cmd+C` (Mac)
   - Click inside your `priceCalculator.js` file in the editor
   - Paste the code using `Ctrl+V` (Windows/Linux) or `Cmd+V` (Mac)
   - Save the file using `Ctrl+S` (Windows/Linux) or `Cmd+S` (Mac)

```javascript
function calculateFinalPrice(price, discount) {
  return price - discount / 100 * price;
}

// Test cases
console.log(calculateFinalPrice(100, 20));        // Should be 80
console.log(calculateFinalPrice("100", 20));      // Bug: NaN or wrong
console.log(calculateFinalPrice(100, undefined)); // Bug: NaN
console.log(calculateFinalPrice(-50, 10));        // Bug: Negative price
```

3. **Run the code:**
   - **Option 1 - Using Keyboard Shortcut:** Press `Ctrl+` ` (Ctrl + backtick) on Windows/Linux or `Cmd+` ` on Mac to open the integrated terminal
   - **Option 2 - Using Menu:** Go to `Terminal` → `New Terminal` in the top menu
   - Once the terminal opens at the bottom of Code Studio, ensure you're in the correct directory where you saved `priceCalculator.js`
   - Type the following command and press `Enter` to execute the script in the terminal:

```bash
node priceCalculator.js
```

   - **Note:** Ensure that Node.js is installed on your system. If you encounter a "command not found" error, please install Node.js from [nodejs.org](https://nodejs.org/) to run the script successfully.

**What You'll See:**  
The output will show wrong numbers or `NaN` (Not a Number). This proves the function is broken!

### Step 2 — Use Context-Aware Prompting to Fix the Bugs

Now let's use a properly structured, context-aware prompt to get consistent, reliable results.

1. Open the Code Studio chat window by pressing `Ctrl+Alt+B` (Windows) or `Cmd+Alt+B` (Mac), or click the Code Studio icon to the left of the centered search box.

2. **Highlight the buggy function** - Select the entire `calculateFinalPrice` function in your `priceCalculator.js` file

3. **Use the context-aware prompt below** - Copy this entire prompt and paste it into the chat window:

```
Fix the calculateFinalPrice function with these requirements:

CURRENT CODE:
function calculateFinalPrice(price, discount) {
  return price - discount / 100 * price;
}

BUGS TO FIX:
1. Handle when price is passed as a string (e.g., "100")
2. Handle when discount is undefined or missing
3. Prevent negative final prices
4. Ensure the function returns a clean number, not NaN

CONSTRAINTS:
- Keep the existing formula structure (price - discount percentage * price)
- Use minimal code changes
- Don't add external dependencies
- Set default discount to 0 if missing

EXPECTED BEHAVIOR:
- calculateFinalPrice(100, 20) → 80
- calculateFinalPrice("100", 20) → 80
- calculateFinalPrice(100, undefined) → 100
- calculateFinalPrice(-50, 10) → 0 (no negative prices)
```

4. **Send the prompt in the chat Window like below Image by Select the entire `calculateFinalPrice` function in your `priceCalculator.js` file**

  <img src="./tutorials-images/context-Aware.png" alt="Context-Aware" /> 

**The Result:**  
<img src="./tutorials-images/Output-context.png" alt="Output" /> 

The AI provides a focused fix that addresses ALL the bugs without unnecessary changes. Unlike vague prompts, this detailed context ensures you get consistent, reliable results every time.

### Step 3 — Apply and Test the Fix

Now let's verify the fixed function actually solves all our problems.

1. **Replace your old function** with the fixed version in `priceCalculator.js`

2. **Update your test cases:**

```javascript
function calculateFinalPrice(price, discount) {
  const p = Number(price) || 0;
  const d = (discount == null ? 0 : Number(discount) || 0);
  const result = p - (d / 100) * p;
  return result < 0 ? 0 : result;
}
 
// Test cases - Let's check if everything works now!
console.log(calculateFinalPrice(100, 20));        // ✅ Should show: 80
console.log(calculateFinalPrice("100", 20));      // ✅ Should show: 80 (handles strings!)
console.log(calculateFinalPrice(100, undefined)); // ✅ Should show: 100 (handles missing discount!)
console.log(calculateFinalPrice(-50, 10));        // ✅ Should show: 0 (no negative prices!)
```
**Success! 🎉**  
All test cases now pass. No more `NaN`, no more crashes, no more negative prices!

## Verification

After applying the AI's suggestions, verify the results to understand the effectiveness of context-aware prompting.

### Test 1: Run the Code

Open the integrated terminal by pressing `Ctrl+` ` (Ctrl + backtick) on Windows/Linux or `Cmd+` ` on Mac, or go to `Terminal` → `New Terminal` in the top menu. Then run the updated file to see if all bugs are fixed:

```bash
node priceCalculator.js
```

**Check the output:** You should see correct Output with no `NaN` errors. If you see any `NaN` or error messages, something went wrong—go back and check your code.

### Test 2: Try Additional Test Cases

Add more test cases to evaluate edge cases:

```javascript
// Additional test cases
console.log(calculateFinalPrice(50, 10));     // Expected: 45
console.log(calculateFinalPrice("75", "25")); // Expected: 56.25
console.log(calculateFinalPrice(1000));       // Expected: 1000 (no discount)
```

**Compare results:** Check if the function handles these cases as expected.

### Test 3: Check Prompt Consistency

Run the same prompt from Step 3 again and compare:
- Are the solutions similar?
- Do both fix the same bugs?
- Is the code approach consistent?

## What's Next?

- **[Generate Your First Code Using Agent](./generate-your-first-code-using-agent.md)** - Let AI write new code for you
- **[Compare AI Models](./compare-ai-models.md)** - Choose the best AI for your task
- **[Using OpenSpec Inside Syncfusion Code](./using-openspec-inside-syncfusion-code.md)** - Work with API specifications


**You're ready!** Start using context-aware prompting in your projects today.
