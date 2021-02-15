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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288850"
---
# <a name="more-about-recordset-persistence"></a>Дополнительные сведения о сохранении наборов записей

**Область применения**: Access 2013, Office 2013

Объект ADO Recordset поддерживает хранение содержимого объекта **Recordset** в файле с помощью метода [Save.](save-method-ado.md) Постоянно хранимый файл может существовать на локальном диске, сетевом сервере или в качестве URL-адреса на веб-сайте. Позднее файл можно восстановить с помощью метода [Open](open-method-ado-recordset.md) объекта **Recordset** или метода [Execute объекта](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) [Connection.](connection-object-ado.md)

Кроме того, метод [GetString](getstring-method-ado.md) преобразует объект **Recordset** в форму, в которой столбцы и строки размещены символами, которые вы указываете.

Чтобы сохранить **набор записей,** начните с его преобразования в форму, которая может храниться в файле. **Объекты recordset** можно хранить в проприетарном формате Advanced Data TableGram (ADTG) или в формате XML. Ниже показаны примеры ADTG. Дополнительные сведения о сохраняемости XML см. в записях [в формате XML.](persisting-records-in-xml-format.md)

Сохраните ожидающих изменений в сохраняемом файле. Это позволяет вам выдавать запрос, который возвращает объект **Recordset,** изменяет набор **записей,** сохраняет его и ожидающих изменений, затем восстанавливает набор **записей,** а затем обновляет источник данных сохраненными ожидающих изменений.

Сведения о постоянном хранении объектов **Stream** см. в главе 10 "Потоки и [сохраняемость".](streams-and-persistence.md)

Пример **сохраняемости recordset** см. в сценарии [сохраняемости наборов записей XML.](xml-recordset-persistence-scenario.md)

## <a name="example"></a>Пример

**Сохраните набор записей:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Откройте сохраняемой файл с помощью Recordset.Open:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

При желании, если у **recordset** нет активного подключения, вы можете принять все значения по умолчанию и просто в коде:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Откройте сохраняемого файла с помощью Connection.Execute:**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Откройте сохраняемой файл с помощью RDS. DataControl:**

В этом случае свойство **Server** не за установлено.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

