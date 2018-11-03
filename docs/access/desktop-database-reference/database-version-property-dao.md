---
title: Свойство Database.Version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611fed16c9020b0a6499427af0788bf9ff050c28
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936562"
---
# <a name="databaseversion-property-dao"></a>Свойство Database.Version (DAO)

**Применимо к**: Access 2013, Office 2013

В рабочей области Microsoft Access возвращает vesion ядро базы данных Microsoft Access или Microsoft Jet созданной базе данных. Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Версия

*выражение* Переменная, которая представляет собой объект **базы данных** .

## <a name="remarks"></a>Примечания

Возвращаемое значение — это строка, которое оценивается как номер версии, следующий формат.

- Рабочая область для Microsoft Access представляет номер версии в форме «*major.minor*». Например «3.0». Номер версии продукта состоит из номера версии (3), за период и номер версии (0).

В следующей таблице показаны версии ядра базы данных была включена в различных версиях продуктов Майкрософт.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Компонент Database Engine</p></th>
<th><p>Версия (год выпуска)</p></th>
<th><p>Microsoft Access</p></th>
<th><p>Microsoft Visual Basic</p></th>
<th><p>Microsoft Excel</p></th>
<th><p>Microsoft Visual C++</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>1.0 (1992)</p></td>
<td><p>1.0</p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>1.1 (1993)</p></td>
<td><p>1.1</p></td>
<td><p>3.0</p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>2.0 (1994)</p></td>
<td><p>2.0</p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>2.5 (1995)</p></td>
<td><p>Н/Д</p></td>
<td><p>4.0 (16-разрядная версия)</p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>3.0 (1995)</p></td>
<td><p>"95 (7.0)</p></td>
<td><p>4.0 (32-разрядная версия)</p></td>
<td><p>"95 (7.0)</p></td>
<td><p>4.x</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>3.5 (1996 г.)</p></td>
<td><p>' 97 (8.0)</p></td>
<td><p>5.0</p></td>
<td><p>' 97 (8.0)</p></td>
<td><p>5.0</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>4.0 (2000)</p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Ядро СУБД Microsoft Access</p></td>
<td><p>12.0 (2007)</p></td>
<td><p>2007</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

