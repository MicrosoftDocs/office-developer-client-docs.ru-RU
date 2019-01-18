---
title: Макрокоманда SetReturnVar
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708160"
---
# <a name="setreturnvar-macro-action"></a>Макрокоманда SetReturnVar

**Применимо к**: Access 2013, Office 2013

Действие **SetReturnVar** создает возвращаемое переменной и устанавливает для определенного значения.

> [!NOTE]
> **SetReturnVar** действие доступно только в макросов данных.

## <a name="setting"></a>Setting

Действие **SetReturnVar** состоит из следующих аргументов.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Да</p></td>
<td><p>Строка, задающая имя переменной.</p></td>
</tr>
<tr class="even">
<td><p>Выражение</p></td>
<td><p>Да</p></td>
<td><p>Выражение, которое будет использоваться для задания значения для этой временной переменной. Перед выражением знак равенства (=). Можно нажмите кнопку <strong>Построить</strong> для задания аргумента с помощью <strong>Построителя выражений</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Действие **SetReturnVar** используется для создания **ReturnVar**, которая является переменной, которая может использоваться макросы, которые могут вызывать макрос данных с помощью **ЗапускМакросаДанных** .

После создания **ReturnVar** с **SetReturnVar** действие вызова макроса можно использовать в выражении. Например при создании **ReturnVar** с именем **UpdateSuccess**, можно использовать переменную, используя следующий синтаксис:

```vb
    =[ReturnVars]![UpdateSuccess]
```

Действие **SetReturnVar** можно использовать только в именованных макросов данных. Он недоступен в макросах данных, подключенные к события макрос данных.

## <a name="example"></a>Пример

Следующий пример демонстрирует действие SetReturnVar используется для возврата значения из именованный макрос данных. ReturnVar, с именем **CurrentServiceRequest** возвращается в макросе или Visual Basic для приложений (VBA) подпрограмму, которая называется именованный макрос данных.

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
