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

Формирование данных определяет столбцы в виде наборов записей, связи между сущностями, представленные столбцы, и способ заполнения набором **записей** данными.

Набор **записей в виде фигуры** может состоять из следующих типов столбцов.

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
<td><p>Поля из <strong>recordset,</strong> возвращаемой командой запроса поставщику данных, таблице или ранее сформированном <strong>набору записей.</strong></p></td>
</tr>
<tr class="even">
<td><p>chapter</p></td>
<td><p>Ссылка на другой <strong>набор записей,</strong>называемый <em>главой.</em> Столбцы главы по возможности определяют отношение <em></em> <strong></strong> <strong></strong> "родитель-потомок", где родительским <em></em> является набор записей, содержащий столбец главы, а потомок — набор записей, представленный главой. <em></em></p></td>
</tr>
<tr class="odd">
<td><p>aggregate</p></td>
<td><p>Значение столбца является производным от <em></em> выполнения агрегированной функции во всех строках или столбцах всех строк в наборе <strong>записей.</strong> (См. "Агрегатные функции" в следующем разделе, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">"Агрегатные функции", "CalC Function" и "НОВОЕ</a>ключевое слово".</p></td>
</tr>
<tr class="even">
<td><p>вычисляемая выражение</p></td>
<td><p>Значение столбца является производным от вычисления Visual Basic для приложений в столбцах в той же строке <strong>recordset</strong>. Выражение является аргументом функции CALC. (См. "Вычисляемая выражение" в следующем разделе, "Агрегатные функции", <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">"CalC Function",</a> "Ключевое слово NEW" <a href="visual-basic-for-applications-functions.md">и "Visual Basic для приложений Функции".)</a></p></td>
</tr>
<tr class="odd">
<td><p>Новые функции</p></td>
<td><p>Пустые, сфабрикованные поля, которые могут быть заполнены данными позже. Столбец определяется ключевым словом NEW. (См. ключевое слово NEW в следующем разделе: <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">"Агрегатные функции", "CalC Function" и "НОВОЕ ключевое слово".)</a></p></td>
</tr>
</tbody>
</table>


Команда фигуры может содержать предложение, определяющие команду запроса для поставщика данных, который возвращает объект **Recordset.** Синтаксис запроса зависит от требований поставщика данных. Обычно это язык SQL (SQL), хотя ADO не требует использования какого-либо конкретного языка запросов.

Вы можете использовать предложение SQL JOIN, чтобы связать две таблицы; однако иерархический набор **записей может** представлять информацию более эффективно. Каждая строка наборов **записей,** созданных с помощью JOIN, повторяет сведения из одной из таблиц. Иерархический набор **записей** имеет только один родительский набор **записей** для каждого из нескольких объектов **recordset.**

Команды shape могут быть выданы объектами **Recordset** или путем установки свойства [CommandText](commandtext-property-ado.md) объекта [Command](command-object-ado.md) и вызова метода [Execute.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)

Команды фигуры могут быть вложенными. То есть *родительская* или  родительская команда может быть другой командой фигуры.

Поставщик фигур всегда возвращает клиентский курсор, даже если пользователь указывает расположение курсора **adUseServer.**

Сведения о навигации по иерархическому набору **записей** см. в подсети "Доступ к [строкам в иерархическом наборе записей".](accessing-rows-in-a-hierarchical-recordset.md)

Точные сведения о синтаксически правильных командах фигур см. в поддомене ["Грамматика формальной фигуры".](formal-shape-grammar.md)

## <a name="see-also"></a>См. также

- [Issuing Commands to the Underlying Data Provider](issuing-commands-to-the-underlying-data-provider.md)

