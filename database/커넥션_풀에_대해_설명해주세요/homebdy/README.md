데이터베이스와 연결된 커넥션을 미리 만들어 놓고 이를 pool로 관리하는 기법입니다.
즉, 필요할 때마다 커넥션 풀의 커넥션을 이용하고 반환하는 기법입니다.

커넥션 풀 기법을 이용하면 미리 만들어 놓은 커넥션을 이용하면 커넥션을 생성하는데 필요한 비용을 줄여 DB에 빠르게 접속할 수 있습니다.