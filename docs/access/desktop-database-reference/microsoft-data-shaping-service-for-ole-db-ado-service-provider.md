---
title: Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288962"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)


**Область применения**: Access 2013, Office 2013

Служба формирования данных Майкрософт для поставщика службы OLE DB поддерживает конструкцию объектов [recordset](recordset-object-ado.md) иерархических (в виде) из поставщика данных.

## <a name="provider-keyword"></a>Ключевое слово поставщика

Чтобы вызвать службу формирования данных для OLE DB, укажите следующее ключевое слово и значение в строке подключения.

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>Динамические свойства

При вызове этого поставщика службы в коллекцию свойств объекта [Connection](connection-object-ado.md) добавляются следующие [динамические](properties-collection-ado.md) свойства.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Динамическое имя свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Уникальные имена для повторнойshape</strong></p></td>
<td><p>Указывает, разрешены <strong>ли объекты Recordset</strong> с дублирующимися значениями для их свойств <strong>reshape Name.</strong> Если это динамическое свойство имеет true и создается новый набор <strong>записей</strong> с таким же именем повторнойshape, заданным пользователем, как у существующего объекта <strong></strong> <strong>Recordset,</strong>то имя нового объекта <strong>Recordset</strong> в reshape будет изменено, чтобы сделать его уникальным. Если это свойство имеет свойство <strong>False</strong> и создается новый объект <strong>Recordset</strong> с таким же именем повторнойshape, заданным пользователем, как у существующего объекта <strong>Recordset,</strong>то оба объекта <strong>Recordset</strong> будут иметь такое же имя повторнойshape. Таким образом, ни <strong>один из наборов записей</strong> не может быть повторно скомелен, пока существуют оба наборы записей. Значение свойства по умолчанию — <strong>False.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Поставщик данных</strong></p></td>
<td><p>Указывает имя поставщика, который будет указывать строки для фигуры. Это значение может быть NONE, если поставщик не будет использоваться для предложения строк.</p></td>
</tr>
</tbody>
</table>


Можно также задать динамические свойства, которые можно переписать, указав их имена в качестве ключевых слов в строке подключения. Например, в Microsoft Visual Basic для динамического свойства **поставщика** данных установите для динамического свойства "MSDASQL", указав:

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса [для свойства Properties.](properties-collection-ado.md) Например, получите и распечатайте текущее значение динамического свойства **поставщика** данных, а затем установите новое значение, например:

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

Дополнительные сведения о формировании данных [см. в теме "Формирование данных".](data-shaping.md)

