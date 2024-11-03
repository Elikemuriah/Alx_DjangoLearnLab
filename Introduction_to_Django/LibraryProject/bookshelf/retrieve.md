## 2. Retrieve Operation
Retrieve and display all attributes of the book created.

### Command
```python
book = Book.objects.get(title="1984")
book.title, book.author, book.publication_year
```

### Expected Output
```python
('1984', 'George Orwell', 1949)
```
This output confirms the retrieval of the book's details.

---
