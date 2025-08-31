# Command 
book = Book.objects.get(title="1984")
book.delete()

# Expected Outcome
<QuerySet []>