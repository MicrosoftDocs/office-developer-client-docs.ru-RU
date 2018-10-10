---
title: 'Step 1: Specify a Server Program (RDS Tutorial)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89aa87aa63a3d8bfdeb291f78d6525f51c4262b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479740"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a><span data-ttu-id="b5935-102">Step 1: Specify a Server Program (RDS Tutorial)</span><span class="sxs-lookup"><span data-stu-id="b5935-102">Step 1: Specify a Server Program (RDS Tutorial)</span></span>


<span data-ttu-id="b5935-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5935-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b5935-104">В общем случае используйте [RDS. Пространства данных](dataspace-object-rds.md) объекта метод [CreateObject](createobject-method-rds.md) , чтобы указать программы сервера по умолчанию, [RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственную программу настраиваемый серверный (бизнес-объект).</span><span class="sxs-lookup"><span data-stu-id="b5935-104">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span></span> <span data-ttu-id="b5935-105">Программа сервера создается на сервере и ссылку на программу сервера или *прокси-сервера*, возвращается.</span><span class="sxs-lookup"><span data-stu-id="b5935-105">A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="b5935-106">В этом руководстве использует программы сервера по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b5935-106">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

