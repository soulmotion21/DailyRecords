git 여러계정 permission

회사 git 계정과 내 git 계정을 동시에 사용하는 경우

각 계정별 ssh key를 발급

```shell
ssh-keygen -t rsa -C 'aaa@aaa.com'
```



해당 키를 아래와 같이조회하면 ssh-rsa.... 키가 표시됨.

ssh-rsa 부터 맨 뒤 계정 이메일 까지 복사해서 github > setting > SSH & GPG keys에 붙여넣으면 됨.

```shell
cat ~/.ssh/id_rsa.pub

ssh-rsa AAA.....
```



여러 계정에 대해 config 작성

```shell
touch ~/.ssh/config or vi ~/.ssh/config
cat ~/.ssh/config (확인할 때) 

# my account 
	Host github.com 
		User soulmotion21 
		IdentityFile ~/.ssh/id_rsa
	
# company account 
	Host github.com-company 
		User dkim-planit 
		IdentityFile ~/.ssh/id_company_rsa
		
```



저장소 url에 연결된 정보

```shell
// 나의 repository url 
git@github.com:{githubId}/{repositoryName}.git 

// 회사 repository url 
git@github.com-company:{githubId}/{repositoryName}.git

```



아래 명령어로 인증여부 확인

```shell
$ ssh -T git@github.com 
Hi name! You've successfully authenticated, but GitHub does not provide shell access. 

$ ssh -T git@github.com-company 
Hi {companyName}! You've successfully authenticated, but GitHub does not provide shell access.

```
