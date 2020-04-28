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
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306813"
---
# <a name="rundatamacro-macro-action"></a>Макрокоманда RunDataMacro

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **RunDataMacro** для запуска именованного макроса данных.

## <a name="setting"></a>Параметр

Действие **RunDataMacro** имеет следующий аргумент.

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
<td><p>Имя запускаемого макроса данных.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вы можете использовать макрокоманду **RunDataMacro** в макросах, именованных макросах данных и следующих макросах: **[после удаления макроса](after-delete-macro-event.md)** **[после вставки](after-insert-macro-event.md)** макроса и **[после обновления макроса](after-update-macro-event.md)**.

Имя макроса данных должно включать таблицу, к которой она подключена (например, **Comments. аддкоммент**, а не только **аддкоммент**).

При выборе макроса данных, который требуется запустить в конструкторе макросов, Access определяет, требуются ли для макроса данных параметры. Если макрос данных требует параметров, отображаются текстовые поля, в которых можно вводить аргументы.

При запуске макроса, содержащего действие **RunDataMacro** , и достижении действия **RunDataMacro** , Access запускает макрос данных, который вызывается. После завершения вызываемого макроса данных Access возвращается к исходному макросу и выполняет следующее действие.

## <a name="example"></a>Пример

В приведенном ниже примере показано, как передать параметр в именованный макрос данных. Макрос данных Дмжеткуррентсервицерекуест таблицы Тблсервицерекуестс вызывается с помощью действия RunDataMacro. После завершения Дмжеткуррентсервицерекуест переменная Куррентсервицерекуест, возвращаемая макросом данных, записывается в текстовое поле Тксткуррентср.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
