---
title: Дополнительные сведения о сохранения записей
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed9d6e264c6bdaedcc0b921b6eed66bf1ff6afa4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946701"
---
# <a name="more-about-recordset-persistence"></a>Дополнительные сведения о сохранения записей

**Применимо к**: Access 2013, Office 2013

Объект ADO Recordset поддерживает хранение содержимого объекта **набора записей** в файл с помощью метода [сохранения](save-method-ado.md) . Постоянно хранимых файл существует на локальном диске, сетевом сервере или как URL-адрес веб-сайту. Более поздних версий файл можно восстановить с помощью любого из объекта **набора** [Open](open-method-ado-recordset.md) метод или метод [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) объект [подключения](connection-object-ado.md) .

Кроме того метод [GetString](getstring-method-ado.md) преобразует объект **набора записей** в форму, в которой столбцы и строки разделяются знаков.

Для сохранения **записей**, начните с преобразование в форме, которые могут храниться в файле. Объекты **набора записей** могут храниться в собственный формат расширенного данных TableGram (ADTG) или форматов open языке (XML). Ниже приводятся примеры ADTG. Дополнительные сведения о хранение в XML можно [Сохранение записей в формате XML](persisting-records-in-xml-format.md).

Сохраните все ожидающие изменения в файле постоянных. Это позволяет выдавать запрос, возвращающий объект **набора записей** редактирует **записей**, сохраняет его и ожидающие изменения, позднее восстанавливает **набора записей**и затем обновляет источник данных с помощью сохраненных ожидающих изменений.

Сведения о постоянно хранение объектов **потока** содержатся в разделе [потоки и сохраняемость](streams-and-persistence.md) Глава 10.

Пример сохранения **записей** содержатся в [Сценарий хранение записей XML](xml-recordset-persistence-scenario.md).

## <a name="example"></a>Пример

**Сохранение набора записей:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Откройте сохраненный файл с Recordset.Open:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

При необходимости Если **записей** нет активного подключения, можно принять значения по умолчанию и просто кода ниже:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Откройте сохраненный файл с Connection.Execute:**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Откройте сохраненный файл с RDS. DataControl:**

В этом случае свойство **сервера** не задан.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

