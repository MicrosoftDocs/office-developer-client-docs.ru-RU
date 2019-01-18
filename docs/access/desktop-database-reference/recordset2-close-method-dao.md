---
title: Метод Recordset2.Close (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 178dec604a185da94493e6d586249bd2a633899c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708433"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="3f63d-102">Метод Recordset2.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f63d-102">Recordset2.Close method (DAO)</span></span>


<span data-ttu-id="3f63d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f63d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f63d-104">Закрытие открытых **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="3f63d-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f63d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f63d-105">Syntax</span></span>

<span data-ttu-id="3f63d-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="3f63d-106">*expression* .Close</span></span>

<span data-ttu-id="3f63d-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3f63d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f63d-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3f63d-108">Remarks</span></span>

<span data-ttu-id="3f63d-109">Если при использовании **Close**объекта **набора записей** закрыт, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="3f63d-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="3f63d-110">При попытке закрыть объект **подключения** имеет все открытые объекты **набора записей** объекты **набора записей** будут закрыты, а все ожидающие обновления или изменения будут отменены.</span><span class="sxs-lookup"><span data-stu-id="3f63d-110">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled.</span></span> <span data-ttu-id="3f63d-111">Аналогично при попытке закрыть объект **рабочей области** , имеет все открытые объекты **подключения** , эти объекты **подключения** будут закрыты, которой закрывается их объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3f63d-111">Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="3f63d-112">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="3f63d-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

