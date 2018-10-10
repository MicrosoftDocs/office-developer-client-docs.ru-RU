---
title: If...Then...Else Macro Block
TOCTitle: If...Then...Else Macro Block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79e5379ad2c50eff3ddf12b597defc7b85cefb39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483179"
---
# <a name="ifthenelse-macro-block"></a>If...Then...Else Macro Block


**Применимо к**: Access 2013 | Office 2013

Можно использовать макрос блок **If** позволяет выполнять группу действия в зависимости от значения выражения.

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a>Параметр

**Если** и **Else If**требуются следующие аргументы.

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
<td><p><strong>Выражение</strong></p></td>
<td><p>Условие, которое требуется проверить. Это должно быть выражение, которое оценивается как True или False.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

При выборе макрос блок **If** текстовое поле отображается таким образом, можно ввести выражение, представляющее условие, которую вы хотите проверить. Кроме того поле со списком отображается, где можно вставить действия макроса, под которой автоматически отображается текст «End If». If и End If квадратная скобка область, в котором можно ввести группу или блок действия. Блок выполняется только в том случае, если выражение, которое вводится имеет значение True.

Чтобы оценить различные выражения, если первое выражение имеет значение false, щелкните **Добавить Else If** для вставки необязательно блок **Else If** . Необходимо ввести выражение, которое оценивается как True или False. В этом случае блок выполняется только в том случае, если выражение имеет значение True и первое выражение имеет значение False.

Как вы, как в том случае, если блокировка можно добавить столько блоки **Else If** .

Щелкните **Добавить Else** для вставки блок **Else** необязательно. В этом случае действия, которые можно вставить **Else** форм блок **Else** , который выполняет только в том случае, когда не следует действий, описанных выше. **Если** блок можно добавить один блок **Else** .

В следующем примере кода макрокоманд в первый блок выполняется, если значение \[состояние\] больше 0. Если значение \[состояние\] не больше 0, исходя из **Else If** выражение. Действия макроса в блоке **Else If** выполняется, если значение \[состояние\] равно 0. И, наконец Если первый блок ни второй блок выполнение, выполните действия в блоке **Else** .

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

**Если** блоки можно вкладывать. Необходимо учитывать вложением блока **Если** блока **если** , чтобы оценить второго выражения, если первое выражение имеет значение True. В следующем примере кода внутреннего блока **If** выполняется только если значение \[состояние\] оба больше 0 *и* больше 100.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
