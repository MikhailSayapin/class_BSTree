# class_BSTree
======================================================
Здесь реализуется класс Tree со следующим интерфейсом:
```
namespace ${Type}Tree 
{
  enum class traversal_order {pre, in, post};
  class Tree {
  public:
    Tree();
    Tree(std::initializer_list<int> list);
    Tree(const Tree& tree);
    void swap(Tree& tree);
    bool insert(int value);
    bool exists(int value);
    bool remove(int value);
    bool save(const string& path);
    bool load(const string& path);
    void print(traversal_order order);
    auto friend operator<<(ostream& stream, const Tree&) -> ostream& stream;
    auto operator=(const Tree&) -> Tree&;
    ~Tree();
  private:
    Node* root;
  };
}
```
Все операции происходят в пространстве имён BSTree.
