def input_name():
  name = input("Введите имя: ")
  return name

def input_lastname():
  lastname = input("Введите фамилию: ")
  return lastname

def input_patronymic():
  patronymic = input("Введите отчество: ")
  return patronymic

def input_number():
  number = input("Введите номер телефона: ")
  return number

def input_address():
  address = input("Введите город: ")
  return address

def creat_contact():
  name = input_name()
  lastname = input_lastname()
  patronymic = input_patronymic()
  number = input_number()
  address = input_address()
  return f"{lastname} {name} {patronymic}\n{number} {address}\n\n"
  
def add_contact():
  contact = creat_contact()
  with open("phonebook.txt", "a") as file_w:
    file_w.write(contact)

def find_contact():
  search = input("Введите данные для поиска: ")
  with open("phonebook.txt", "r") as file_s:
    contact_str = file_s.read()
  contacts = contact_str.split("\n\n")
  for i in contacts:
    if search in i:
      print(i)
      return
  print("Контакт не найден!")
     
    
def show_contacts():
  with open("phonebook.txt", "r") as f:
    contacts_str = f.read()
  list_contacts = contacts_str.rstrip().split("\n\n")
  for i, contact in enumerate(list_contacts, 1):
    print(i, contact+"\n")
    
def copy_contact():
  data = input("Введите номер контакта: ")
  with open("phonebook.txt", "r") as first_f, open("copyfile.txt", "w") as second_f:
    contacts_str = first_f.read()
    list_contacts = contacts_str.rstrip().split("\n\n")
    i = int(data) - 1
    second_f.write(list_contacts[i])
    
def ui():
  with open("phonebook.txt", "a"):
    pass
  print(
    "\nВозможные варианты действий:\n"
    "1. Добавить контакт\n"
    "2. Копировать контакт\n"
    "3. Показать все контакты\n"
    "4. Найти контакт\n"
    "5. Выход\n"
  )
  choise = input("Выберите действие: ")
  match choise:
    case "1":
      add_contact()
    case "2":
      copy_contact()
    case "3":
      show_contacts()
    case "4":
      find_contact()
    case "5":
      print("Всего доброго!")
    case _:
      print("Неверный ввод")
  ui()
ui()
