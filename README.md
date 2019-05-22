# SpaceBattle
Проект за весенний семестр 2019 - SpaceBattle - ООП

Онлайн игра для двух человек в режиме реального времени.

Задача разбита на 3 решения:
  1) Библиотека SpaceBattle.Data
    Содержит общие для клиента и сервера интерфейсы, игровые объекты и логику
  2) Клиент SpaceBattle.Client
  Вся графика и звуки находятся у клиента.
    Цикл работы:
      1. приобразует нажатия клавиш в команды,
      2. отправляет команды на сервер и ожидает ответа,
      3. обрабатывает команды и составляет локальное состояние игры,
      4. начинает отрисовывать локальное состояние,
      5. получает ответ от сервера с актуальным состоянием вычесленным им,
      6. продолжает отрисовку уже актуального состояния,
      7. заканчивает отрисовку goto(1)
  3) Сервер SpaceBattle.Server
  Цикл работы:
      1. получает команды от клиентов
      2. вычисляет новое состояние основываясь на командах от обоих клиентов
      3. отправляет актуальное состояние клиентам goto(1)
