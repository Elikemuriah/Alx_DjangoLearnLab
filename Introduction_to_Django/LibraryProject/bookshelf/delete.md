## 4. Delete Operation
Delete the book instance and confirm the deletion by retrieving all books again.

### Command
```python
from bookshelf.models import Book
book = Book.objects.first()
book.delete()
Book.objects.all()
```

### Expected Output
```python
<QuerySet []>
```
This output confirms that the book has been deleted.
