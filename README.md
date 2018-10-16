# Модель апельсинового дерева

## Введение
Фермер Федор заинтересован в создании модели своей апельсиновой фермы. Как доказательство своей концепции, он надеется смоделировать одно апельсиновое дерево и его ежегодное производство на протяжении всей его жизни. Федор начал работать над самой программой, но успех его фермы оставил ему совсем мало времени для развития. В результате нас наняли для того, чтобы сделать приложение для него.

В этой задаче мы будем разрабатывать собственный класс: `OrangeTree`. Мы разработаем его интерфейс и все его поведенческие требования к спецификациям, предоставленным Федором. Как только модель будет завершена, мы создадим скрипт, который будет моделировать производство дерева.


## Releases
### Pre-release: обзор предоставленного кода
Как уже упоминалось во *Введении*, Федор уже начал разрабатывать это приложение. Он создал полный и проверенный класс «Orange», который мы будем использовать – на нашем апельсиновом дереве будут расти апельсины. Федор только начал заниматься созданием класса «OrangeTree». Он изложил несколько методов и написал несколько комментариев о том, что они должны делать; он также предоставил некоторый код скелета для тестирования апельсинового дерева. И, наконец, он написал некоторые сценарии, которые будут запускаться (`runner.js`), когда мы хотим видеть производство дерева на протяжении его жизни. Просмотрите код, чтобы понять суть того, что планировал сделать Федор.


### Release 0: Модель апельсинового дерева
Здесь представлены некоторые детали, которые Федор предоставил для того, чтобы мы понимали его видение того, какое поведение от модели апельсинового дерева он ожидал. Помните о том, что это ранняя версия приложения, подтверждающая лишь основную концепцию, поэтому мы не будем волноваться о моделировании таких вещей, как влияние температуры на производство. Мы строим самую базовую модель.

Каждая из деталей, написанных Федором, должна быть переведена в тесты, чтобы мы могли убедиться, что наша модель соответствует ожиданиям. В скобках Федор предоставил метод, которым он намеревался сопоставить эти детали. Наш класс может спокойно включать в себя и другие методы, помимо указанных.

- Дерево должно быть определенного возраста, который мы должны проверить (`.age`).
- Дерево должно иметь высоту, которую мы должны проверить (`.height`).
- Каждый вегетационный период (`.passGrowingSeason`) 
  - Любые неубранные апельсины из предыдущего сезона должны упасть.
  - Дереву должен быть один год.
  - Дерево должно расти на 2,5 фута в высоту до тех пор, пока оно не достигнет максимальной высоты - скажем, 25 футов.
  - Дерево должно приносить плоды, если оно зрелое (то есть не менее шести лет) - скажем, от 100 до 300 апельсинов.
- Мы должны проверить, достаточно ли дерево зрелое для производства фруктов (`.isMature`).
- Дерево должно погибнуть в возрасте 100 лет, и мы должны суметь проверить, погибло ли ​​оно (`isDead`).
- Мы должны проверить, есть ли на дереве апельсины (`hasOranges`).
- Мы должны выбрать апельсин с дерева (`.pickAnOrange`) или спровоцировать вывод ошибки в случае, если мы попытаемся взять апельсин, а на дереве их нет.


### Release 1: Завершите скрипт моделирования производства

Теперь у нас есть полностью проверенные и функциональные классы «Orange» и «OrangeTree». Теперь пришло время использовать эти модели в приложении. Помните, что Федор хочет видеть ежегодное производство апельсинового дерева в течение всей его жизни.

Нам нужно заполнить файл `runner.js`. В частности, нам нужно вычислить локальную переменную `averageOrangeDiameter`, которая говорит нам о том, сколько в среднем составляет урожай апельсинов. Как только это будет сделано, установите ожидаемое значение для вывода сценария. Как только у нас появятся наши ожидания, запустите скрипт, чтобы увидеть наши классы в действии.

Оправдал ли сценарий наши ожидания? Если нет, каковы ошибки или неожиданное поведение? Понимаем ли мы, почему так происходило? Напишите тесты, чтобы «засечь» любые ошибки в нашем классе «OrangeTree». Нам также может потребоваться обновление существующих тестов в том случае, если мы обнаружим, что мы считаем неверную вещь верной или делаем что-то неправильно. Продолжайте до тех пор, пока скрипт не будет работать правильно.

## Заключение
Мы смоделировали объект из реального мира в соответствии с потребностями нашего приложения. Впредь мы будем делать такие вещи часто. Нам приходилось принимать решения относительно внутреннего состояния нашего дерева (то есть, какие переменные ему нужны). У каждого дерева следует отслеживать возраст, высоту и количество апельсинов. И мы можем использовать эти показатели для того, чтобы быть способными рассчитать больше показателей, касающихся дерева: достаточно ли оно взрослое для того, чтобы приносить плоды, погибло ли оно, и растут ли на нем апельсины?
