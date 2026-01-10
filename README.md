# Docker Dashboard

Vite 기반의 대시보드 프론트엔드 프로젝트입니다. `apexcharts`로 차트를 렌더링하고, `axios`로 API 요청을 수행하도록 구성되어 있습니다.

## 기술 스택

- Vite + TypeScript
- ApexCharts
- Axios

## 로컬 개발

```bash
npm install
npm run dev
```

## 프로덕션 빌드

```bash
npm run build
npm run preview
```

## Docker로 실행

멀티 스테이지 Dockerfile을 통해 빌드 후 Nginx로 정적 파일을 제공합니다.

```bash
docker build -t docker-dashboard .

docker run --rm -p 8080:80 docker-dashboard
```

브라우저에서 `http://localhost:8080`으로 접속합니다.
