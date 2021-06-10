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

Объект ADO Recordset поддерживает хранение содержимого объекта **Recordset** в файле с помощью метода [Сохранить.](save-method-ado.md) Постоянно хранимый файл может существовать на локальном диске, сетевом сервере или в качестве URL-адреса на веб-сайте. Позже файл можно восстановить с помощью метода [](open-method-ado-recordset.md) Open объекта **Recordset** или метода [Выполнения](connection-object-ado.md) объекта [Подключения.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)

Кроме того, метод [GetString](getstring-method-ado.md) преобразует объект **Recordset** в форму, в которой столбцы и строки делимитированы с символами, которые вы указываете.

Чтобы сохранить **набор записей,** начните с преобразования его в форму, которая может храниться в файле. **Объекты recordset** можно хранить в фирменом формате Advanced Data TableGram (ADTG) или в формате open Extensible Markup Language (XML). Ниже показаны примеры ADTG. Дополнительные сведения о сохраняемости XML см. в см. в рублях ["Сохранение записей в формате XML".](persisting-records-in-xml-format.md)

Сохраните все ожидающих изменений в сохраняемом файле. Это позволяет выдать запрос, возвращающий объект **Recordset,** изменить набор **recordset,** сохранить его и ожидающих изменений, а затем восстановить набор **recordset,** а затем обновить источник данных с сохраненными ожидающих изменений.

Сведения о постоянном хранении объектов **Stream** см. в [Потоки и сохраняемость](streams-and-persistence.md) в главе 10.

Пример сохранения **Recordset** см. в [XML-сценарии](xml-recordset-persistence-scenario.md)сохранения записей.

## <a name="example"></a>Пример

**Сохранить набор записей:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Откройте файл сохраняемой папкой Recordset.Open:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

Необязательно, если **в Наборе записей** нет активного подключения, вы можете принять все по умолчанию и просто кодировать следующее:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Откройте сохраняемого файла с Connection.Exeмило:**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Откройте сохраняемый файл с помощью RDS. DataControl:**

В этом случае свойство **Server** не заданной.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

