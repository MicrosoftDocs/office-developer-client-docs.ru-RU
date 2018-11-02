---
title: Макрокоманда RunDataMacro
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c1d540b909a2ac5741719470f5632e34205806ff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927986"
---
# <a name="rundatamacro-macro-action"></a>Макрокоманда RunDataMacro

**Применимо к**: Access 2013, Office 2013

**ЗапускМакросаДанных** можно использовать для запуска именованный макрос данных.

## <a name="setting"></a>Параметр

**ЗапускМакросаДанных** использует следующий аргумент.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Имя макроса данных для запуска.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Можно использовать **ЗапускМакросаДанных** в макросы, с именем макросов данных и следующие события макрос: **[после удаления событий макроса](after-delete-macro-event.md)**, **[события после вставки макросов](after-insert-macro-event.md)** и **[событие макрос после обновления](after-update-macro-event.md)**.

Имя макроса данных необходимо включить таблицу, к которой он подключен (например, **Comments.AddComment**, не только **AddComment**).

При выборе макрос данных, которая должна работать в конструктор макросов Access определяет необходимость в макрос данных параметров. Если макрос данных требуются параметры, текстовых полей отображаются для ввода в аргументах.

При запуске макроса, содержащего **ЗапускМакросаДанных** и достигает **ЗапускМакросаДанных** , Access запускает макрос называемое данных. По завершении макрос называемое данных Access возвращает исходное макрос и выполняется следующее действие.

## <a name="example"></a>Пример

Следующем примере показано, как передать параметр именованный макрос данных. Макрос данных dmGetCurrentServiceRequest таблицы tblServiceRequests вызывается с помощью ЗапускМакросаДанных. По завершении dmGetCurrentServiceRequest переменной CurrentServiceRequest возвращаются записи макроса данных в текстовом поле txtCurrentSR формы.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
