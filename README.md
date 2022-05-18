# code-generation
Can we generate sourcecode for algorithms automatically?

# a star algorithm

A star algorithm is kind of intelligent, it uses a cost function and a heuristic.

What is the cost function for lines of code? That get nearer to the output values?

Project the output data or desired result onto a multidimensional surface.

We move the inputs the lines of code to change the output movement.

But what of ordering of code?

One line of code changes the possibilities for the next line of code.

The neighbours of the current code are the possibilities of the current line of code.

What if the reverse mapping? From desired output to source data.

How do you move toward an answer with the intermediately generated code?

Transform the shape of the input data to the destination data

Join on all the fields of objects

Rule recognition if the pattern is the same for all joins.

If not there is some other property.

Could have a set of primitives: create new object, create recursive call, loop

Then when the structure of the input data matches output data you need to find the conditions to get to the output structure.

The distance function needs to compare the input data structure to the candidate data structure.

But without brute forcing how do you search an opportunity in depth. You need intelligence to go in a direction

I thought of an idea to use a* algorithm to "walk" toward a solution that solves a programming problem. Each neighbour can be a weighted list of programming tasks such as if statement, for each, assignment, recursive call. How do you map example data structures transformations to code that fulfils the changes to the data structure? You need a cost function that decreases when the output gets nearer to the solution. What does the cost function for code solving a problem look similar to?

If you project the desired code variables onto a multidimensional space and with a time dimension, where each variable has a assignment algebra you can imagine the input code causing movements to the output algebra for each variable 

How do you measure that a solution gets nearer to the solution when you haven't planned what you could do

It should be a multidimensional walk toward a solution that solves the programming problem.

I want to generate the btree algorithm and other algorithms with this approach

I should provide example inputs to output mappings and join the Data between the input and output and try recalculate the processing steps to go from one to the other but I am having problems deciding what the cost function looks like.

If you project the desired code variables onto a multidimensional space and with a time dimension, where each variable has a assignment algebra you can imagine the input code causing movements to the output algebra for each variable 

How do you measure that a solution gets nearer to the solution when you haven't planned what you could do

It should be a multidimensional walk toward a solution that solves the programming problem.

I want to generate the btree algorithm and other algorithms with this approach

I should provide example inputs to output mappings and join the Data between the input and output and try recalculate the processing steps to go from one to the other but I am having problems deciding what the cost function looks like.

.:en
We can scan the output structure and generate facts of each relationship of data.

We can compare where the data moved through based on a path traversal of source data to destination data. Generate a patch.

This has a pointer to this object to this piece of data.

Input data

Node1 is root

Node1 children node2

Node1 children node3

Example 1

Insert a node node4

Desired Output data

Node1 is root

Node1 children node2

Node1 children node3

Node1 children node4

Patch

Node1 inserted into node1 children

Why node1? Theorise.

Node1 is root

Run operators against node1, node4

Len(node1.children) <= Maxsize


Example 2

Node split - insert node5

Input data

Root node is node1

Node1 children node2

Node1 children node3

Node1 children node4

Desired target data

Root node is node3

Node3 children node1

Node3 children node2

Node3 children node4

Node4 children node5

This represents a node split as each node can only have 3 items inside it.

How do we learn the rule that a node can only have 3 nodes?

Insert a constant into the system of facts

MaxSize is 3
Insert operators in system
Len(node.children)
MaxSize
== Equal to
>= Greater than or equal to
<= Less than or equal to
> Greater than
< Less than

Run every permutation of each operator to decide to do patch command steps.

Patch instructions
Node1 is no longer root node
Node3 is root node
Node2 children is node1
Remove node4 from node1
Why was node4 removed from node1
Why was node4 added to node3

Theorise. What fact was true.
Compare node1 properties to node4
Eventually....
Len(node1.children) == MaxSize
Add node4 to node3
Why?
Theorise. What fact is true
Node4 >= Node3 true
Does >= hold for all examples? Or is it more complicated
Twist operation. One goes down, one goes up and going down joins one going down.
Root = A
Node1 is A
New root = B

Twist operation is -
Root = B
B.children = A


And see where the data moves. We need to generate the steps that deterministically creates the same structure with the same data in the right places.

There shall be patterns. So there is usually a property in the object that is compared against to do a btree split.

So there is at most one field or a comparison that determines the destination of the object in the btree.

I thought we can randomly generate condition statements for each input object.

Walk the patch and insert condition objects.

It's a graph transformation problem
.:LT
Galime nuskaityti išvesties struktūrą ir generuoti kiekvieno duomenų ryšio faktus.

Galime palyginti, kur buvo perkelti duomenys, remdamiesi šaltinio duomenų perėjimu iki paskirties duomenų. Sugeneruokite pleistrą.

Tai turi žymeklį į šį objektą į šią duomenų dalį.

Įvesties duomenys

1 mazgas yra šakninis

Mazgas1 vaikų mazgas2

Mazgas1 vaikų mazgas3

1 pavyzdys

Įdėkite mazgo mazgą4

Norimi išvesties duomenys

1 mazgas yra šakninis

Mazgas1 vaikų mazgas2

Mazgas1 vaikų mazgas3

Mazgas1 vaikų mazgas4

Pleistras

1 mazgas įterptas į mazgo 1 antrinius elementus

Kodėl mazgas1? Teorizuoti.

1 mazgas yra šakninis

Vykdykite operatorius nuo node1, node4

Len(mazgas1.vaikai) &lt;= Didžiausias dydis


2 pavyzdys

Mazgo padalijimas – įterpkite mazgą5

Įvesties duomenys

Šakninis mazgas yra mazgas1

Mazgas1 vaikų mazgas2

Mazgas1 vaikų mazgas3

Mazgas1 vaikų mazgas4

Norimi tiksliniai duomenys

Šakninis mazgas yra node3

Node3 vaikų mazgas1

Node3 vaikų mazgas2

Node3 vaikų mazgas4

Mazgas4 vaikai mazgas5

Tai reiškia mazgo padalijimą, nes kiekviename mazge gali būti tik 3 elementai.

Kaip išmokti taisyklę, kad mazgas gali turėti tik 3 mazgus?

Į faktų sistemą įterpkite konstantą

Maksimalus dydis yra 3
Įdėkite operatorius į sistemą
Len(mazgas.vaikai)
Maksimalus dydis
== Lygus
&gt;= Didesnis nei arba lygus
&lt;= Mažiau nei arba lygus
&gt; Didesnis nei
&lt; Mažiau nei

Vykdykite kiekvieną kiekvieno operatoriaus permutaciją, kad nuspręstumėte atlikti pataisos komandos veiksmus.

Pleistro instrukcijos
1 mazgas nebėra šakninis mazgas
Node3 yra šakninis mazgas
Node2 vaikai yra mazgas1
Pašalinkite 4 mazgą iš 1 mazgo
Kodėl mazgas4 buvo pašalintas iš mazgo1
Kodėl mazgas4 buvo pridėtas prie mazgo3

Teorizuoti. Koks faktas buvo tiesa.
Palyginkite 1 mazgo savybes su 4 mazgu
Pagaliau....
Len(mazgas1.vaikai) == Didžiausias dydis
Pridėkite mazgą4 prie mazgo3
Kodėl?
Teorizuoti. Koks faktas yra tiesa
4 mazgas &gt;= 3 mazgas tiesa
Ar &gt;= tinka visiems pavyzdžiams? Arba tai sudėtingiau
Sukimo operacija. Vienas leidžiasi žemyn, vienas kyla aukštyn ir leidžiasi žemyn, o vienas leidžiasi žemyn.
Šaknis = A
1 mazgas yra A
Nauja šaknis = B

Sukimo operacija yra -
Šaknis = B
B.vaikai = A


Ir pažiūrėkite, kur juda duomenys. Turime sugeneruoti veiksmus, kurie deterministiškai sukuria tą pačią struktūrą su tais pačiais duomenimis tinkamose vietose.

Turi būti modeliai. Taigi paprastai objekte yra savybė, su kuria lyginamas bmedžio padalijimas.

Taigi yra daugiausia vienas laukas arba palyginimas, kuris nustato objekto paskirties vietą btree.

Maniau, kad galime atsitiktinai generuoti sąlygų sakinius kiekvienam įvesties objektui.

Eikite į pleistrą ir įdėkite sąlyginius objektus.

Tai grafiko transformacijos problema

.:CN
我们可以扫描输出结构并生成每个数据关系的事实。

我们可以根据源数据到目标数据的路径遍历来比较数据移动的位置。生成补丁。

这有一个指向这个对象的指针，指向这条数据。

输入数据

Node1 是根

节点 1 子节点 2

节点 1 子节点 3

示例 1

插入一个节点node4

所需的输出数据

Node1 是根

节点 1 子节点 2

节点 1 子节点 3

节点 1 子节点 4

修补

Node1 插入到 node1 子节点中

为什么是节点1？理论。

Node1 是根

针对 node1、node4 运行算子

Len(node1.children) &lt;= Maxsize


示例 2

节点拆分 - 插入 node5

输入数据

根节点是node1

节点 1 子节点 2

节点 1 子节点 3

节点 1 子节点 4

所需的目标数据

根节点是node3

节点 3 子节点 1

节点 3 子节点 2

节点 3 子节点 4

节点 4 子节点 5

这表示一个节点拆分，因为每个节点里面只能有 3 个项目。

我们如何学习一个节点只能有 3 个节点的规则？

在事实系统中插入一个常数

最大尺寸为 3
在系统中插入运算符
Len(node.children)
最大尺寸
== 等于
&gt;= 大于或等于
&lt;= 小于或等于
&gt; 大于
&lt; 小于

运行每个运算符的每个排列以决定执行补丁命令步骤。

补丁说明
Node1 不再是根节点
Node3 是根节点
Node2 的子节点是 node1
从 node1 中删除 node4
为什么从 node1 中删除 node4
为什么node4被添加到node3

理论。什么事实是真的。
将 node1 属性与 node4 进行比较
最终....
Len(node1.children) == MaxSize
将node4添加到node3
为什么？
理论。什么事实是真的
节点 4 &gt;= 节点 3 真
&gt;= 是否适用于所有示例？还是更复杂
扭动操作。一个下降，一个上升，下降连接一个下降。
根 = A
节点 1 是 A
新根 = B

扭曲操作是 -
根 = B
B.儿童 = A


并查看数据移动到哪里。我们需要生成确定性地在正确位置创建具有相同数据的相同结构的步骤。

应该有图案。因此，对象中通常有一个属性可以进行比较以进行 btree 拆分。

所以最多有一个字段或一个比较来确定对象在 btree 中的目的地。

我认为我们可以为每个输入对象随机生成条件语句。

走补丁并插入条件对象。

这是一个图形转换问题

.:RU
Мы можем сканировать структуру вывода и генерировать факты каждой взаимосвязи данных.

Мы можем сравнить, куда переместились данные, на основе прохождения пути от исходных данных до данных назначения. Создайте патч.

У этого есть указатель на этот объект для этого фрагмента данных.

Входные данные

Node1 является корневым

Узел 1 дочерний узел 2

Узел 1 дочерний узел 3

Пример 1

Вставить узел node4

Желаемые выходные данные

Node1 является корневым

Узел 1 дочерний узел 2

Узел 1 дочерний узел 3

Узел 1 дочерний узел 4

Пластырь

Node1 вставлен в дочерние узлы node1

Почему узел1? Теория.

Node1 является корневым

Выполнить операторы против node1, node4

Len(node1.children) &lt;= Максимальный размер


Пример 2

Разделение узла — вставка node5

Входные данные

Корневой узел — node1

Узел 1 дочерний узел 2

Узел 1 дочерний узел 3

Узел 1 дочерний узел 4

Желаемые целевые данные

Корневой узел — node3

Node3 дочерний node1

Node3 потомки node2

Node3 потомки node4

Node4 потомки node5

Это представляет собой разделение узла, поскольку внутри каждого узла может быть только 3 элемента.

Как узнать правило, согласно которому узел может иметь только 3 узла?

Вставить константу в систему фактов

Максимальный размер равен 3
Вставить операторов в систему
Лен(узел.дети)
Максимальный размер
== равно
&gt;= больше или равно
&lt;= Меньше или равно
&gt; Больше, чем
&lt; Менее чем

Запустите каждую перестановку каждого оператора, чтобы принять решение о выполнении шагов команды исправления.

Инструкции по патчу
Node1 больше не является корневым узлом
Node3 является корневым узлом
Дочерний узел Node2 - это node1
Удалить node4 из node1
Почему node4 был удален из node1
Почему node4 был добавлен к node3

Теория. Какой факт был правдой.
Сравните свойства node1 со свойствами node4
В конце концов....
Len(node1.children) == MaxSize
Добавить node4 к node3
Почему?
Теория. Какой факт является правдой
Узел 4 &gt;= Узел 3 истина
Выполняется ли &gt;= для всех примеров? Или это сложнее
Операция скручивания. Один идет вниз, один идет вверх, а спуск соединяется с одним спуском.
Корень = А
Узел 1 — это А
Новый корень = B

Операция скручивания -
Корень = В
Б.дети = А


И посмотреть, куда перемещаются данные. Нам нужно сгенерировать шаги, которые детерминировано создают ту же структуру с теми же данными в нужных местах.

Должны быть узоры. Таким образом, обычно в объекте есть свойство, которое сравнивается для разделения btree.

Таким образом, имеется не более одного поля или сравнения, определяющего место назначения объекта в b-дереве.

Я думал, что мы можем случайным образом генерировать операторы условий для каждого входного объекта.

Пройдите патч и вставьте объекты состояния.

Это задача преобразования графа

.:JA
出力構造をスキャンして、データの各関係のファクトを生成できます。

ソースデータから宛先データへのパストラバーサルに基づいて、データが移動した場所を比較できます。パッチを生成します。

これには、このデータへのこのオブジェクトへのポインタがあります。

入力データ

Node1はルートです

Node1の子node2

Node1の子node3

例1

ノードnode4を挿入します

必要な出力データ

Node1はルートです

Node1の子node2

Node1の子node3

Node1の子node4

パッチ

node1がnode1の子に挿入されました

なぜnode1？理論。

Node1はルートです

node1、node4に対して演算子を実行します

Len（node1.children）&lt;=最大サイズ


例2

ノード分割-ノード5を挿入

入力データ

ルートノードはnode1です

Node1の子node2

Node1の子node3

Node1の子node4

必要なターゲットデータ

ルートノードはnode3です

Node3の子node1

Node3の子node2

Node3の子node4

Node4の子node5

これは、各ノード内に3つのアイテムしか含めることができないため、ノードの分割を表します。

1つのノードが持つことができるノードは3つだけであるというルールをどのように学習しますか？

ファクトのシステムに定数を挿入します

MaxSizeは3です
システムに演算子を挿入します
Len（node.children）
MaxSize
==等しい
&gt;=以上
&lt;=以下
&gt;より大きい
&lt;未満

各演算子のすべての順列を実行して、パッチコマンドステップを実行することを決定します。

パッチの説明
Node1はルートノードではなくなりました
Node3はルートノードです
Node2の子はnode1です
node1からnode4を削除します
node4がnode1から削除されたのはなぜですか
node4がnode3に追加されたのはなぜですか

理論。どんな事実が真実でしたか。
node1のプロパティをnode4と比較します
最終的....
Len（node1.children）== MaxSize
node4をnode3に追加します
なんで？
理論。本当の事実
Node4&gt; = Node3 true
&gt; =はすべての例に当てはまりますか？それとももっと複雑ですか
ツイスト操作。 1つは下降し、1つは上昇し、1つは下降し、もう1つは下降します。
ルート=A
Node1はAです
新しいルート=B

ツイスト操作は-
ルート=B
B.children = A


そして、データがどこに移動するかを確認します。適切な場所に同じデータを使用して同じ構造を決定論的に作成するステップを生成する必要があります。

パターンがあるはずです。したがって、通常、btree分割を行うために比較されるプロパティがオブジェクトにあります。

したがって、btree内のオブジェクトの宛先を決定するフィールドまたは比較は最大で1つです。

入力オブジェクトごとに条件ステートメントをランダムに生成できると思いました。

パッチをウォークし、条件オブジェクトを挿入します。

グラフ変換の問題です
