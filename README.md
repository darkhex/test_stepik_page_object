#h1 Test case 
 # run specific tests
test_guest_cant_see_success_message_after_adding_product_to_basket: 
Открываем страницу товара 
Добавляем товар в корзину 
Проверяем, что нет сообщения об успехе с помощью is_not_element_present
 

test_guest_cant_see_success_message: 
Открываем страницу товара 
Проверяем, что нет сообщения об успехе с помощью is_not_element_present
 

test_message_disappeared_after_adding_product_to_basket: 
Открываем страницу товара
Добавляем товар в корзину
Проверяем, что нет сообщения об успехе с помощью is_disappeared
---
# all tests for test_product_page 

for 2 
in test_main_page.py
add 
@pytest.mark.login_guest
in mark addadd screenshots
@pytest.mark.for_temp_test

---
Additional:
- add screenshots
---

@pytest.mark.login
class TestLoginFromProductPage():
    @pytest.fixture(scope="function", autouse=True)
    def setup(self):
        self.product = ProductFactory(title = "Best book created by robot")
        # создаем по апи
        self.link = self.product.link
        yield
        # после этого ключевого слова начинается teardown
        # выполнится после каждого теста в классе
        # удаляем те данные, которые мы создали 
        self.product.delete()
        

    def test_guest_can_go_to_login_page_from_product_page(self, browser):
        page = ProductPage(browser, self.link)
        # дальше обычная реализация теста

    def test_guest_should_see_login_link(self, browser):
        page = ProductPage(browser, self.link)
        # дальше обычная реализация теста