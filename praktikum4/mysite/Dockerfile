# Gunakan image Python resmi sebagai base image
FROM python:3.12

# Atur variabel lingkungan
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Buat direktori kerja di dalam container
WORKDIR /app

# Copy file requirements.txt ke direktori kerja di dalam container
COPY requirements.txt .

# Install dependencies
RUN pip install --upgrade pip && \
    pip install -r requirements.txt

# Copy seluruh kode aplikasi ke dalam container
COPY . .

# Jalankan perintah untuk menginisialisasi dan menjalankan server Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8080"]
