
# CRUD Operations Documentation for Book Model

## 1. Create Operation
Create a `Book` instance with the title "1984", author "George Orwell", and publication year 1949.

### Command
```python
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
```

### Expected Output
```python
<Book: 1984>
```
This confirms that the book instance has been successfully created.

---

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

## 3. Update Operation
Update the title of “1984” to “Nineteen Eighty-Four”.

### Command
```python
book.title = "Nineteen Eighty-Four"
book.save()
book.title
```

### Expected Output
```python
'Nineteen Eighty-Four'
```
This confirms that the title has been successfully updated.

---

## 4. Delete Operation
Delete the book instance and confirm the deletion by retrieving all books again.

### Command
```python
book.delete()
Book.objects.all()
```

### Expected Output
```python
<QuerySet []>
```
This output confirms that the book has been deleted.
