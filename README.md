# โครงการพยากรณ์อากาศ

โปรเจคนี้เป็นสคริปต์ Python ที่ใช้ในการดึงข้อมูลพยากรณ์อากาศจาก API ของกรมอุตุนิยมวิทยาและบันทึกข้อมูลลงในไฟล์ CSV

## การติดตั้ง

### 1. คัดลอกไฟล์และติดตั้งแพ็คเกจที่จำเป็น

1. ดาวน์โหลดหรือคัดลอกไฟล์ทั้งหมดจากโปรเจคนี้ไปยังเครื่องของคุณ

    ```bash
    git clone https://github.com/pyyupsk/weather-forecasting-project.git
    ```

2. เปิด Command Prompt หรือ Terminal และนำทางไปยังโฟลเดอร์โปรเจค

    ```bash
    cd weather-forecasting-project
    ```

### 2. สร้างและติดตั้งสภาพแวดล้อมเสมือน (Virtual Environment)

- **Windows**

  ```bash
  setup.bat
  ```

- **macOS/Linux** (ถ้าต้องการใช้ระบบปฏิบัติการอื่น จะต้องสร้างสคริปต์ที่คล้ายกัน)

  ```bash
  python -m venv venv
  source venv/bin/activate
  pip install -r requirements.txt
  ```

### 3. รันโปรเจค

- **Windows**

  ```bash
  run.bat
  ```

  หรือรันโดยตรงจาก Python

  ```bash
  python src/main.py
  ```

## การตั้งค่า

1. สร้างไฟล์ `.env` ในโฟลเดอร์หลักของโปรเจค
2. ใส่โทเค็น API ของกรมอุตุนิยมวิทยาลงในไฟล์ `.env` ด้วยรูปแบบนี้:

   ```
   TMD_API_TOKEN=your_api_token_here
   ```

## การใช้งาน

เมื่อรันสคริปต์ `src/main.py` โปรแกรมจะ:

1. โหลด API Token จากไฟล์ `.env`
2. ดึงข้อมูลพยากรณ์อากาศจาก API โดยใช้ข้อมูลที่กำหนด
3. บันทึกข้อมูลลงในไฟล์ `weather_forecast_data.csv`

## การตั้งค่ารหัส (Code Style)

โปรเจคนี้ใช้ [flake8](https://flake8.pycqa.org/) สำหรับการตรวจสอบรหัสและมีการตั้งค่า `max-line-length` เป็น 120 ตัวอักษร

สามารถทำการตั้งค่าได้ดังนี้จากไฟล์ [`setup.cfg`](setup.cfg)

```toml
[flake8]
max-line-length = 120
```

## ข้อผิดพลาดทั่วไป

- ถ้าคุณพบข้อผิดพลาดเกี่ยวกับการติดตั้งแพ็คเกจหรือการสร้างสภาพแวดล้อมเสมือน โปรดตรวจสอบว่าได้ติดตั้ง Python และ Pip แล้ว
- ตรวจสอบว่าได้ใส่โทเค็น API ในไฟล์ `.env` ถูกต้องหรือไม่

---