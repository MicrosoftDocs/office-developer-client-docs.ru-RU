---
title: Свойство QueryDef. Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300947"
---
# <a name="querydeftype-property-dao"></a>Свойство QueryDef. Type (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает операционный тип или тип данных объекта. **Целое число**, доступное только для чтения.

## <a name="syntax"></a>Синтаксис

*Expression* . Тип

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Замечания

В приведенной ниже таблице представлены возможные параметры и возвращаемые значения для объекта **QueryDef** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Тип запроса</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Дбкактион</strong></p></td>
<td><p>Действие</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбкаппенд</strong></p></td>
<td><p>Error</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбккомпаунд</strong></p></td>
<td><p>Состав</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбккросстаб</strong></p></td>
<td><p>Перекрестный</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбкддл</strong></p></td>
<td><p>Определение данных</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбкделете</strong></p></td>
<td><p>Delete</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбкмакетабле</strong></p></td>
<td><p>Создание таблицы</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбкпроцедуре</strong></p></td>
<td><p>Процедура (только для рабочих областей ODBCDirect)</p><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбкселект</strong></p></td>
<td><p>Выбор</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбксетоператион</strong></p></td>
<td><p>Union</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбксптбулк</strong></p></td>
<td><p>Используется с <strong>дбксклпасссраугх</strong> , чтобы указать запрос, который не возвращает записи (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбксклпасссраугх</strong></p></td>
<td><p>Сквозная передача (только для рабочих областей Microsoft Access)</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбкупдате</strong></p></td>
<td><p>Update</p></td>
</tr>
</tbody>
</table>


При добавлении нового **[поля](field-object-dao.md)**, **[параметра](parameter-object-dao.md)** или объекта **[Свойства](property-object-dao.md)** в коллекцию объекта **[index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** или **[tabledef](tabledef-object-dao.md)** возникает ошибка, если базовая база данных не поддерживается. тип данных, указанный для нового объекта.

