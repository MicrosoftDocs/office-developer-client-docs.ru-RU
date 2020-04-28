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

Объект ADO Recordset поддерживает сохранение содержимого объекта **Recordset** в файле с помощью метода [Save](save-method-ado.md) . Сохраняемый файл может находиться на локальном диске, сетевом сервере или в виде URL-адреса на веб-сайте. Позже файл можно восстановить с помощью метода [Open](open-method-ado-recordset.md) объекта **Recordset** или метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объекта [Connection](connection-object-ado.md) .

Кроме того, метод [GetString](getstring-method-ado.md) преобразует объект **Recordset** в форму, в которой столбцы и строки разделяются указанными символами.

Чтобы сохранить **набор записей**, начните с преобразования его в форму, которая может храниться в файле. Объекты **Recordset** могут храниться в формате дополнительных данных ТАБЛЕГРАМ (адтг) или формате Open Extensible Markup Language (XML). Примеры АДТГ приведены ниже. Для получения дополнительных сведений о сохраняемости [в формате](persisting-records-in-xml-format.md)XML см.

Сохраните все ожидающие изменения в материализованном файле. Это позволяет выдать запрос, возвращающий объект **Recordset** , изменяя **набор записей**, сохраняет его и ожидающие изменения **, в дальнейшем**восстанавливает источник данных с сохранением всех ожидающих изменений.

Сведения о постоянном хранении объектов **Stream** [можно найти в](streams-and-persistence.md) статье 10.

Пример сохраняемости в **наборе записей** представлен в [сценарии сохраняемости в XML Recordset](xml-recordset-persistence-scenario.md).

## <a name="example"></a>Пример

**Сохранение набора записей:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Откройте постоянный файл с помощью объекта Recordset. Open:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

При необходимости вы можете принять все значения по умолчанию, если в **наборе записей** нет активного подключения, и просто закодировать следующее:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Откройте постоянный файл с подключением. Execute:**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Откройте постоянный файл с помощью RDS. DataControl**

В этом случае свойство **Server** не задается.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

