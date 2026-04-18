LangGraph Multi-Agent System.
Это не просто чат-бот, а фабрика агентов.
Убраны 'галлюцинации' искуственного интелекта и даю контроль над расходами через оркестрацию.

Эта  система автоматизирует работу с документами и базами данных через ИИ. Компания тратит 20 часов в неделю на поиск информации в договорах и отчётах — мой агент делает это за 5 секунд. Экономия времени — 80%. Мультиагентная система, построенная на LangGraph, объединяющая трех специализированных агентов для решения различных задач. Система развернута в **Kubernetes** и предоставляет REST API, веб-интерфейс и полноценный мониторинг.

Добавлен ClickHouse и превратила систему из «аналитического помощника» в промышленную аналитическую платформу реального времени. ClickHouse идеально подходит для хранения и анализа больших объёмов логов, метрик, истории диалогов и результатов работы агентов.

- DEMO (видео на Youtube) - https://youtube.com/shorts/wrsNgsw41LU?si=5tRZj8XAlcaQAcrI


### Основные возможности

- RAG Agent- поиск информации по документам с Elasticsearch.
- SQL Agent- выполнение SQL запросов к PostgreSQL.
- Chat Agent- диалоговый ассистент.

- Загрузка документов | Поддержка TXT, PDF, DOCX.
- REST API- автоматическая документация Swagger.
- Веб-интерфейс- Streamlit UI для удобного взаимодействия.
- Мониторинг- Prometheus + Grafana для отслеживания метрик.
- Оркестрация- Kubernetes для масштабирования.


## Технологический стек

- Оркестратор- LangGraph/Управление агентами и состоянием.
- API- FastAPI/RESTful API сервер. 
- UI- Streamlit/Веб-интерфейс.
- База данных- PostgreSQL/Хранение бизнес-данных.
- Поиск- Elasticsearch/Векторный поиск для RAG. 
- Мониторинг-Prometheus + Grafana/Сбор метрик и визуализация.
- Логи- Kibana/Анализ логов.
- Контейнеризация- Docker/Упаковка приложения
- Оркестрация- Kubernetes (Minikube)/Развертывание и масштабирование.

## Быстрый старт

### Предварительные требования

- Python 3.12+
- Docker Desktop
- Minikube
- kubectl


##  Быстрый старт

```bash
# Клонирование
git clone https://github.com/proteinovaya111/Multi-Agent_System.git
cd Multi-Agent_System

# Установка
python -m venv langgraph-env
source langgraph-env/bin/activate  # Windows: .\langgraph-env\Scripts\Activate.ps1
pip install -r requirements.txt

# Запуск сервисов (PostgreSQL, Elasticsearch, Prometheus, Grafana)
docker-compose up -d

# Запуск API
python src/api.py

# В другом окне — веб-интерфейс
streamlit run streamlit_app.py


# Упаковка https://railway.com/workspace/upgrade (30 дней бесплатного пользования, дальше 5 $).
