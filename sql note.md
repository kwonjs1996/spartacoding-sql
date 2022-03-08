```sql
show tables; //데이터베이스 안에 테이블을 보여줘라


select * //모든필드 
select * from orders

모든필드 from 어디서 orders

select order_no, created_at, user_id, email from orders
 order_no, created_at, user_id, email 필드의 어디서 orders 에서

 SELECT * from orders
where payment_method = 'kakaopay'
모든 필드에서 orders를 불러오고 payment_method중 kakaopay를 가져와라
문자열을 가져온다는것 '' 사용하기

SELECT * from point_users
where point >= 5000

모든필드의 point_users에서 포인트가 5000점 이상인 것을 찾아라

SELECT * from orders
where course_title = '앱개발 종합반' and payment_method = 'CARD'

orders를 불러오고 그 중 앱개발 종합반 이면서 결제수단이 카드인 데이터를 가져와라
and 둘 다  or 이거나

// where 절과 함께 자주 쓰는 문법
// != = 같지않음, between a and b //범위//,
// in(a,b,c...) //포함//, like '%아무거나' //문자열규칙// '%아무거나' % 앞에 뭐가있던 아무거나가 들어가는것,
///  limit a ///a 갯수만큼만 데이터를 보겠다.///
/// distinct(abc)///abc 안의 데이터를 중복제거하고 보겠다/// select distinct(abc) from abc///
/// count(*)  ///안에 들어있는 정보가 몇개냐/// select count(*) from ABC///
/// naver 이메일을 사용하면서, 웹개발 종합반을 신청했고 결제는 kakaopay로 이뤄진 주문데이터 추출하기
SELECT * from orders
where email like '%naver.com' and 
course_title = '웹개발 종합반' and
payment_method = 'kakaopay'
```
