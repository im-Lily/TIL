- 파이참 가상환경 설정
  - https://bskyvision.com/946
- 네이버 API 
  1. NAVER Maps JavaScript API v3 기반으로 구현
     - https://navermaps.github.io/maps.js.ncp/docs/tutorial-2-Getting-Started.html
  2. 현재 내 위치 표시 -> HTML5 Geolocation API 활용
     - https://navermaps.github.io/maps.js.ncp/docs/tutorial-6-map-geolocation.example.html
  3. DB에서 전기차 충전소 위치 데이터 불러오기
     - 전기차 충전소 위치 마커 클러스터링
     - https://navermaps.github.io/maps.js.ncp/docs/tutorial-marker-cluster.example.html
     - 이슈) 클러스터링, 보이는 영역 지도만 마커 표시 이미지 - 오류x
       - home_path / url 
         - https://github.com/navermaps/maps.js/blob/master/docs/img/cluster-marker-1.png
         - https://github.com/navermaps/maps.js/blob/master/docs/img/marker-default.png
         - static 디렉토리에 이미지 파일 존재, load static 완료
       - 참고사이트 
         - https://www.zooo.kr/fxbbs/f_view.php?i_code=program&i_id=220

- geospatial query django

- 특정 위치반경정보 필터링
  - https://velog.io/@devmin/Django-filtering-position-haversine 
- SQL 구문으로 DB 데이터 가져오기
  - https://chagokx2.tistory.com/10

- https://www.inflearn.com/course/%EC%BD%94%EB%A1%9C%EB%82%98%EB%A7%B5-%EC%A7%80%EB%8F%84%EC%84%9C%EB%B9%84%EC%8A%A4#

- 현재위치에서 반경2km 내 업체들 거리, 도보/자전거 이동거리 구하기
  - https://wonpaper.tistory.com/56
- 인포윈도우 표시
  - https://gdtbgl93.tistory.com/83
- 이슈)  query 부분 현재위치 변경, 인포윈도우 undefined, 마커 클릭 시 내 위치 사라짐
  - query 부분 현재위치 변경
    - global 변수 사용
  - 인포윈도우 undefined
    - 오타
  - 마커 클릭 시 내 위치 사라짐
    - 함수 건들여야함(난이도 상)
    - 원 상태로 복구
  - 혼잡도에 따른 마커색상 상이하게 표시
    - marker.png : https://stackoverflow.com/questions/7095574/google-maps-api-3-custom-marker-color-for-default-dot-marker
    - https://stackoverflow.com/questions/50660061/change-marker-in-map

- 발표자료 참고
  - https://github.com/nero96in/coronamap_deploy