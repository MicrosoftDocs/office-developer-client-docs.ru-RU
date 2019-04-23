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

Служба формирования данных Майкрософт для поставщика службы OLE DB поддерживает создание иерархических объектов [Recordset](recordset-object-ado.md) от поставщика данных.

## <a name="provider-keyword"></a>Ключевое слово Provider

Чтобы вызвать службу формирования данных для OLE DB, укажите следующее ключевое слово и значение в строке подключения.

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>Динамические свойства

При вызове этого поставщика услуг следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта [Connection](connection-object-ado.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя динамического свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Уникальные имена перерисовки</strong></p></td>
<td><p>Указывает, разрешены ли объекты <strong>Recordset</strong> с повторяющимися значениями свойств <strong>имени</strong> перерисовки. Если это динамическое свойство имеет <strong>значение true</strong> и создан новый <strong>набор записей</strong> с таким же пользовательским именем изменения фигуры, что и у существующего объекта <strong>Recordset</strong>, то имя нового объекта <strong>Recordset</strong> изменяется, чтобы сделать его уникальным. Если это свойство имеет <strong>значение false</strong> и создан новый <strong>набор записей</strong> с тем же именем, что и у существующего объекта Recordset, <strong></strong>то оба объекта <strong>Recordset</strong> будут иметь одно и то же имя изменения формы. Поэтому ни один из <strong>наборов записей</strong> не может быть переопределен до тех пор, пока оба объекта Recordset существуют. Значение свойства по умолчанию — <strong>false</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Поставщик данных</strong></p></td>
<td><p>Указывает имя поставщика, который будет предоставлять строки в форме. Это значение может быть равно NONE, если поставщик не будет использоваться для предоставления строк.</p></td>
</tr>
</tbody>
</table>


Вы также можете задать динамические свойства для записи, указав их имена в виде ключевых слов в строке подключения. Например, в Microsoft Visual Basic задайте динамическое свойство **Data Provider** равным "мсдаскл", указав следующее:

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для свойства [Properties](properties-collection-ado.md) . Например, получите и распечатайте текущее значение динамического свойства **поставщика данных** , а затем задайте новое значение, как показано ниже:

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

Дополнительные сведения о процессе формирования данных см. [](data-shaping.md)

