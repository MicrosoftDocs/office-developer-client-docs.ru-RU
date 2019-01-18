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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703617"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)


**Применимо к**: Access 2013, Office 2013

Служба формирования данных Microsoft для поставщика OLE DB служба поддерживает построение объектов иерархических (формы) [набора записей](recordset-object-ado.md) из поставщика данных.

## <a name="provider-keyword"></a>Ключевое слово поставщика

Для запуска службы формирования данных для OLE DB, укажите следующие ключевое слово и значение в строке подключения.

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>Динамические свойства

При вызове этого поставщика услуг в семейство сайтов [Свойства](properties-collection-ado.md) объект [подключения](connection-object-ado.md) добавляются следующие динамические свойства.

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
<td><p><strong>Изменения формы уникальные имена</strong></p></td>
<td><p>Указывает, разрешены ли объекты <strong>набора записей</strong> с повторяющихся значений для их <strong>Изменить имя</strong> свойства. Если это динамических свойство имеет <strong>значение True,</strong> и создается новый <strong>набор записей</strong> изменить имя же определенные пользователем форму как существующих <strong>записей</strong>, а затем изменяется имя нового объекта <strong>набора записей</strong> изменения формы, чтобы сделать его уникальным. Если это свойство имеет <strong>значение False</strong> и создания нового <strong>набора записей</strong> с изменить имя же определенные пользователем форму как существующих <strong>записей</strong>, оба <strong>набора записей</strong> объекта будет иметь такой же изменить имя. Таким образом ни один из <strong>набора записей</strong> форму можно изменить до тех пор, пока существует оба набора записей. Значение по умолчанию свойства имеет <strong>значение False</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Поставщик данных</strong></p></td>
<td><p>Указывает имя поставщика, который будет предоставлять строки, чтобы иметь форму. Это значение может быть нет, если поставщик не будет использоваться для предоставления строк.</p></td>
</tr>
</tbody>
</table>


Можно также установить для записи динамические свойства путем указания их имена в качестве ключевых слов в строке подключения. Например в Microsoft Visual Basic, задайте для свойства динамических **Поставщика данных** для «MSDASQL», указав:

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

Можно также задать или получить динамического свойства, указав его имя в качестве индекса в [поле свойства](properties-collection-ado.md) . К примеру получить и печать текущее значение свойства динамической **Поставщика данных** , а затем задать новое значение, следующим образом:

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

Дополнительные сведения о данных формирования [Формирования данных](data-shaping.md)см.

