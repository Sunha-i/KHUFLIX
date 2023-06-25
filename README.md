# <img width="13.5%" src="https://github.com/Sunha-i/KHUFLIX/assets/74592552/a9347ca7-e2d0-467b-b94b-61e6834b04df"/> using AWS, Node js
> <samp>[2021-2] OpenSource SW Development Team Project ✘</samp><code>2021.9.18 ~ 2021.12.11</code>

## 👀 Preview

|<img width="1552" alt="first_page" src="https://github.com/Sunha-i/KHUFLIX/assets/74592552/9f721021-f400-4ade-9f47-c9477fda31bd">|<img width="1552" alt="main_page" src="https://github.com/Sunha-i/KHUFLIX/assets/74592552/8d5226dd-77d1-4d1f-93f6-f89e06cd0ed0">|
|---|---|

[🔗_더보기](https://tothelune.tistory.com/141)  

## :heart: KhuFlix
- Node.js를 사용한 Netflix와 유사한 서비스 만들어보기 
- Create similar service to Netflix with Node js

## :wavy_dash: Configuration
1. Frontend : Html, CSS, Vanilla Javascript, ejs
2. Backend : Node.js
3. Database : Mongo Atlas
4. AWS : EC2

## :point_down: Branch Name
- aylee, shPark: Front-End
- yhLim: Back-End

## :scroll: DB Schema
### Users collection
```
{
    name: {type: String, required: false},
    id: {type: String, required: true, unique: true},
    pw: {type: String, required: false}, 
    history:[{title:String, episode:Number}], 
    like:[{title:String}] 
}
```
### Vidoes collection
```
{
    title: String,
    src: String, 
    content: String,
    cast: String,
    feature: String,
    genre: String,
    ost: [{song: String, singer: String, ost_src: String}],
    episode: [{time: Number, epi_content: String, epi_src: String, epi_title: String}],
    type: String, 
    category: String 
}
```

## :banana: Prerequisit
- node v16.X<br>
- npm v8.x<br>
- <a href="https://www.mongodb.com/try/download/enterprise">Mongo DB v.5.0.3</a><br>
- <a href="https://developers.kakao.com/console/app">카카오 로그인 API KEY발급</a>(필수 동의 항목: 닉네임)<br>
- <a href="https://developers.naver.com/apps/#/register">네이버 로그인 API KEY발급</a>(필수 동의 항목: 회원이름, 이메일주소)

## :monkey: Required File
위 저장소를 클론한 후 config/secret.js 파일의 빈칸을 채워주세요. 내용은 다음과 같습니다.
```
module.exports={
    'mongoDB':{
        'password':'로컬DB 사용 시 안 채워도 됩니다.',
        'local_URL':'mongodb://localhost:27017/yourDBname'
    },
    'naver':{
        'clientID':'Yours',
        'clientSecret':'Yours',
        'callbackURL':'http://localhost:4000/auth/naver/callback'
    },
    'kakao':{
        'clientID': 'Yours',
        'callbackURL': 'http://localhost:4000/auth/kakao/callback'
    }
}
```

## :star2: Install
```sh
npm install
```

## :alien: Run program
```sh
npm start
```
동영상 데이터 셋팅을 위해 <a href="http://localhost:4000/set_videos">localhost:4000/set_videos</a>에 접속해주세요.<br>
모든 준비가 완료 되었습니다. <a href="http://localhost:4000/first">localhost:4000/first</a>로 접속하여 영상을 즐겨주세요.


## :grey_exclamation: Reference links
<a href="https://www.w3schools.com/">W3school</a><br>
<a href="https://developer.mozilla.org/ko/docs/Mozilla">Mozilla</a><br>
<a href="http://www.passportjs.org/">Passport JS</a><br>
<a href="https://developers.naver.com/main/">Naver Developer</a><br>
<a href="https://developers.kakao.com/">Kakao Developer</a><br>
<a href="https://mongoosejs.com/">Mongoose</a><br>
<a href="https://aws.amazon.com/free/?trk=ps_a134p000003yHYmAAM&trkCampaign=acq_paid_search_brand&sc_channel=PS&sc_campaign=acquisition_KR&sc_publisher=Google&sc_category=Core-Main&sc_country=KR&sc_geo=APAC&sc_outcome=acq&sc_detail=aws&sc_content=Brand_Core_aws_e&sc_segment=444218215904&sc_medium=ACQ-P|PS-GO|Brand|Desktop|SU|Core-Main|Core|KR|EN|Text&s_kwcid=AL!4422!3!444218215904!e!!g!!aws&ef_id=Cj0KCQiAqbyNBhC2ARIsALDwAsDK3D5JI3YOpoI3HUBy3nGyWe-N5Dr0FLUGNXLk7DEtpO3vOcfcQDgaAtodEALw_wcB:G:s&s_kwcid=AL!4422!3!444218215904!e!!g!!aws&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all">AWS</a>

## :heavy_check_mark: Pages
- First
- Login
- Signup
- Main
- Search
- Detail
- Movie
- TV program
- Like

## © License
> MIT License Copyright(c) [Sunha Park]<br>
> MIT License Copyright(c) [Ahyoung Lee]<br>
> MIT License Copyright(c) [Yunhui Lim]

## :envelope: Contact
이용 중 궁금한 사항 있으시면 아래로 연락부탁드립니다.
- Email: khuflix@gmail.com
