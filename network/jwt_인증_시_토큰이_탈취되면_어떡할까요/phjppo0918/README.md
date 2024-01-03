많은 방법이 있겠지만, refresh token rotation을 도입하면 좋을 것 같습니다. 

refresh token을 통한 access 재발급시 refresh token 또한 갱신하고, 만약 갱신 이전 refresh token으로 재발급을 시도하면 토큰이 탈취되었다 간주하고 해당 유저와 대응되는 refresh token을 삭제해 더이상 갱신이 불가능하게끔 하는 방식입니다. 

물론 이 방법이 완벽히 해결하는 방법은 아니라고 생각합니다. 해킹 이후에 정상 유저가 장기간 미접속하여 refresh 요청을 안보내면 해커가 지속적으로 재발급할 수 있다는 문제가 그대로 남아있습니다.
결국 클라이언트 측에서도 토큰을 탈취당하지 않도록 잘 관리하는 것이 중요하다고 생각합니다.

# 참고
https://mgyo.tistory.com/832