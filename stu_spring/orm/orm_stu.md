# ORM

## ORM을 정리하게된 이유
- 이유
    - 처음 springboot에 입문했을 때, findById, findByEmail 같은 글자를 보고, 전혀 이게 db에 연동되는 orm인줄 몰랐다.
    - 그리고 인터넷에서 나름 열심히 찾아봤는데 검색어가 잘 못 된 것인지 JPA ORM을 사용하는 방법을 찾을 수 없었다.
    - 스프링 부트를 공부하며 느꼈는데, 가장 생각을 많이 해야 하는 가장 어려운 부분이라고 생각해서

## JPA와 ORM이란
- JPA란?
    - Java Persistence API의 약자로 자바 진영의 표준 ORM 기술이다.
- JPA의 특징
    - SQL문을 개발자 대신 해 줌으로써 반복적인 CRUD를 위한 SQL을 작성하지 않아도 된다.
    - SQL문을 직접 작성하지 않아 객체가 변화해도 엔티티의 속성만 수정하면 되어 유지보수가 편하다.
    - 관계형 데이터베이스와 자바의 객체 사이의 차이로 인해 생기는 어려움을 해결해준다.
    - JPA는 표준이기 때문에 다른 프레임워크로 변경이 쉽다.
- ORM이란?
    - Object Relational Mapping 의 약자로, 관계형 데이터베이스에 매핑해주는 기술이다.
    - 객체 지향 프로그래밍 언어와 데이터베이스 간의 매핑이기 때문에 자바에만 있지 않다.
    - 즉 JPA는 ORM이라는 기술을 통해 자바의 객체와 관계형 db를 매핑시켜주는 기술이다.
- ORM의 기능
    - 우리가 적절한 ORM 코드를 짠다면, 프레임워크에서 알아서 적절한 쿼리문으로 바꿔서 실행해준다.
    - 우리가 원래 사용하던 SQL보다 직관적이다.
- ORM의 단점
    - 직접 SQL을 사용하는 것 보다 복잡해질 수도 있다.
    - 속도난 생산성이 저하될 수 있다.
    - 완전히 ORM만 사용할 수 없기 때문에 DBMS로부터 완전히 독립할 수 없다.
        - 이 경우에는 @Query(value="쿼리문")을 통해 직접적으로 SQL문을 사용할 수 있다..
    - 테이블보다 더 많은 객체를 만들게 될 수 있다.
    - 탐색과 순회에서 자바는 객체간의 연결을 통해, RDBMS는 쿼리를 최적화해서 탐색한다.