---
title: RunDataMacro Macro Action
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9790faf03ba0f6ea02520abb525c4301ac2181e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480240"
---
# <a name="rundatamacro-macro-action"></a>RunDataMacro Macro Action

**Применимо к**: Access 2013 | Office 2013

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


## <a name="remarks"></a>Замечания

Можно использовать **ЗапускМакросаДанных** в макросы, с именем макросов данных и следующие события макрос: **[После удаления события макрос](after-delete-macro-event.md)**, **[После вставки события макросов](after-insert-macro-event.md)** и **[После обновления макрос события](after-update-macro-event.md)**.

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
