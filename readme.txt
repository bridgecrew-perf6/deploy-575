# 구조
/
 L requirements.txt : 특정 환경에서 사용한 모듈들을 기술
                      환경이 구축될 때, 이 서비스 운영/개발 시 사용한 필요한 모듈 설치
                      하기 위해 기술되는 파일이다
                      - 반드시 버전을 명시하여 향후 서버 변경되도 문제없이 구동되게끔 동일한 환경 제공
 L run.py           : 서비스 메인
 L wsgi.py          : 엔트리 포인트, 아파치 서버가 바라보는 파일이다
 L deploy.json      : 데이터통신포멧 표현 시 제이슨 사용, 페브릭이 배포 작업을 하는데 필요한 상수값들을 저장한 파일
                      - 환경변수가 저장된 파일

# fabric 설치
- pip(or conda) install fabric(x)
    => python2.7xx버전에 맞게 설치가 된다
    => python3.x버전 사용 불가
- pip(or conda) install fabric3(o)

# github 사용
1. github.com 접속 후 저장소 생성
2. 로컬 pc에서 git 명령어를 이용하여 적절한 위치 저장소를 다운로드
    - 현재위치
        - $cd / ...py_project
    - 저장소에서 카피
        - git clone https://github.com/zsdf21/deploy.git
    - 이미 작성된 내용을 카피해서 만들어진 폴더 deploy안으로 붙여넣는다
        - 커밋 메시지 작성
        - 커밋
            - 에러 : 메일 확인하라
        - 공통 처리:
        $ git config --global user.name "zsdf21"
        $ git config --global user.email "zsdf21@gmail.com"
        
