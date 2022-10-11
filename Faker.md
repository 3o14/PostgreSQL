# ._.) 파이썬으로 가짜 데이터 생성하기 Faker

<br/>

## 🖥 가짜 데이터
소프트웨어를 개발하다 보면, 특히 시제품(prototype)을 개발하거나, 단위 테스트를 작성할 때 가짜 데이터가 필요할 때가 있습니다. 이럴 때, 직접 가짜 데이터를 하드코딩(hard-coding)할 수도 있겠지만, 좀 더 쉽고 빠르게 가짜 데이터를 얻을 수 있는 방법이 있어서 소개드리려고 합니다. 바로, Faker라는 라이브러리인데요. Faker를 사용하면 가짜 데이터를 정말 너무 간단하게 생성할 수 있습니다. 👍

<br/><br/>

## 🖥 패키지 설치
```python
$ pip install Faker
```
<br/><br/>

## 🖥 패키지 임포트
```python
$ python
>>> from faker import Faker
```
<br/><br/>

## 🖥 가짜 이름 생성
`name()` 메서드를 사용하면 간단하게 가짜 이름을 생성할 수 있습니다.

```python
>>> fake = Faker()
>>> fake
>>> fake.name()
'Jamie Wood'
>>> fake.name()
'Brenda Smith'
>>> fake.name()
'Susan Davis'
```

만약에 한국어로 가짜 이름이 필요하다면, Faker 인스턴스를 생성할 때, "ko_KR"을 넘겨주면 됩니다.

```python
>>> fake = Faker("ko_KR")
>>> fake.name()
'한미경'
>>> fake.name()
'차명숙'
>>> fake.name()
'서진호'
```

<br/><br/>

## 🖥 가짜 주소 생성
```python
>>> fake = Faker()
>>> fake.address()
'5165 Beck Square\nEast Stevenview, CA 56728'
>>> fake.address()
'413 Eugene Run Apt. 897\nNew Derekview, MS 96196'
>>> fake.address()
'974 Steven Road Suite 716\nNorth Paul, IN 37971'
```

```python
>>> fake = Faker("ko_KR")
>>> fake.address()
'광주광역시 종로구 학동거리 (민석윤윤마을)'
>>> fake.address()
'충청북도 영동군 양재천8길 (성수손이동)'
>>> fake.address()
'부산광역시 남구 석촌호수01거리'
```


<br/><br/>

## 🖥 가짜 IP 주소 생성
```python
>>> fake.ipv4_private()
'10.59.101.64'
>>> fake.ipv4_private()
'192.168.31.182'
>>> fake.ipv4_private()
'10.214.166.132'
```
<br/><br/>

## 🖥 가짜 유저 생성

위와 같이 단순한 데이터 뿐만 아니라 유저 정보와 같은 복잡한 가짜 데이터 생성도 가능합니다.

```py
>>> fake = Faker("ko_KR")
>>> fake.profile()
{'job': '광석 및 석제품 가공기 조작원', 'company': '(주) 이', 'ssn': '690002-2669541', 'residence': '부산광역시 중구 가락68로 (지우김박리)', 'current_location': (Decimal('15.3446765blood_group': 'AB-', 'website': ['http://www.yu.com/'], 'username': 'baghyeonu', 'name': '김정수', 'sex': 'M', 'address': '울산광역시 영등포구 선릉거리', 'mail': 'ajeong@dreamwiz.co date(1960, 8, 25)}
>>> fake.profile()
{'job': '택시 운전원', 'company': '유한회사 김', 'ssn': '460516-1023548', 'residence': '세종특별자치시 강남구 언주가 (영순최박읍)', 'current_location': (Decimal('-15.7989395'), Decimal('147.654997')), 'blood_g
roup': 'A+', 'website': ['https://www.igim.net/'], 'username': 'cunja94', 'name': '서건우', 'sex': 'M', 'address': '강원도 성남시 분당구 압구정로 (상호고마을)', 'mail': 'cunjajang@hotmail.com', 'birthda
te': date(1937, 4, 9)}
>>> fake.profile()
{'job': '펄프 및 종이 제조장치 조작원', 'company': '강최류', 'ssn': '100604-2394559', 'residence': '제주특별자치도 연천군 석촌호수로 (정자최김읍)', 'current_location': (Decimal('-89.653332'), Decimal('166.852129')),
'blood_group': 'O+', 'website': ['http://ju.net/'], 'username': 'yejun15', 'name': '김은주', 'sex': 'F', 'address': '대구광역시 영등포구 오금289로', 'mail': 'jbag@daum.net', 'birthdate': date(1947
, 8, 3)}
```

<br/><br/>

## 🖥 아무말 대잔치

```py
>>> fake.word()
'nemo'
>>> fake.words()
['voluptatibus', 'doloribus', 'saepe']
>>> fake.sentence()
'Ea consectetur soluta accusantium aperiam.'
>>> fake.sentences()
['Consequuntur sed deserunt laborum molestiae provident.', 'Numquam recusandae corrupti voluptate autem libero commodi atque.', 'Eum repellat optio aspernatur voluptate fugit archit
ecto.']
>>> fake.paragraph()
'Natus tempore unde illum ipsa. Voluptate at quisquam saepe quisquam at. Explicabo veritatis tenetur natus.'
>>> fake.text()
'A occaecati tempora beatae optio nihil. Est sapiente doloribus assumenda eaque ipsa autem. Est facilis quibusdam consectetur occaecati occaecati. Nam in adipisci fuga eum debitis.'
```

[faker 사용하기](https://wikidocs.net/105448)
