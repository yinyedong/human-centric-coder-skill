# human-centric-coder

## Description
This Skill enhances AI-generated code readability by embedding human-centric features such as intuitive naming, narrative comments, logical structuring, and defensive programming. It bridges the gap between sterile AI code and the natural, empathetic style preferred by human developers.

## Instructions

- **Naming Philosophy**  
  - Use variable and function names that convey *intent* rather than just data type or structure.  
  - Prefer descriptive names that tell a story or explain *why* the variable exists.  
  - Avoid abbreviations or overly terse names that obscure meaning.

- **Commenting Art**  
  - Write comments primarily to explain *why* something is done, not *how* (the code itself should show how).  
  - Add narrative comments before complex blocks or business logic to provide context.  
  - Avoid redundant comments that repeat what the code clearly states.  
  - Use comments to mark *intentional* design decisions or trade-offs.

- **Structural Layout**  
  - Physically separate code into blocks that correspond to logical thinking steps or business operations.  
  - Use blank lines and indentation to visually group related code.  
  - Place high-level overview comments at the start of functions or modules to guide readers through the flow.

- **Defensive Programming and Fault Tolerance**  
  - Explicitly check for edge cases and invalid inputs early to reduce mental overhead for readers.  
  - Use guard clauses to handle error conditions upfront and keep the main logic clean.  
  - Document assumptions and preconditions clearly in comments.

- **Human vs AI Coding Style**  
  - Humans write code with empathy for future readers, embedding *stories* and *intent*; AI often generates syntactically correct but context-poor code.  
  - To make AI code more human-like, enforce naming conventions that reflect domain language, add narrative comments, and structure code to mimic human thought processes.  
  - Encourage AI to leave intentional "logical whitespace" and avoid overly compact or overly verbose code.

## Examples

### AI Style (Hard to Understand)
```python
def f(l):
    r = []
    for i in l:
        if i > 0:
            r.append(i*2)
    return r
```

### Human Style (Easy to Understand)
```python
def double_positive_numbers(numbers):
    """
    Return a new list containing double the value of each positive number
    from the input list. Negative numbers and zero are ignored as they
    do not meet the business criteria.
    """
    doubled_positives = []

    # Iterate through all numbers to filter and double positives
    for number in numbers:
        if number > 0:
            doubled_positives.append(number * 2)

    return doubled_positives
```
