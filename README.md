# ELK
test ELK server

### Elasticsearch 설치
```
--실행(설치) & 실행 중 컨테이너 확인
> docker run -d --name elasticsearch-test-01 -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.5.0
> docker ps
> docker stop elasticsearch-test-01
> docker start elasticsearch-test-01
--에러시 컨테이너 이름 확인 후 삭제
> docker ps -a
> docker rm elasticsearch-test-01
> docker ps -a
> docker run -d --name elasticsearch-test-01 -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.5.0
```
설치성공 후 localhost:9200 진입 시
```
{
  "name" : "c954c8fc864b",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "T3n5dIZmQAi6egJd0dhLKA",
  "version" : {
    "number" : "7.5.0",
    "build_flavor" : "default",
    "build_type" : "docker",
    "build_hash" : "e9ccaed468e2fac2275a3761849cbee64b39519f",
    "build_date" : "2019-11-26T01:06:52.518245Z",
    "build_snapshot" : false,
    "lucene_version" : "8.3.0",
    "minimum_wire_compatibility_version" : "6.8.0",
    "minimum_index_compatibility_version" : "6.0.0-beta1"
  },
  "tagline" : "You Know, for Search"
}
```
### TDD - postman for api test 
Elasticsearch에 restful api로 데이터 저장 테스트 성공
<img width="950" alt="api-test" src="https://user-images.githubusercontent.com/37662184/74999427-fe864600-549e-11ea-98b6-d4f2b4b32b51.png">

### yarn
```
$ npm install --global yarn
$ yarn && yarn start
```



### 참고자료

* [ELK-stack](https://www.elastic.co/kr/what-is/elk-stack)  
* [ELK-typescript](https://velog.io/@jeff0720/Elasticsearch-%EC%9D%B4%ED%95%B4%EC%99%80-%EB%A1%9C%EA%B7%B8-%EC%84%9C%EB%B2%84-%EA%B5%AC%EC%B6%95-%EC%8B%A4%EC%8A%B5%EC%9C%BC%EB%A1%9C-%ED%95%B5%EC%8B%AC-%EA%B0%9C%EB%85%90-%EC%9D%B5%ED%9E%88%EA%B8%B0)  
* [ELK-spring](https://woowabros.github.io/experience/2020/01/16/set-elk-with-alarm.html)  
* [postman 사용법](https://meetup.toast.com/posts/107)  
* [yarn 사용법](https://www.vobour.com/yarn-%EC%B2%98%EC%9D%8C-%EB%B3%B4%EB%8A%94-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EC%9D%98-%EC%83%88-%ED%8C%A8%ED%82%A4%EC%A7%80-%EB%A7%A4%EB%8B%88%EC%A0%80-yarn-fir)  
* [docker docs](https://docs.docker.com/engine/reference/commandline/docker/)  
* [docker 안내서](https://subicura.com/2017/02/10/docker-guide-for-beginners-create-image-and-deploy.html)  
* [elasticsearch config module js](https://medium.com/@siddharthac6/elasticsearch-node-js-b16ea8bec427)  
* [elasticsearch js github](https://github.com/elastic/elasticsearch-js)  
* [elasticsearch js example code](https://qbox.io/blog/integrating-elasticsearch-into-node-js-application)