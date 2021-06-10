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

Формирование данных определяет столбцы фигурного набора **записей,** связи между сущностями, представленными столбцами, и способ заполнения данных **в Наборе** записей.

Сформированный **набор записей** может состоять из следующих типов столбцов.

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
<td><p>Поля из <strong>recordset,</strong> возвращаемой командой запроса поставщику данных, таблице или ранее сформированным <strong>Набору записей.</strong></p></td>
</tr>
<tr class="even">
<td><p>глава</p></td>
<td><p>Ссылка на другой <strong>Набор записей</strong>, называемый <em>главой</em>. Столбцы глав делают возможным <em></em> определение отношения между <em></em> родителем и ребенком, в <em></em> котором родитель — набор записей, содержащий столбец главы, а ребенок — набор <strong>записей,</strong> представленный главой. <strong></strong></p></td>
</tr>
<tr class="odd">
<td><p>сводка</p></td>
<td><p>Значение столбца выводится путем выполнения <em></em> совокупной функции во всех строках или столбце всех строк детского <strong>recordset.</strong> (См. агрегированные функции в следующей статье, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Агрегированные функции, функция CALC и новое ключевое</a>слово .)</p></td>
</tr>
<tr class="even">
<td><p>вычисляемая экспрессия</p></td>
<td><p>Значение столбца выводится путем вычисления выражения Visual Basic для приложений на столбцах в том же ряду <strong>Recordset.</strong> Выражение является аргументом для функции CALC. (См. вычисляемую экспрессию в следующей статье, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Агрегированные функции, функции CALC,</a> а также новое ключевое слово и <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений Функции.)</a></p></td>
</tr>
<tr class="odd">
<td><p>Новые функции</p></td>
<td><p>Пустые, сфабрикованные поля, которые могут быть заполнены данными в более позднее время. Столбец определяется с помощью ключевого слова NEW. (См. новое ключевое слово в следующей статье, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Агрегированные функции, функция CALC и новое ключевое</a>слово .)</p></td>
</tr>
</tbody>
</table>


Команда фигуры может содержать пункт, указывающий команду запроса основному поставщику данных, который возвращает объект **Recordset.** Синтаксис запроса зависит от требований поставщика данных. Обычно это язык SQL (SQL), хотя ADO не требует использования какого-либо конкретного языка запросов.

Вы можете использовать пункт SQL JOIN, чтобы связать две таблицы; однако иерархический **набор записей может** представлять информацию более эффективно. Каждая строка **наборов записей,** созданных join, повторяет сведения из одной из таблиц. Иерархический **набор записей имеет** только один родительский **набор записей** для каждого из нескольких объектов **recordset** для детей.

Команды формы могут быть выданы **объектами Recordset** или путем установки свойства [CommandText](commandtext-property-ado.md) объекта [Command](command-object-ado.md) и вызова метода [Execute.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)

Команды формы можно вложены. То есть *родительская или* *детская* команда может сама быть другой командой фигуры.

Поставщик фигур всегда возвращает курсор клиента, даже если пользователь указывает расположение **курсора adUseServer.**

Сведения о навигации по иерархическому **набору записей** см. в сайте [Accessing Rows in a Hierarchical Recordset.](accessing-rows-in-a-hierarchical-recordset.md)

Точные сведения о синтаксически правильных командах фигур см. в [разделе Formal Shape Grammar](formal-shape-grammar.md).

## <a name="see-also"></a>См. также

- [Issuing Commands to the Underlying Data Provider](issuing-commands-to-the-underlying-data-provider.md)

