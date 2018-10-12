---
title: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
TOCTitle: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
ms:assetid: 4503151d-de8b-98d1-1aa8-11f1b6e6b55c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249209(v=office.15)
ms:contentKeyID: 48544542
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41fd4a1aabda0887d265e3aa0ec9201b1abbbde7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482885"
---
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a>Step 4: Server Returns the Recordset (RDS Tutorial)


**Применимо к**: Access 2013 | Office 2013

Служб удаленных рабочих СТОЛОВ преобразует полученного объекта **набора записей** в форме, могут быть отправлены клиенту (то есть, оно *выполняет маршалинг* **набора записей**). Точное преобразование и способ отправки зависит ли сервера в Интернете или интрасети, локальной сети, или является библиотекой динамической компоновки. Тем не менее в этом сведений не является обязательным; все, что имеет значение, служб удаленных рабочих СТОЛОВ отправляет **записей** клиенту.

На стороне клиента объекта **набора записей** возвращается и присваивается локальной переменной.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```
