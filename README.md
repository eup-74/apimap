# 어디까지 갈까?

출발지와 도착지를 검색해 자동차 경로 거리와 예상 소요 시간을 확인하는 정적 웹앱입니다.

## 실행

`index.html`을 브라우저에서 열거나 프로젝트 루트에서 정적 파일 서버를 실행합니다. 빌드 단계나 패키지 설치가 필요하지 않습니다.

## Vercel 배포

GitHub 저장소에 `index.html`과 `README.md`를 올린 다음 Vercel에서 저장소를 Import하면 됩니다. 프레임워크는 **Other**를 선택하고 Build Command와 Output Directory는 비워 둡니다. 환경변수, Redis, 서버리스 함수는 필요하지 않습니다.

## 데이터 제공자

- 장소 검색: [OpenStreetMap Nominatim](https://nominatim.openstreetmap.org/)
- 자동차 경로: [OSRM 공개 데모 서버](https://router.project-osrm.org/)
- 지도: [OpenStreetMap](https://www.openstreetmap.org/)

검색어는 입력 중 짧게 기다린 뒤 조회하며, 검색 요청을 순차 처리하고 같은 검색어의 결과를 브라우저 메모리에 캐시합니다. 공개 데모 서버는 사용량 제한이나 일시적 장애가 있을 수 있으며 상용 서비스 수준의 가용성을 보장하지 않습니다. 대량 트래픽이 예상되는 서비스는 각 제공자의 사용 정책을 확인하고 적합한 호스팅 서비스를 선택해야 합니다.
