# bookclass Book:
    def __init__(self, title, author, year):
        self.title = title
        self.author = author
        self.year = year
        self.is_read = False

    def read(self):
        """Mark the book as read."""
        self.is_read = True
        print(f"You have read '{self.title}'.")

    def unread(self):
        """Mark the book as unread."""
        self.is_read = False
        print(f"You have not read '{self.title}'.")

    def display_info(self):
        """Display the book information."""
        read_status = "read" if self.is_read else "not read yet"
        print(f"'{self.title}' by {self.author} ({self.year}) - {read_status}")


# Example usage
my_book = Book("To Kill a Mockingbird", "Harper Lee", 1960)
my_book.display_info()  # Show book info
my_book.read()          # Mark the book as read
my_book.display_info()  # Show updated info
my_book.unread()        # Mark the book as unread
my_book.display_info()  # Show updated info
