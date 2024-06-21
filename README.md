Weekend Fun

Quick weekend fun to play around with your skills. Use the 2GB JSON file to insert rows into an SQL table. You can use any programming language or tools to accomplish this task. The goal is to insert the rows as fast as possible.

Download the JSON file [here](https://drive.google.com/file/d/1t6WjsOxMXzq8yZn_i_zqWnqmAz6xfXnO/view?usp=share_link).

The JSON file is an array of objects. Each object has the following schema:

```json
{
  "_id": {
    "$oid": "654229ef8f2793f66f3373e9"
  },
  "product_id": 100000,
  "text": "Greek liquor with a dry taste of anise.",
  "translations": {
    "RU": "Греческий ликер с сухим вкусом аниса.",
    "UK": "Грецький лікер із сухим смаком анісу.",
    "BG": "Гръцки ликьор със сух вкус на анасон.",
    "HR": "Grčki liker sa suhim okusom anisa.",
    "CS": "Řecký alkohol s suchou chutí anýzu.",
    "DA": "Græsk spiritus med en tør smag af anis.",
    "NL": "Griekse likeur met een droge smaak van anijs.",
    "EN": "Greek liquor with a dry taste of anise.",
    "ET": "Kreeka liköör aniisi kuiva maitsega.",
    "FI": "Kreikkalainen viina, jossa kuivaa aniksen makua.",
    "FR": "Liqueur grecque au goût sec d'anis.",
    "DE": "Griechischer Likör mit trockenem Anisgeschmack.",
    "EL": "Ελληνικό λικέρ με ξηρή γεύση γλυκάνισου.",
    "HU": "Görög likőr ánizs száraz ízével.",
    "GA": "Deochanna na Gréige le blas tirim anise.",
    "IT": "Liquore greco dal gusto secco di anice.",
    "LV": "Grieķu lakrica ar sausu anīsa garšu.",
    "LT": "Graikiškas alkoholinis gėrimas su sausu anyžių skoniu.",
    "MT": "Likur Grieg b'togħma niexfa ta 'anisi.",
    "PL": "Grecki trunek o wytrawnym smaku anyżu.",
    "PT": "Licor grego com um sabor seco de anis.",
    "RO": "Lichior grecesc cu gust uscat de anason.",
    "SK": "Grécky likér so suchou chuťou anízu.",
    "SL": "Grški liker s suhim okusom po janežu.",
    "ES": "Licor griego con sabor seco de anís.",
    "SV": "Grekisk sprit med en torr smak av anis.",
    "JA": "アニスの辛口の味わいが特徴のギリシャのお酒。",
    "ZH": "带有干茴香味道的希腊酒。",
    "KO": "그리스 주류의 건조 맛의 맛.",
    "HI": "सौंफ के सूखे स्वाद के साथ ग्रीक शराब।",
    "ID": "Minuman keras Yunani dengan rasa adas manis kering.",
    "TR": "Kuru anason tadında Yunan likörü.",
    "CA": "El licor grec amb un gust sec d'anise.",
    "VI": "Rượu Hy Lạp có vị khô của cây hồi.",
    "TH": "เหล้ากรีกที่มีรสชาติแห้งของโป๊ยกั๊ก",
    "NO": "Gresk brennevin med en tørr smak av anis.",
    "SR": "Grèko piæe sa suvim ukusom anisa.",
    "MS": "Minuman keras Yunani dengan rasa kering anise.",
    "BN": "মৌরি একটি শুকনো স্বাদ সঙ্গে গ্রীক মদ.",
    "SW": "Pombe ya Kigiriki na ladha kavu ya anise."
  },
  "createdAt": {
    "$date": "2023-11-01T10:35:27.508Z"
  },
  "__v": 0
}
```

The SQL table schema should be as follows:

```sql
CREATE TABLE translations (
  id SERIAL PRIMARY KEY,
  product_id INT,
  text TEXT,
  lang_code VARCHAR(2),
  created_at TIMESTAMP
);
```

The `lang_code` column should contain the language code of the translation. For example, for the translation in Russian, the `lang_code` should be `RU`. Approximately 40 translations are available for each product, so you should insert 40 rows for each product. Total rows to insert are around 2,000,000.

## Submission

To submit your solution, create a new branch in this repository with the name `weekend-fun`. Push your code to this branch and create a pull request. In the pull request description, include the time it took to insert all the rows into the SQL table.

Good luck! 🚀
