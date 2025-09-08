# code-server

This repository contains the `code-server` setup.

(이 저장소는 `code-server` 설정을 포함합니다.)

## Getting Started

(시작하기)

To get started with `code-server`, follow these steps:

(`code-server`를 시작하려면 다음 단계를 따르세요:)

1.  **Configure your `docker-compose.yml` file:**
    
    (`docker-compose.yml` 파일 설정:)

    Before running `docker-compose`, ensure you have set a strong password in your `docker-compose.yml` file. This is crucial for security.
    
    (`docker-compose`를 실행하기 전에 `docker-compose.yml` 파일에 강력한 비밀번호를 설정했는지 확인하세요. 이는 보안에 매우 중요합니다.)

    Look for the `PASSWORD` environment variable and replace `your_secure_password` with a unique and secure password.
    
    (`PASSWORD` 환경 변수를 찾아 `your_secure_password`를 고유하고 안전한 비밀번호로 바꾸세요.)

    ```yaml
    # Example snippet from docker-compose.yml
    # (docker-compose.yml 예시 코드)
    environment:
      - PASSWORD=your_secure_password # <<< CHANGE THIS!
      # (PASSWORD=your_secure_password # <<< 이 부분을 변경하세요!)
    ```


2.  **Start `code-server` using Docker Compose:**

    (Docker Compose를 사용하여 `code-server` 시작:)

    Navigate to the directory where your `docker-compose.yml` file is located and run:
    
    (`docker-compose.yml` 파일이 있는 디렉토리로 이동하여 다음을 실행하세요:)

    ```bash
    docker-compose up -d
    ```

    This command will start `code-server` in detached mode.
    
    (이 명령은 `code-server`를 백그라운드 모드로 시작합니다.)

## Important Security Note
(중요 보안 참고)

Always configure a strong password in your `docker-compose.yml` file. Running `code-server` without a password or with a weak password can expose your development environment to unauthorized access.

(`docker-compose.yml` 파일에 항상 강력한 비밀번호를 설정하세요. 비밀번호 없이 또는 약한 비밀번호로 `code-server`를 실행하면 개발 환경이 무단 액세스에 노출될 수 있습니다.)
