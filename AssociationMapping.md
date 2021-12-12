## 연관관계 매핑, @JoinColumn

[참조1](https://victorydntmd.tistory.com/208)

### 연관관계 매핑
- 연관관계 매핑이란 객체의 참조와 테이블의 외래키를 매핑하는 것
- JPA에서는 JDBC(Mybatis)와 달리 연관관계에 있는 상대 테이블의 PK를 멤버변수로 갖지 않고, 엔티티 자체를 통째로 참조
> ```java
> //Mybatis
> private Integer categoryNo;
> 
> //Jpa
> private Category category;
> ```
- Jpa에서는 엔티티 객체를 참조.

### 방향, 다중성, 주인(Owner)
방향
- 단방향 관계 : 한 쪽이 다른 한 쪽의 엔티티만 참조
- 양방향 관계 : 두 엔티티가 서로 참조
다중성 : 다음 네 가지 중 하나
- OneToOne
- OneToMany
- ManyToOne
- ManyToMany
주인(Owner)
- 연관 관계를 갖는 두 테이블에 대해 외래키를 갖는 테이블이 주인
- 주인만이 외래 키를 관리(등록, 수정, 삭제)할 수 있고, 주인이 아니면 읽기만 가능
