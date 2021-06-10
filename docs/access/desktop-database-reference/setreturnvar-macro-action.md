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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308675"
---
# <a name="setreturnvar-macro-action"></a>Макрокоманда SetReturnVar

**Область применения**: Access 2013, Office 2013

Действие **SetReturnVar** создает переменную возврата и задает ее определенному значению.

> [!NOTE]
> Действие **SetReturnVar** доступно только в макросах данных.

## <a name="setting"></a>Параметр

Действие **SetReturnVar** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Да</p></td>
<td><p>Строка, определяющая имя переменной.</p></td>
</tr>
<tr class="even">
<td><p>Expression</p></td>
<td><p>Да</p></td>
<td><p>Выражение, которое будет использоваться для задания значений для данной временной переменной. Не ставьте перед выражением знак равенства (=). Вы можете нажать кнопку <strong>Build</strong>, чтобы использовать <strong>Создатель выражений</strong> для установки данного аргумента.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

Действие **SetReturnVar** используется для создания **returnVar**, переменной, которая может использоваться макросами, которые называют макрос данных с помощью **действия RunDataMacro.**

После создания **ReturnVar** с помощью действия **SetReturnVar** макрос вызова может использовать его в выражении. Например, если вы создали **ReturnVar** с именем **UpdateSuccess,** переменную можно использовать с помощью следующего синтаксиса:

```vb
    =[ReturnVars]![UpdateSuccess]
```

Действие **SetReturnVar** можно использовать только в названных макросах данных. Он не доступен в макросах данных, присоединенных к событию макрос данных.

## <a name="example"></a>Пример

В следующем примере показано, как использовать действие SetReturnVar для возврата значения из названного макроса данных. ReturnVar с именем **CurrentServiceRequest** возвращается в макрос или Visual Basic для приложений (VBA), который называется названным макросом данных.

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
