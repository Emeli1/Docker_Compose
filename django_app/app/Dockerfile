# Используем официальный образ Python
FROM python:3.9

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем файлы requirements
COPY ../requirementsv.txt /app/requirements.txt

# Устанавливаем зависимости
RUN pip install -r requirements.txt

# Копируем проект
COPY . /app/

# Запускаем сервер Django
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "logistic.wsgi:application"]


