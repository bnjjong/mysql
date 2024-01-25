# mysql

# 인스트루먼트(instrument)
> Mysql 데이터 메트릭중 하나.

# 컨슈머 (consumer)
> MySQL에서 컨슈머는 Performance_Schema에서 사용되는 개념입니다. Performance_Schema는 MySQL의 성능 모니터링을 위해 사용되며, 다양한 성능 및 관리 지표를 제공합니다

Performance_Schema는 정보를 수집하는 `'인스트루먼트(Instruments)'`와 수집한 정보를 저장하는 `'컨슈머(Consumers)'`를 설정하여 이용하는 구조입니다1.

컨슈머는 인스트루먼트가 정보를 보내는 대상을 의미합니다. Performance_Schema는 인스트루먼트 결과를 다양한 테이블에 저장하게 됩니다

예를 들어 잠금에 대한 정보를 수집하려면 `wait/lock/metadata/sql/mdl` 인스트루먼트를 활성화 해야 함.

이러한 테이블은 다른 테이블과 마찬가지로 SELECT 문을 사용하여 쿼리할 수 있습니다. 그리고 성능 스키마의 테이블은 지속적인 온디스크 스토리지를 사용하지 않는 인메모리 테이블이기 때문에, 수집된 내용은 서버 시작 시 다시 채워지고 서버 종료 시 삭제됩니다
