# Именование

### Именование функций (принцип P/A/HC/LC)
**1. Префикс**<br/>
Префикс (P, prefix) — расширяет смысл названия
- `is` — является ли переменная копределённым значением (возвращает true/false)
  ```javascript
  function isAdmin(id) {
    if (id.level === 10) return true;
    else return false;
  }
  ```
- `has` — имеет ли переменная определённое значение (возвращает true/false)
  ```javascript
    function hasCats(count) {
      if (count > 0) return true;
      else return false;
    }
  ```
- `should` — (НЕ ПОНЯЛ) условный оператор `true`, связанные с определённым действием
  ```javascript
    function shouldUpdateURL(url, expectedURL) {
      return url !== expecedURL;
    }
  ```

**2. Действие**<br/>
Действие (A, action) — глагольная часть названия функции
- `get` — получить значение
  ```javascript
    function getUserName() {
      return user.name;
    }
  ```
- `set` — задать значение
  ```javascript
    function setAge(newAge) {
      user.age = newAge;
    }
  ```
- `reset` — вернуть переменную в начальное значение
  ```javascript
    function resetName() {
      user.name = `user${id}`;
    }
  ```
- `fetch` — выполнить запрос данных, требующий времени на выолнение (например, асинхронный запрос)
  ```javascript
    function fetchUserInfo(id) {
      fetch(`https://api.github.com/users/${id}`);
    }
  ```
- `delete` — полностью удалить сущность (после удаления она перестаёт существовать)
  ```javascript
    function deleteUser(id) {
      users.id = "";
    }
  ```
- `compose` — создать новые данные из существующих
  ```javascript
    function composeBIO(firstName, lastName) {
      return firstName + lastName;
    }
  ```
- `handle` — обработать что-то (например, событие)
  ```javascript
    function handleClick() {
      console.log("Было нажатие мыши");
    }
  ```

**3. Высокоуровневый контекст**<br/>
Высокоуровневый контекст (HC, high level context) — это сущность, с которой работает функция (например: user, article)

**4. Низкоуровневый контекст**<br/>
Низкоуровневый контекст (LC, low level context) — подсущность, уточняющая, с чем именно идёт работа (например: user**ID**, article**Name**)


### Именование переменных
**1. Принцип S-I-D**<br/>
Имя переменной должно быть:
- Короткое (S, short)
- Интуитивно понятное (I, intuitive)
- Описательное (D, descriptive)

*Примеры:*
- `isAdmin`
- `hasMessages`
- `shouldDisplayPagination`

**2. Избегать сокращений**<br/>
Допускается использование только распространённые сокращения: btn, evt

**3. Избегать дублирования**<br/>
Не использовать имя сущности, если это не снижает информативность (например, метод объекта или класса)
```javascript
  class User {
    // Неправильно
    getUserName() {...}

    // Правильно
    getName() {...}
  }
```

**4. Учитывать количество**<br/>
В зависимости от количества значений, название переменной указывать в единственном/множественном числе

**5. Осмысленные произносимые слова**<br/>
```javascript
  // Плохо
  let yyyymmdstr = new Date();

  // Хорошо
  let currentDate = new Date();
```



## Источники
- [x] [Практическое руководство по именованию классов, функций и переменных](https://habr.com/ru/post/558874)