## GitHub Actions로 이미지 빌드 및 배포, Manifest 파일 업데이트를 통한 GitOps 설정 🖥

이 프로젝트는 간단한 API를 가진 테스트용 프로젝트입니다. <br> 
프로젝트의 목적은 다음과 같습니다:
1. GitHub Actions를 활용하여 CI(Continuous Integration) 구현
2. ArgoCD가 관리하는 Manifest 파일에 GitOps 설정 적용

### 🔄 프로젝트 흐름
1. 코드가 GitHub에 **Push**되면 GitHub Actions가 자동으로 이미지를 빌드하고 Docker Hub에 **Push**합니다.
2. 해당 이미지를 **Manifest 파일**에 업데이트합니다.
3. ArgoCD가 **GitOps**를 통해 Manifest 파일의 변경 사항을 자동으로 반영
4. 해당 이미지를 기반으로 **KIND 클러스터**에 배포
