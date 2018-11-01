---
title: Этап 1. Указание серверной программы (руководство по RDS)
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fe85853b013caf8610e7706f3d836551ce8801c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871880"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a><span data-ttu-id="a166c-102">Этап 1. Указание серверной программы (руководство по RDS)</span><span class="sxs-lookup"><span data-stu-id="a166c-102">Step 1: Specify a Server Program (RDS Tutorial)</span></span>


<span data-ttu-id="a166c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a166c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a166c-104">В общем случае используйте [RDS. Пространства данных](dataspace-object-rds.md) объекта метод [CreateObject](createobject-method-rds.md) , чтобы указать программы сервера по умолчанию, [RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственную программу настраиваемый серверный (бизнес-объект).</span><span class="sxs-lookup"><span data-stu-id="a166c-104">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span></span> <span data-ttu-id="a166c-105">Программа сервера создается на сервере и ссылку на программу сервера или *прокси-сервера*, возвращается.</span><span class="sxs-lookup"><span data-stu-id="a166c-105">A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="a166c-106">В этом руководстве использует программы сервера по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="a166c-106">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

