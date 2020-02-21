# ELK
test ELK server

### Elasticsearch 설치
```
> docker run -d --name elasticsearch-test-01 -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.5.0
```
설치성공 후 
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




### 참고자료

[ELK-stack](https://www.elastic.co/kr/what-is/elk-stack)  
[ELK-typescript](https://velog.io/@jeff0720/Elasticsearch-%EC%9D%B4%ED%95%B4%EC%99%80-%EB%A1%9C%EA%B7%B8-%EC%84%9C%EB%B2%84-%EA%B5%AC%EC%B6%95-%EC%8B%A4%EC%8A%B5%EC%9C%BC%EB%A1%9C-%ED%95%B5%EC%8B%AC-%EA%B0%9C%EB%85%90-%EC%9D%B5%ED%9E%88%EA%B8%B0)
[ELK-spring](https://woowabros.github.io/experience/2020/01/16/set-elk-with-alarm.html)
[postman 사용법](https://meetup.toast.com/posts/107)