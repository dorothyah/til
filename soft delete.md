## Spring JPA에서 soft delete 구현하기

1. Entity 클래스에서 boolean 값으로 column을 만들어준다.

```
@Column
private boolean isDeleted = Boolean.FALSE;
```

2. 삭제 명령 재정의
```
@SQLDelete(sql = "UPDATE post SET is_deleted = true WHERE id=?")
```
delete 요청이 들어올 경우 삭제하지않고 isDeleted 값을 true로 바꿔준다.

3. 데이터 목록을 가져올때 isDeleted가 false인 값만 보여주도록 설정한다.
```
@Where(clause = "is_deleted=false")
```

4. 연관된 entity가 있을 경우 같이 삭제하기 위해서는 CascadeType.REMOVE를 사용한다.
```
@OneToMany(mappedBy = "post", cascade = CascadeType.REMOVE)
```
그리고 해당 entity에서도 위의 세 가지를 똑같이 설정해주면 된다.

참고한 자료<br>
https://velog.io/@max9106/JPA-soft-delete <br>
https://www.baeldung.com/spring-jpa-soft-delete
