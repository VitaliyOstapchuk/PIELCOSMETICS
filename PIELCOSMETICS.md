# PIELCOSMETICS
AUTOTESTS
package com.pielcosmetics;

import org.junit.After;
import org.junit.Before;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebDriverSettings {
    public ChromeDriver driver;    // оголошуємо метод driver для всіх тестів
    @Before
    // цей метод для того щоб якщо багато тестів кожен раз не встановлювати різні Property.
    // виконується кожен раз до початку тесту
    public void setUP () {
        System.setProperty("webdriver.chrome.driver", "//home/pc/Downloads/TelegramDesktop/chromedriver/chromedriver"); //прописуємо шлях до chromedriver
        driver = new ChromeDriver();            // підключаємо браузер
        System.out.println("test start");
    }
    @After                                //для виконання дій після запуску
    // виконується кожен раз до початку тесту
    public void close() {
        System.out.println("test close");
        driver.quit();                                   //щоб закрити браузер
    }

}
