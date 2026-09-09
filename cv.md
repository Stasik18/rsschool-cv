### CV

## Информация об авторе

| Поле                                  | Значение                                                                                                                                                                                     |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Имя                                   | Стас                                                                                                                                                                                         |
| Контакты: почта/telegram/на сервер DS | [rosgard000@gmail.com](mailto:rosgard000@gmail.com) / [`@StasBgtk`](https://t.me/StasBgtk) / Stas @Stasik18                                                                                  |
| О себе                                | Мне 23, Фулл-тайм в учёбе, всегда рад новым знакомствам, служил в армии, учился в БГУИР (не выпустился)                                                                                      |
| Стек/Навыки                           | JavaScript, HTML5, CSS3/SASS/SCSS/CSS nesting, React, Семантическая верстка, Адаптивная верстка, TypeScript, Prisma, REST API, Redux, RTK, RTK Query, Zustand, RHF, Zod, Tanstack Form, Next |

---

Пример хука (переиспользуемый useKeyDown):

```typescript
import { useEffect, useRef } from 'react'

type Key = string

export function useKeyDown(
  key: Key,
  onKeyDown: () => void,
  isActive: boolean = true
): void {
  const onKeyDownRef = useRef(onKeyDown)

  useEffect(() => {
    onKeyDownRef.current = onKeyDown
  }, [onKeyDown])

  useEffect(() => {
    if (!isActive) return

    const handleKeyDown = (event: KeyboardEvent) => {
      if (event.key === key) {
        onKeyDownRef.current()
      }
    }

    document.addEventListener('keydown', handleKeyDown)
    return () => document.removeEventListener('keydown', handleKeyDown)
  }, [key, isActive])
}
```

|             |                                                                                                                                                                                             |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Опыт работы | Без опыта работа, писал всё сам, не много участвовал с стартапах, учился на PREAX, получил там хорошие основы, все технологии изучал сам + вопросы к компитентным друзям, когда были затупы |
| Образование | 11 классов                                                                                                                                                                                  |
| Английский  | мой уровень А2-А1, понимаю с большего доку, сам ни б ни м, НО исправляюсь, как только повляется свободное окошко - отдаю его _АНГЛИЙСКОМУ_                                                  |
|             |                                                                                                                                                                                             |
