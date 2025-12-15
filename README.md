# Сравнение систем Text-to-Speech (TTS): API vs. Tortoise TTS

## Цель проекта

Целью данного проекта является сравнение качества синтеза речи, полученной от различных систем Text-to-Speech (TTS):
1.  **Коммерческий/Бесплатный API** (например, Zvukogram, Google TTS).
2.  **Нейросетевая модель с открытым исходным кодом** (Tortoise TTS).
3.  *Дополнительно:* Современная модель из Hugging Face (VITS).

Работа проводилась в среде **Google Colab** из-за высокой требовательности модели Tortoise TTS к вычислительным ресурсам (GPU).

---

##  Задание

В рамках выполнения задания был взят небольшой текстовый отрывок:
>The desert planet holds ancient secrets, buried beneath endless dunes and silence.
Water is life—and on Arrakis, every drop is measured, honored, and fiercely protected.
A leader must see not only the present danger, but the shadow of consequence stretching far into the future.
The spice flows through all things: it shapes fate, awakens prescience, and binds the universe together.
To know the desert is to understand patience, adaptation, and the quiet power of survival.

 и озвучен с помощью трех различных методов:

### 1. Синтез через внешнее API (Zvukogram / Google TTS)

* **Использованный сервис: Zvukogram** 
* **Результат:** `abbi.mp3`.

### 2. Синтез с помощью Tortoise TTS

* **Модель:** [neonbjb/tortoise-tts](!pip install gtts -qq)
* **Результат:** `gtts_api_output.mp3`

### 3. (Опционально) Синтез с помощью Hugging Face VITS

* **Модель:** `facebook/mms-tts-eng`
* **Результат:** `neural_tts_hf.wav`

---

##  Содержимое репозитория

* **`TTS_Системы.ipynb`**: Основной ноутбук Google Colab с кодом для установки, загрузки моделей, синтеза речи и сравнения.
* **`abbi.mp3`** (или другой файл): Аудио, сгенерированное через API.
* **`gtts_api_output.mp3`**: Аудио, сгенерированное моделью Tortoise TTS.
* **`neural_tts_hf.wav`** (опционально): Аудио, сгенерированное моделью VITS из Hugging Face.

---

##  Сравнение моделей и личное мнение

* Синтезирование через Tortoise TTS звучит роботизоровано и не истественно
* Синтезирование через  Hugging Face звучит хорошо, но кажество звука хуже
* Синтез черзе стороние API намного луше всех предыдущих
