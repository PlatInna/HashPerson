# HashPerson
Coursera: C++ Development Fundamentals: Brown Belt: Week 1

We want to learn how to embed the structure ```c++ Person ``` into the container unordered_set <Person, PersonHasher> Для этого вам нужно реализовать структуры PersonHasher, 
AddressHasher, и операторы сравнения:

```c++
struct Address {
  string city, street;
  int building;

  bool operator==(const Address& other) const {
    // реализуйте оператор
  }
};

struct Person {
  string name;
  int height;
  double weight;
  Address address;

  bool operator==(const Person& other) const {
    // реализуйте оператор
  }
};

struct AddressHasher {
  // реализуйте структуру
};

struct PersonHasher {
  // реализуйте структуру
};
```

Для этого используйте стандартные хеш-функции std::hash и комбинируйте хеши полей с помощью полинома, как показано в лекции.
Требования:
  - хеш-функции должны зависеть от всех полей структур
  - хеш-функция должна равномерно рассеивать объекты типа Person; это её свойство проверяется тестом TestDistribution в заготовке решения.
