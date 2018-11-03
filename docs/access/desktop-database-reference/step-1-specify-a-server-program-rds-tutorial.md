---
title: Этап 1. Указание серверной программы (руководство по RDS)
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5bd5e8edc17eb482177d97cb82611a8b6b12d0a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946057"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a>Шаг 1: Укажите программы сервера (учебник служб удаленных рабочих СТОЛОВ)

**Применимо к**: Access 2013, Office 2013

В общем случае используйте [RDS. Пространства данных](dataspace-object-rds.md) объекта метод [CreateObject](createobject-method-rds.md) , чтобы указать программы сервера по умолчанию, [RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственную программу настраиваемый серверный (бизнес-объект). Программа сервера создается на сервере и ссылку на программу сервера или *прокси-сервера*, возвращается.

В этом руководстве использует программы сервера по умолчанию:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

