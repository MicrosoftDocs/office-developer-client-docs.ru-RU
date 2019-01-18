---
title: Дополнительные сведения о сохранении наборов записей
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 194dcf3826409c91f8d046b39b9009b43aee5477
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717610"
---
# <a name="more-about-recordset-persistence"></a>Дополнительные сведения о сохранении наборов записей

**Применимо к**: Access 2013, Office 2013

Объект ADO Recordset поддерживает хранение содержимого объекта **набора записей** в файл с помощью метода [сохранения](save-method-ado.md) . Постоянно хранимых файл существует на локальном диске, сетевом сервере или как URL-адрес веб-сайту. Более поздних версий файл можно восстановить с помощью любого из объекта **набора** [Open](open-method-ado-recordset.md) метод или метод [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объект [подключения](connection-object-ado.md) .

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

