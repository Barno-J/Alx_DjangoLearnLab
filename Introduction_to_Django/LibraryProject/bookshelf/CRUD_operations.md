# Create Command
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
book

# Expected outcome
<Book: 1984 by George Orwell (1949)>


# retrieve Command 
book = Book.objects.get(title="1984")

# Expected Output
<QuerySet [<Book: 1984 by George Orwell (1949)>]>


#  Update Command
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()
book

# Expected Outcome
<Book: Nineteen Eighty-Four by George Orwell (1949)>

# Delete Command 
book = Book.objects.get(title="1984")
book.delete()

# Expected Outcome
<QuerySet []>