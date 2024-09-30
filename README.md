# locale-th-TH

Repo สำหรับภาษาไทย ใน repo นี้ประกอบด้วยไฟล์ภาษาอังกฤษสำหรับการสำรวจ State of JS/CSS/HTML/อื่นๆ จาก repo `en-US`

## วิธีช่วย

#### 1. อาสาเป็นผู้แปล

หากคุณต้องการเริ่มช่วยแปลการสำรวจ คุณควรเข้าร่วม Discord และส่งข้อความถึง SachaG พร้อมระบุชื่อผู้ใช้ GitHub ของคุณและโค้ด locale (ของไทยคือ th-TH)

หลังจากนั้น จะได้สิทธิ์การเป็นผู้ดูแล repo ซึ่งมีไฟล์ yaml สำหรับการแปลทั้งหมด และสามารถจัดการได้เองกับสมาชิกคนอื่นๆในทีมแปล

#### 2. การหาสิ่งที่ต้องแปล

เพื่อค้นหาข้อความที่ยังไม่ได้แปล คุณสามารถเข้าไปเรียกดูแอปที่ใช้ในการทำแบบสำรวจ เว็บไซต์ผลลัพธ์การสำรวจ ฯลฯ หรือคุณสามารถใช้ API ของเราเพื่อรับข้อมูลเพิ่มเติม เช่น เปอร์เซ็นต์การแปลที่เสร็จสิ้นสำหรับ locale หรือรายการข้อความที่ยังไม่ได้แปล:

- https://graphiql.devographics.com/

ตัวอย่าง query:

```graphql
query GetLocaleData {
  locale(localeId: ru_RU) {
    completion
    totalCount
    translatedCount
    translators
    untranslatedKeys
  }
}
```

#### 3. การรับเครดิต

ผู้แปลทุกคนจะได้รับเครดิตในทุกเว็บไซต์ที่ใช้การแปลเหล่านี้ โดยเริ่มต้นที่แอปที่ใช้ทำแบบสำรวจเพื่อรับเครดิต กรุณาเพิ่มชื่อผู้ใช้ GitHub ของคุณใน array `translators` ในไฟล์ `config.yml` ของแต่ละ locale

ตัวอย่างสำหรับ locale `de-DE`:

https://github.com/Devographics/locale-de-DE/blob/main/config.yml#L3

#### 4. Push เข้าโปรดักชั่น

ในปัจจุบันยังไม่มีการอัปเดตแอปผลิตโดยอัตโนมัติเมื่อมีการอัปเดตการแปล ดังนั้นวิธีที่ดีที่สุดตอนนี้คือส่งข้อความถึงคุณ SachaG ใน Discord เพื่อแจ้งเมื่อทำเสร็จแล้ว

## ไฟล์การแปล

#### Surveys App

ข้อความเหล่านี้เกี่ยวข้องกับแอปที่ใช้ในการทำแบบสำรวจ

- `surveys.yml`
- `accounts.yml`
- `state_of_js_2020_survey.yml`

#### Results App

ข้อความเหล่านี้จะปรากฏเฉพาะในเว็บไซต์แบบสแตติกที่แสดงผลลัพธ์และสถิติของการสำรวจ

- `results.yml`
- `state_of_css_2020.yml`
- `state_of_js_2020.yml`

#### ทั้งสองอย่าง

ข้อความเหล่านี้จะปรากฏในทั้งสองแอป

- `common.yml`
- `state_of_css.yml`
- `state_of_js.yml`

#### อื่นๆ

- `homepage.yml`

## เข้าร่วมทีมแปล

เราแนะนำให้เข้า[ทีมแปล](https://github.com/orgs/Devographics/teams/translators/teams)

## Local Development

วิธีการเห็นสิ่งที่ตัวเองเปลี่ยนจาก local ยังไม่มีครับ #กำลังสร้างมองข้ามไปก่อน

## Getting Help

เข้า[Discord ของเรา](https://discord.gg/zRDb35jfrt)