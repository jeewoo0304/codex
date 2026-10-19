# React Publishing Guidelines (Backend Integration Pending)

## 1. Component Architecture (컴포넌트 구조 원칙)

- **Modularization**: 하나의 파일에 모든 코드를 넣지 말고, 컴포넌트는 작게 쪼개서 `src/components/` 하위에 목적별로 배치할 것.
- **TypeScript First**: 모든 컴포넌트는 반드시 TypeScript를 사용하며, 파일 상단에 명시적인 `Props` 인터페이스를 선언할 것.
- **Naming Convention**: 컴포넌트 파일명과 함수명은 PascalCase를 사용할 것 (예: `UserCard.tsx`).

## 2. Styling Rules (스타일링 원칙 - 디자인 변동성 대응)

- **Flexibility**: 디자인이 계속 변경될 수 있으므로, 하드코딩된 값보다는 Tailwind CSS의 유연한 유틸리티 클래스를 적극 활용할 것.
- **Layout Standards**: 화면 배치는 Flexbox와 Grid를 우선적으로 사용하여 반응형 대응이 쉽도록 구조화할 것.
- **Placeholder Style**: 아직 디자인이 나오지 않은 영역이나 미완성 컴포넌트는 임시로 시각적 영역을 잡아주는 `Placeholder` 형태로 처리하고 주석으로 남겨둘 것.

## 3. Data & State Management (데이터 규칙)

- **Mock Data Isolation**: 백엔드 API 연동 전이므로, 컴포넌트 내부에서 임의로 데이터를 만들지 말고 반드시 `src/data/mockData.ts`를 참조해서 렌더링할 것.
- **Props Driven**: UI 컴포넌트는 최대한 '더미 데이터나 상태를 외부에서 주입받는(Props-driven)' 순수 컴포넌트 형태로 짤 것 (나중에 API가 붙을 때 교체하기 쉽도록).
