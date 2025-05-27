# 🌍 Поисковая система в 2ГИС

## 📌 Описание проекта

Проект представляет собой **Веб приложеиние**, вдохновлённый интерфейсом 2ГИС, с реализацией поисковой строки, имитирующей работу городской справочной системы.

Поисковая система позволяет пользователю вводить название компании, адрес или ключевое слово. При совпадении — отображается список результатов.  

Реализация выполнена с помощью **HTML**, **CSS** и **JavaScript**.

---

## 🧩 Функциональность

### ✅ Реализовано:
- Поисковая строка с автоподсказками
- Фильтрация по списку организаций при вводе запроса
- Адаптивный дизайн (мобильная версия)
- CSS-анимация появления результатов
- Поддержка "бургер-меню" в мобильной версии

---

## ⚙️ Технологии

| Инструмент      | Назначение                      |
|----------------|----------------------------------|
| HTML5           | Структура сайта                  |
| CSS3 (Flexbox)  | Адаптивная вёрстка, стилизация   |
| JavaScript      | Поисковая логика, фильтрация     |
| Git + GitHub    | Контроль версий, публикация      |

---

## 🧠 Отличия CSS vs JavaScript (поисковая строка)

| Параметр               | CSS Только              | JavaScript |
|------------------------|--------------------------|------------|
| **Поиск по данным**     | ❌ Невозможно              | ✅ Да       |
| **Фильтрация списка**   | ❌ Только вручную          | ✅ Да       |
| **Реакция на ввод**     | ❌ Ограничено (focus/hover)| ✅ Да (input)|
| **Интерактивность**     | ❌ Нет логики              | ✅ Полный контроль |
| **UI-анимации**         | ✅ Да (плавность, переходы)| ✅ Также можно |

> 📝 Вывод: **CSS** можно использовать только для внешнего вида поля ввода и анимаций. Вся логика поиска (сравнение текста, отображение результатов) — реализуется через **JavaScript**.
## ⚙️Вариативная часть Cтруктура кода :
--
## ⚙️ Html :

>  <!-- <form class="btn" action=""> -->
        <button class="btn" type="submit" > 
            <a href="#poli" class="btn">Полезные Ссылки</a>
        </button>
    </div>
    <form>
   <!-- <input type="text" placeholder="Искать здесь..."> -->
   <input type="text" id="searchInput" placeholder="Поиск по сайту..." />
   <div id="content">

</form>
---
## ⚙️ CSS :
form {
  position: relative;
  width: 300px;
  margin: 0 auto;
}
#searchInput {
  width: 300px;
  padding: 10px;
  margin: 5 px;
  font-size: 16px;
}

input {
  width: 100%;
  height: 42px;
  border-radius: 5px;
  outline: none;
  border: 2px solid #202b20;
  border-radius: 8px;
  background: #435843;
  color: #9E9C9C;
}

input:hover{
 border: 2px solid #3cca3c;
}
#map{
  margin-left:10rem ;
}
.button1 {
  position: absolute; 
  top: 0;
  right: 0px;
  width: 42px;
  height: 42px;
  border: none;
  background: #7BA7AB;
  border-radius: 0 5px 5px 0;
  cursor: pointer;
}
---
## ⚙️ JavaScript :
<script>
  const input = document.getElementById('searchInput');
  input.addEventListener('input', function () {
    const query = input.value.toLowerCase();
    document.querySelectorAll('.section').forEach(section => {
      const text = section.textContent.toLowerCase();
      section.style.display = text.includes(query) ? 'block' : 'none';
    });
  });
</script>

---
## 💻 Склонируйте проект:
   ```bash
   git clone [Поисковая система](https://bekzodrakhmatullaev.github.io/my_site_1)
