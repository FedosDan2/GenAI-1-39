# Генератор пошаговых инструкций

Проект для генерации структурированных пошаговых инструкций с использованием языковых моделей. 
Реализовано два подхода: использование библиотеки Transformers и локальной модели через Ollama.

## 📋 О проекте

Изначально проект использовал библиотеку `transformers` для доступа к многочисленным предобученным моделям, точнее в моём коде исползовалась модель **sberbank-ai/rugpt3large_based_on_gpt2**  (`using_transformers.py`). Задача была решена, однако эксперименты показали, что модели, доступные через Transformers, часто генерируют нерелевантные, несвязные или низкокачественные ответы на русском языке.

Было принято решение попробовать также решить данную задачу через использование **Ollama**, модель **llama2** (`using_ollama.py`), который предоставляет:
- Локальный запуск моделей
- Высокое качество генерации на русском языке
- Стабильность работы
- Четкое следование инструкциям промпта

## Установка и запуск

# ДЛЯ using_transformers.py
```bash
pip install torch transformers
python using_transformers.py

# ДЛЯ using_transformers.py

## Установка Ollama

## Windows
- Скачайте установщик: Ollama Windows Installer https://ollama.com/download/windows
- Запустите установку и следуйте инструкциям

## MacOS
### Установка через Homebrew
brew install ollama
### Или скачайте вручную: Ollama macOS Installer https://ollama.com/download/mac

## Linux
### Установка через bash
curl -fsSL https://ollama.ai/install.sh | sh
### Или скачайте вручную: Ollama Linux Installer https://ollama.com/download/linux


## Загрузка модели
ollama pull llama2