> aws cli로 s3 객체 접근 방법
1. `brew install awscli`로 설치
- `aws configure`로 aws credential 설정
- `aws s3 ls`로  버킷 목록 조회
- `aws s3 ls s3://(버킷명)`으로 버킷 내 파일 목록 조회
- `aws s3api list-objects --bucket (버킷명) --query 'Contents[].Key' > s3KeyList.json`
    - 해당 버킷에 있는 모든 객체의 key 값만 뽑아서 s3KeyList.json 파일에 저장
    - `aws s3api list-objects --bucket (버킷명) --query 'Contents[].{Key: Key}' > s3KeyList.json` 처럼 원하는 형식으로 추출 가능
