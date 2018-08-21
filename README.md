# [BenignDeus.github.io](https://benigndeus.github.io)

---
## [git] [GitHub] [error] `[git the requested URL returend error : 403]`
Local에서 https형식으로 push가 안 되는 경우에는 다음과 같은 일을 해야 한다. Google에서 검색해봐도 반은 ssh형식으로 바꾸라는 말이고, 확실한 해결법을 제공해주지는 않는다. 내 경우는 예전에 다른 GitHub 아이디를 사용하여 git Bash를 이용했었는데, 컴퓨터에는 그 로그(?)가 남아있었다. 따라서 Windows환경에서는 그 로그를 제거해줘야 https형식의 push가 가능하다. 다음은 그 해결책이다.

>1. 제어판
>2. 자격 증명 관리자
>3. Windows 자격 증명
>4. 일반 자격 증명
>5. 'git:https://github' 제거

그러면 드디어 git Bash에서 제대로 로그인이 가능하다.

---