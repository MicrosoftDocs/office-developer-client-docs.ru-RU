---
title: Общие сведения о командах Shape
TOCTitle: Shape commands in general
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 399836158084f07b30b06a9fb099da74527d0cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308654"
---
# <a name="shape-commands-in-general"></a>Общие сведения о командах Shape

**Область применения**: Access 2013, Office 2013

При создании данных определяются столбцы объекта **Recordset**в форме, отношения между сущностями, представленные столбцами, и способ заполнения объекта **Recordset** данными.

Объект **Recordset** в форме может состоять из следующих типов столбцов.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип столбца</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>data</p></td>
<td><p>Поля из <strong>набора записей</strong> , возвращенные командой запроса к поставщику данных, таблице или ранее фигурному <strong>набору записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p>части</p></td>
<td><p>Ссылка на другой <strong>набор записей</strong>, называемый <em>главой</em>. В столбцах главы можно определить связь типа " <em>родители-потомки</em> ", в которой <em>родитель</em> — это объект <strong>Recordset</strong> , содержащий столбец Chapter, а <em>дочерний</em> элемент — это <strong>набор записей</strong> , представленный главой.</p></td>
</tr>
<tr class="odd">
<td><p>объединит</p></td>
<td><p>Значение столбца извлекается путем выполнения <em>статистической функции</em> для всех строк или столбцов всех строк дочернего объекта <strong>Recordset</strong>. (См. статистические функции в следующих разделах, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">статистические функции, функция calc и ключевое слово New</a>.)</p></td>
</tr>
<tr class="even">
<td><p>Вычисляемое выражение</p></td>
<td><p>Значение столбца извлекается путем вычисления выражения Visual Basic для приложений для столбцов в той же строке <strong>набора записей</strong>. Выражение является аргументом функции CALC. (См. вычисленное выражение в следующих разделах, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">статистические функции, функция calc и ключевое слово New</a> и в <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений</a>.)</p></td>
</tr>
<tr class="odd">
<td><p>Новые функции</p></td>
<td><p>Пустые, заполненные поля, которые могут быть заполнены данными позже. Столбец определяется с помощью ключевого слова NEW. (См. ключевое слово NEW в следующих разделах, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">статистические функции, функция calc и ключевое слово New</a>.)</p></td>
</tr>
</tbody>
</table>


Команда Shape может содержать предложение, задающее команду запроса для базового поставщика данных, который будет возвращать объект **Recordset** . Синтаксис запроса зависит от требований базового поставщика данных. Как правило, это будет язык структурированных запросов (SQL), хотя для ADO не требуется использование какого-либо конкретного языка запросов.

Вы можете использовать предложение JOIN SQL, чтобы связать две таблицы; Однако иерархический **набор записей** может представлять данные более эффективно. Каждая строка **набора записей** , созданная при объединении, повторяет данные из одной из таблиц. Иерархический **набор** записей имеет только один родительский **набор записей** для каждого из нескольких дочерних объектов **Recordset** .

Команды Shape могут выдаваться объектами **Recordset** или путем установки свойства [CommandText](commandtext-property-ado.md) объекта [Command](command-object-ado.md) , а затем вызова метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .

Команды фигур могут быть вложенными. То есть *родительская команда* или *дочерняя команда* может быть другой командой Shape.

Поставщик фигур всегда возвращает клиентский курсор, даже если пользователь указывает расположение курсора **адусесервер**.

Сведения о переходе на иерархический **набор записей**содержатся [в разделе доступ к строкам в иерархическом наборе записей](accessing-rows-in-a-hierarchical-recordset.md).

Точные сведения о синтаксически правильных командах формы можно узнать в статье [формальное описание грамматики фигур](formal-shape-grammar.md).

## <a name="see-also"></a>См. также

- [Issuing Commands to the Underlying Data Provider](issuing-commands-to-the-underlying-data-provider.md)

