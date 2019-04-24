---
title: Свойство Recordset. UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ced8fc78729924ce271aa0fe38d77d287a131f13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307534"
---
# <a name="recordsetupdateoptions-property-dao"></a>Свойство Recordset. UpdateOptions (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . UpdateOptions

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

При выполнении **[обновления](recordset-update-method-dao.md)** пакетного режима, DAO и библиотека курсора клиентских пакетов создайте ряд инструкций SQL UPDATE, чтобы внести необходимые изменения. Предложение WHERE (SQL) создается для каждого обновления, чтобы изолировать записи, помеченные как измененные свойством **[рекордстатус](recordset-recordstatus-property-dao.md)** . Так как некоторые удаленные серверы используют триггеры или другие способы обеспечения целостности данных, часто важно ограничить обновление полей только теми, которые затрагиваются этим изменением. 

Для этого присвойте свойству **UpdateOptions** одно из констант **дбкритериакэй**, **дбкритериамодвалуес**, **дбкритериааллколс**или **дбкритериатиместамп**. Таким образом выполняется только абсолютный минимальный объем кода триггера. В результате операция обновления выполняется быстрее, и в ней уменьшается количество потенциальных ошибок.

Вы также можете сцепить любую константу **дбкритериаделетеинсерт** или **дбкритериаупдате** , чтобы определить, следует ли использовать набор инструкций SQL DELETE и INSERT или инструкцию SQL UPDATE для каждого обновления при отправке пакетных изменений. обратно на сервер. В первом случае для обновления записи требуется две отдельные операции. В некоторых случаях, особенно когда удаленная система реализует триггеры DELETE, INSERT и UPDATE, выбор правильного значения свойства **UpdateOptions** может значительно повлиять на производительность.

Если не указать константы, будут использоваться **дбкритериаупдате** и **дбкритериакэй** .

Только что добавленные записи будут всегда создавать операторы INSERT и удаленные записи, которые всегда будут создавать операторы DELETE, поэтому это свойство применяется только к обновлению записей в библиотеке курсоров.

## <a name="example"></a>Пример

В этом примере используются свойства **BatchSize** и **UpdateOptions** для управления аспектами обновления пакетов для указанного объекта **Recordset** .

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

