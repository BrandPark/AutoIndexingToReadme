# auto-indexing-README-for-TIL

TIL을 작성할 때 Index를 직접 수정하는 작업이 번거로워 만들었습니다.

`git hook`을 사용하여 **Commit을 README.md 파일에 인덱스를 만들어주거나 수정하는 작업을 자동으로 해줍니다.**

# Setting
1. `.git/hooks/`에 `pre-commit`파일을 넣습니다.
2. `PreCommit.java` 파일과 `README.md` 파일을 `.git`이 있는 곳에 넣습니다.

# 주의사항
- `.git`이 있는 곳에 `PreCommit.java`와 README.md가 있어야 합니다.
- `{Index}` 또는 `# Index`를 찾아서 해당 위치에 넣습니다. TIL 설명과 Index만 있는 상황을 가정했기 때문에 **해당 키워드 뒤의 내용은 사라지니 주의**해야합니다.
- 인덱스의 구조는 Category-files 구조로 깊이 1만큼만 탐색합니다.

# 사용법

#### 1. README.md 파일에 인덱스를 넣을 위치를 지정한다.

![image](https://user-images.githubusercontent.com/53790137/152467925-fb2536dd-3bc9-4481-b76f-92b76409416a.png)

#### 2. commit 한다.

![image](https://user-images.githubusercontent.com/53790137/152467233-0f14a9db-187a-4f33-b324-9d1204bcbc49.png)

#### 3. 결과 확인

![image](https://user-images.githubusercontent.com/53790137/152467784-f1c75fd5-cc39-42bd-ad75-9cc23919138b.png)

