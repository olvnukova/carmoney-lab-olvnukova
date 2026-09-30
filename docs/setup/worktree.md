# Список воркtrees репозитория

Вывод списка рабочих копий (worktrees) проекта с их HEAD-коммитами и ветками:

```text
C:/Users/ol.vnukova/Desktop/обучение ИИ/carmoney-lab-olvnukova                                             4680a84 [d1/1.2.1-1.2.3-olvnukova]
C:/Users/ol.vnukova/Desktop/обучение ИИ/carmoney-lab-olvnukova/.kilo/worktrees/1-2-2                       4680a84 [1-2-2]
C:/Users/ol.vnukova/Desktop/обучение ИИ/carmoney-lab-olvnukova/.kilo/worktrees/1-2-3-olvnukova             4680a84 [1-2-3-olvnukova]
C:/Users/ol.vnukova/Desktop/обучение ИИ/carmoney-lab-olvnukova/.kilo/worktrees/celestial-echium            b3c17d6 [celestial-echium]
C:/Users/ol.vnukova/Desktop/обучение ИИ/carmoney-lab-olvnukova/.kilo/worktrees/lush-end                    4680a84 (detached HEAD)
```

Тесты в tests/Unit/:

VinValidatorTest.php — проверяет VinValidator::isValid(): длина 17, регистр, запрещённые буквы I/O/Q, спецсимволы, пустая строка.
LtvCalculatorTest.php — проверяет LtvCalculator::calculate(): LTV = amount / marketValue (50%, 33.33%, 120%) и InvalidArgumentException при market_value = 0 или amount ≤ 0.
DecisionEngineTest.php — проверяет DecisionEngine::decide(): пороги approve/review/reject по LTV на границах и внутри зон (28.5, 45.0, 72.3, 85.0, 85.01, 120.0).
AssessmentServiceTest.php — проверяет сквозной сценарий AssessmentService::assess() для трёх исходов: approve с approved_limit = requested_amount, review и reject с лимитом 0 (и что в payload пробрасывается vehicle_age).
ApplicationValidatorTest.php — проверяет ApplicationValidator: принимает валидную заявку и нормализует VIN в верхний регистр, отклоняет year из будущего, requested_amount ниже минимума, и собирает все ошибки сразу по полям vin/market_value/term_months.

Где я сейчас: папка C:\Users\ol.vnukova\Desktop\обучение ИИ\carmoney-lab-olvnukova\.kilo\worktrees\1-2-3-olvnukova, ветка определить не удалось — команда git branch --show-current заблокирована политикой прав (git * → deny, без явного разрешения для branch --show-current). Можно посмотреть через git branch --list или git rev-parse --abbrev-ref HEAD, если нужно.
