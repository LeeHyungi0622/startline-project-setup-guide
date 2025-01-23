# [스타트라인: 프로젝트 사전 셋팅 가이드](https://mike-4.gitbook.io/undefined)

(상단 링크를 클릭하면, 배포된 웹 페이지에서 확인 가능합니다)

## GitBook과 GitHub Repository 연동 및 활용

① Spaces에 노트 추가하고, 우측 상단 `Integrations` 클릭 후 `GitHub Sync` 클릭한 뒤 `Edit configuration` 하위에서 GitHub 계정 연동 및 Repository 선택을 통해 연동
(프로젝트 적용 경로를 반드시 `/(roo)`로 설정하도록 한다)

② 작성 내용을 Push한 뒤에 `Spaces` 하위 해당 노트에서 우측 상단 바로 하위에 있는 `Change requests`를 클릭하여 변경된 내용을 반영하도록 한다.
`(반영 후 1분 내외로 시간이 시간이 소요된다)`

<br/>

# 프로젝트 전체 시작 전 Outline 잡기

## ① 프로젝트 기본 설정

- 환경 구축 및 초기 실행 가능 상태 체크

- [프론트엔드 프로젝트 환경 구축](/Front-End/EnvSetting/)

  - [나만의 개발환경 셋팅하기](/Front-End/EnvSetting/1.BaseDevEnv.md)

  - [프론트엔드 프로젝트 환경 구축 관련 추가학습](/Front-End/EnvSetting/2.AdditionalStudy/)

    - [Node.js vs Deno](/Front-End/EnvSetting/2.AdditionalStudy/1.Deno_and_NodeJS.md)
    - [nvm vs fnm](/Front-End/EnvSetting/2.AdditionalStudy/2.nvm_and_fnm.md)
    - [npx 그리고 bundler](/Front-End/EnvSetting/2.AdditionalStudy/3.npx_and_bundler.md)
      - [bundler vs transpiler](/Front-End/EnvSetting/2.AdditionalStudy/3-1.bundler_and_transpiler/)
        - [Bundler and Transpiler](/Front-End/EnvSetting/2.AdditionalStudy/3-1.bundler_and_transpiler/1.Bundler_and_Transpiler.md)
        - [Bundler](/Front-End/EnvSetting/2.AdditionalStudy/3-1.bundler_and_transpiler/2.Bundler.md)
        - [Transpiler](/Front-End/EnvSetting/2.AdditionalStudy/3-1.bundler_and_transpiler/3.Transpiler.md)
        - [Parcel and Vite](/Front-End/EnvSetting/2.AdditionalStudy/3-1.bundler_and_transpiler/4.Parcel_and_Vite.md)
    - [Dependency vs DevDependency](/Front-End/EnvSetting/2.AdditionalStudy/4.devdependency_and_dependency.md)

## ② CI/CD 파이프라인 구축

### 확장성과 재사용성을 고려한 CI/CD 파이프라인 구축

- 향후 다른 프로젝트에 쉽게 연결해서 사용할 수 있도록 고려하여 구축

### 기술 스택

- React, Node.js 기반 프로젝트 기반으로 준비를 할 것이기 때문에 `GitHub Actions + Vercel or Netlify`로 진행
- 우선적으로 개인 포트폴리오 웹 사이트의 경우에는 `Turborepo` 사용
  (React와 Node.js 프로젝트에 특화되어 있으며, 프론트엔드 중심 프로젝트에 적합)
- MonoRepo와 CI/CD 파이프라인 구축하는 방향으로 진행하기 위해 `Nx` 사용

## ③ 개발

- 기능 구현 및 테스트 진행

- [React.js 개발 기본](/Front-End/ReactJS/)

  - [JSX](/React/1.Basic/1.JSX.md)
  - [React로 사고하기](/React/1.Basic/2.ThinkInReact.md)
  - [Hooks](/React/1.Basic/3.Hooks.md)
  - [Router](/React/1.Basic/4.Router.md)
  - [Navigation](/React/1.Basic/5.Navigation.md)

- [React.js 개발 심화](/Front-End/ReactJS/)

  - [useRef & Custom Hook](/Front-End/ReactJS/2.Immediate/4.UseRefCustomHook.md)
  - [usehooks-ts](/Front-End/ReactJS/2.Immediate/5.useHookTS.md)

- [TypeScript 기본](/Front-End/TypeScript/TypeScript.md)

## ④ CI/CD 파이프라인 확장

- 테스트 자동화, 다중 환경 배포 등 추가 기능 추가
