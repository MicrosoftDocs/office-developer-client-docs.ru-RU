---
title: Метод DBEngine. SetOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294199"
---
# <a name="dbenginesetoption-method-dao"></a>Метод DBEngine. SetOption (DAO)

**Область применения**: Access 2013, Office 2013

Временно переопределяет значения ключей ядра СУБД Microsoft Access в реестре Windows (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . SetOption (***параметр***, ***значение***)

*выражение*: выражение, возвращающее объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Константа, описанная в разделе Примечания.</p></td>
</tr>
<tr class="even">
<td><p><em>Value</em></p></td>
<td><p>Обязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Значение, которое необходимо присвоить параметру.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Каждая константа относится к соответствующему разделу реестра в каталоге\_hKey\_\\программное\\обеспечение\\Microsoft\\Office\\12,0 access Engine\\Engines Engine\\(то есть **дбшаредасинкделай** соответствует ключевому программному\_\_\\\\\\\\\\12,0\\\\обеспечению для локального компьютера hKey\\шаредасинкделай и т. д.).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>дбпажетимеаут</strong></p></td>
<td><p>Ключ Пажетимеаут</p></td>
</tr>
<tr class="even">
<td><p><strong>дбшаредасинкделай</strong></p></td>
<td><p>Ключ Шаредасинкделай</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбексклусивеасинкделай</strong></p></td>
<td><p>Ключ Ексклусивеасинкделай</p></td>
</tr>
<tr class="even">
<td><p><strong>дблоккретри</strong></p></td>
<td><p>Ключ Локкретри</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбусеркоммитсинк</strong></p></td>
<td><p>Ключ Усеркоммитсинк</p></td>
</tr>
<tr class="even">
<td><p><strong>дбимплиЦиткоммитсинк</strong></p></td>
<td><p>Ключ ИмплиЦиткоммитсинк</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбмаксбуфферсизе</strong></p></td>
<td><p>Ключ Максбуфферсизе</p></td>
</tr>
<tr class="even">
<td><p><strong>дбмакслокксперфиле</strong></p></td>
<td><p>Ключ MaxLocksPerFile</p></td>
</tr>
<tr class="odd">
<td><p><strong>дблоккделай</strong></p></td>
<td><p>Ключ Локкделай</p></td>
</tr>
<tr class="even">
<td><p><strong>дбрециклелвс</strong></p></td>
<td><p>Ключ Рециклелвс</p></td>
</tr>
<tr class="odd">
<td><p><strong>дбфлуштрансактионтимеаут</strong></p></td>
<td><p>Ключ Флуштрансактионтимеаут</p></td>
</tr>
</tbody>
</table>


Метод **SetOption** используется для переопределения значений реестра во время выполнения. Новые значения, установленные с помощью метода **SetOption** , действуют до тех пор, пока не будут изменены другим вызовом **SetOption** или пока объект **DBEngine** не будет закрыт.

