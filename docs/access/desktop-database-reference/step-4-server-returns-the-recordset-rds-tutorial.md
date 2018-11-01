---
title: Этап 4. Возврат набора записей сервером (руководство по RDS)
TOCTitle: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
ms:assetid: 4503151d-de8b-98d1-1aa8-11f1b6e6b55c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249209(v=office.15)
ms:contentKeyID: 48544542
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c7aaaa556d11fc3c457c89a35edb1240628aa9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868625"
---
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a><span data-ttu-id="523e8-102">Этап 4. Возврат набора записей сервером (руководство по RDS)</span><span class="sxs-lookup"><span data-stu-id="523e8-102">Step 4: Server Returns the Recordset (RDS Tutorial)</span></span>


<span data-ttu-id="523e8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="523e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="523e8-104">Служб удаленных рабочих СТОЛОВ преобразует полученного объекта **набора записей** в форме, могут быть отправлены клиенту (то есть, оно *выполняет маршалинг* **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="523e8-104">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**).</span></span> <span data-ttu-id="523e8-105">Точное преобразование и способ отправки зависит ли сервера в Интернете или интрасети, локальной сети, или является библиотекой динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="523e8-105">The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library.</span></span> <span data-ttu-id="523e8-106">Тем не менее в этом сведений не является обязательным; все, что имеет значение, служб удаленных рабочих СТОЛОВ отправляет **записей** клиенту.</span><span class="sxs-lookup"><span data-stu-id="523e8-106">However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="523e8-107">На стороне клиента объекта **набора записей** возвращается и присваивается локальной переменной.</span><span class="sxs-lookup"><span data-stu-id="523e8-107">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

