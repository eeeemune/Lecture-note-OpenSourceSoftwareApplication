# [오픈소스응용프로그래밍] 09.SOLID 원칙

<aside>

# 💖 객체지향설계 원칙

</aside>

## SOLID 원칙

<aside>

**슬라이드 예시처럼 시험 문제도 나올 거라고 말씀하심. 각각의 원칙이 지켜지지 않으면 나타날 수 있는 문제점을 알 수 있고 코드에서 문제점을 찾고 고치는 문제**

</aside>

## ⚡ Single Responsibility Principle

<aside>

**Single Responsibility Principle**

클래스를 변경해야 하는 이유는 단 하나여야 한다.

</aside>

![image.png](image%209.png)

### 예시: 적용 후

```cpp
class User {
  public: 
  void Login() {
    cout << "User logged in" << endl;
  }
  void Logout() {
    cout << "User logged out" << endl;
  }
  void PrintUserInfo(string username) {
    cout << "Username: " << username << endl;
  }
};
```

### 예시: 적용 후

```cpp
class Authentication {
  public:
  void Login() {
    cout << "User logged in" << endl;
  }
  void Logout() {
    cout << "User logged out" << endl;
  }
};

class UserInfo {
  public:
  void PrintUserInfo(string username) {
    cout << "Username: " << username << endl;
  }
};

class User: public Authentication, public UserInfo {};
```

## ⚡ Open Closed Principle

<aside>

**Open Closed Principle**

확장에는 열려 있어야 하고, 수정에는 닫혀 있어야 한다.

</aside>

### 예시: 적용 전

```cpp
class Account {
  public: Account(double balance, int type_of_account): balance_(balance),
  type_of_account_(type_of_account) {}
  void Deposit(double amount) {
    balance_ += amount;
  }
  void Withdraw(double amount) {
    balance_ -= amount;
  }
  double balance() const {
    return balance_;
  }
  double CalculateInterest() const {
    if (type_of_account_ == 1) {
      .....
    } else if (type_of_account_ == 2) {
      .....
    }.....
    // LOGIC based on type of account
  }
  private: double balance_;
  int type_of_account_;
};
```

### 예시: 적용 후

```cpp
class SavingsAccount: public Account {
  public: SavingsAccount(double balance,
    double interate_rate): balance_(balance),
  interest_rate_(interest_rate) {}
  void Deposit(double amount) override {
    balance_ += amount;
  }
  void Withdraw(double amount) override {
    balance_ -= amount;
  }
  double balance() override {
    return balance_;
  }
  double CalculateInterest() override {
    return balance_ * interest_rate_;
  }
  private: double balance_;
  double interest_rate_;
};
```

```cpp
class SavingsAccount: public Account {
  public: SavingsAccount(double balance,
    double interate_rate): balance_(balance),
  interest_rate_(interest_rate) {}
  void Deposit(double amount) override {
    balance_ += amount;
  }
  void Withdraw(double amount) override {
    balance_ -= amount;
  }
  double balance() override {
    return balance_;
  }
  double CalculateInterest() override {
    return balance_ * interest_rate_;
  }
  private: double balance_;
  double interest_rate_;
};
```

```cpp
class FixedDepositAccount: public Account {
  public: FixedDepositAccount(double balance,
    double interate_rate,
    int time): balance_(balance),
  interest_rate_(interest_rate),
  time _(time) {}
  void Deposit(double amount) override {
    balance_ += amount;
  }
  void Withdraw(double amount) override {
    // Logic to withdraw after a certain time
    balance_ -= amount;
  }
  double balance() override {
    return balance_;
  }
  double CalculateInterest() override {
    return balance_ * interest_rate_;
  }
  private: double balance_;
  double interest_rate_;
  int time_;
};
```

## ⚡ Liskov Substitution Principle

<aside>

**외워야 할 부분은 아니라고 하심. 혹시 나중에 피터코드의 규칙이 시험에 나온다면 그 때 따로 말씀하시겠다고 하심.**

</aside>

<aside>

**Liskov Substitution Principle**

상위 클래스의 자리에 하위 클래스를 집어 넣더라도 문제없이 작동해야 한다

</aside>

### 예시: 적용 전

```cpp
class Bird
{
public:
    virtual void Fly() = 0;
};
class Crow : public Bird
{
public:
    void Fly() override
    {
        cout << "Crow is flying" << endl;
    }
};
class Penguin : public Bird
{
public:
    void Fly() override
    {
        throw runtime_error("Penguins can't fly");
    }
};
void makeBirdFly(const Bird &bird)
{
    bird.fly();
}
```

하위 클래스인 펭귄을 bird로 대체하면 오류가 발생함. 이 경우 리스코프 치환 원칙이 지켜지지 않았음.

### 예시: 적용 후

```cpp
class Bird
{
public:
    virtual bool CanFly() = 0;
};
class FlyingBird : public Bird
{
public:
    bool CanFly() override
    {
        return true;
    }
    virtual void Fly() = 0;
};
class Crow : public FlyingBird
{
public:
    void Fly() override
    {
        cout << "Crow is flying" << endl;
    }
};
class Penguin : public Bird
{
public:
    void CanFly() override
    {
        return false;
    }
};
void makeBirdFly(const FlyingBird &bird)
{
    bird.Fly();
}
```

문제 해결: 비행할 수없는 새가 있음을 미리 인지하고 계층구조를 변경해서 `FlyingBird`라는 class를 새로 만든다

## ⚡ Interface Segregation Principle

<aside>

**Interface Sergregation Principle**

클라이언트는 자신이 사용하지 않는 메서드와 의존 관계를 맺어서는 안 된다.

</aside>

클라이언트는 자신이 사용하지 않는 메서드와 의존관계를 맺으면 안 된다. 인터페이스는 가능한 작게 설계해서 **불필요한 코드와의 의존관계를 방지**함

### 예시: 적용 전

```cpp
class Printer
{
public:
    virtual void Print() = 0;
    virtual void Scan() = 0;
    virtual void Fax() = 0;
};

class InkJetPrinter : public Printer
{
public:
    void Print() override
    {
        cout << "InkJet Printer Printing" << endl;
        // Implementation of print for InkJet printer
    }
    void Scan() override
    {
        cout << "InkJet Printer Scanning" << endl;
        // Implementation of scan for InkJet printer
    }
    void Fax() override
    {
        cout << "InkJet Printer Faxing" << endl;
        // Implementation of fax for InkJet printer
    }
};
class LaserPrinter : public Printer
{
public:
    void Print() override
    {
        cout << "Laser Printer Printing" << endl;
        // Implementation of print for laser printer
    }
    void Scan() override
    {
        cout << "Laser Printer Scanning" << endl;
        // Implementation of scan for laser printer
    }
    void Fax() override
    {
        throw runtime_error("Laser Printer Can't Fax");
    }
};
```

위에서, `LaserPrinter`는 fax 기능이 필요하지 않지만 `Printer`를 상속받았기 때문에 가지게 됨

- 이 경우 인터페이스 분리 원칙을 위반함

### 예시: 적용 후

```cpp
class IsPrintable
{
public:
    virtual void Print() = 0;
};
class IsScannable
{
public:
    virtual void Scan() = 0;
};
class IsFaxable
{
public:
    virtual void Fax() = 0;
};
class LaserPrinter : public IsPrintable,
                     public IsScannable
{
public:
    void Print() override
    {
        cout << "Laser Printer Printing" << endl;
        // Implementation of print for laser printer
    }
    void Scan() override
    {
        cout << "Laser Printer Scanning" << endl;
        // Implementation of scan for laser printer
    }
};
class InkJetPrinter : public IsPrintable,
                      public IsScannable,
                      public IsFaxable
{
public:
    void Print() override
    {
        cout << "InkJet Printer Printing" << endl;
        // Implementation of print for InkJet printer
    }
    void Scan() override
    {
        cout << "InkJet Printer Scanning" << endl;
        // Implementation of scan for InkJet printer
    }
    void Fax() override
    {
        cout << "InkJet Printer Faxing" << endl;
        // Implementation of fax for InkJet printer
    }
};
```

scan, print, fax 기능을 각각 분리함

## ⚡ Dependency Inversion Principle

<aside>

**Dependency Inversion Principle**

어떤 클래스를 상속받고 싶을 때는 그 클래스가 아닌 그 클래스의 interface class를 상속받아야 한다.

</aside>

의존 관계 역전 원칙. 클라이언트는 구체 클래스가 아닌 추상 클래스에 의존해야 한다. 고수준 모듈과 저수준 모듈이 있을 때 고수준 모듈이 저수준 모듈에 의존하면 안됨

- 이 때, A가 B에 의존한다는 것은?
    - A를 수정했을 때 B도 수정해야 함

### 예시: 적용 전

```cpp
class FruitBasket
{ // Low-level module
public:
    void AddToBasket(const std::string &fruit, const std::string &color){
        basket.push_back(std::make_tuple(fruit, color));
    }
    std::vector<std::tuple<std::string, std::string>>
    get_basket() { return basket_; }

private:
    std::vector<std::tuple<std::string, std::string>> basket_;
};
class ColorSearcher
{ // High-level module
public:
    void ListColor(FruitBasket fruit_basket, const std::string &color)
    {
        for (auto item : fruit_basket.get_basket())
        {
            if (Std::get<1>(item) == color)
            {
                std::cout << "Found" << std::get<0>(item) << std::endl;
            }
        }
    }
}
```

### 예시: 적용 후

```cpp
class BasketSearcher
{ // abstract module
public:
    virtual std::vector<std::string>
    SearchByColor(const std::string &color) = 0;
};
class FruitBasket : public BasketSearcher
{ // Low-level module
public:
    void AddToBasket(const std::string &fruit,
                     const std::string &color)
    {
        basket_.push_back(std::make_tuple(fruit, color));
    }
    std::vector<std::string>
    SearchByColor(const std::string &color) override
    {
        std::vector<std::string> found;
        for (auto item : basket_)
        {
            if (std::get<1>(item) == color)
            {
                found.push_back(std::get<0>(item));
            }
        }
        return found;
    }

private:
    std::vector<std::tuple<std::string, std::string>> basket_;
};
class ColorSearcher
{ // High-level module
public:
    void ListColor(BasketSearcher &basket,
                   std::string color)
    {
        for (auto item : basket.SearchByColor(color))
        {
            std::cout << "Found " << item << std::endl;
        }
    }
};
```