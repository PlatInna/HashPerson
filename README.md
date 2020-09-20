# HashPerson
Coursera: C++ Development Fundamentals: Brown Belt: Week 1

We want to learn how to embed the structure ```Person``` into the container ```unordered_set <Person, PersonHasher>```. You need to implement the structures ```PersonHasher```,
```AddressHasher``` and comparison operators:
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

Use the standard hash functions ```std::hash``` and combine the field hashes using a polynomial, as shown in the lecture.

Requirements:
   - hash functions must depend on all fields of structures
   - the hash function should evenly scatter objects of type ```Person```; this feature is checked by the ```TestDistribution``` test in the solution template.
