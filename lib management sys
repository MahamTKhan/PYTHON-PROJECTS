#available_books = ["A", "B", "C", "D", "E"]
class Maham_library:

    def __init__(self,lst_bk,lib_n):
        self.lst_of_books=lst_bk
        self.name_of_lib=lib_n
    
    #@classmethod
    def display(self):
        
        # lst=[obj for obj in available_books]

        lst=[obj for obj in self.lst_of_books]
        print("AVAILABLE BOOKS:")
        print(lst)

    def add(self,name_of_bk):
        if (name_of_bk) not in self.lst_of_books:
            self.lst_of_books.append(name_of_bk)
            print("Thankyou for adding a book")
        else:
            print("The book is already in the library")


    def lend(self,user,bk_name):
           num=int(input("enter num of books to be borrowed"))
           dict = {f"{bk_name}": f"{user}" for i in range(num)}
           for item in self.lst_of_books:
               if (item==bk_name):
                   dict[bk_name]=user
                   self.lst_of_books.remove(bk_name)
                   print(f"The {bk_name} has been lended to {user}")

               #else:
                  #print("Sorry,the book is not available")

    def return_book(self,user,bk_name):
            if (dict['key']==user):
                print("No such book was lended")

            else:
                self.lst_of_books.append(bk_name)
                print("The book has been returned")



user1=Maham_library(["A", "B", "C", "D", "E"],"maham")

user1.display()

print("ADD METHOD:")
user1.add("l")

print("LEND METHOD:")
user1.lend("maham","E")

print("RETURN METHOD:")
user1.return_book("maham","E")
